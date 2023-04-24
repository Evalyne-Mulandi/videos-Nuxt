<template>
    <main class="  p-24 min-h-screen bg-slate-900  ">
      <div class=" m-3 md:max-w-md max-w-4xl justify-center items-center  mx-auto rounded-lg  ">
          <!-- success alert -->
        <div class="mb-4" v-if="success">
        <div
          class="bg-green-700 border  text-white px-4 py-3 rounded relative"
          role="alert"
        >
          <strong class="font-bold">Success! </strong>
          <span class="block sm:inline">{{ success }}.</span>
        </div>
      </div>
         <!-- error alert -->
      <div class="mb-4" v-if="errMsg">
        <div
          class="bg-red-500 border  text-white px-4 py-3 rounded relative"
          role="alert"
        >
          <strong class="font-bold">Error! </strong>
          <span class="block sm:inline">{{ errMsg }}.</span>
        </div>
      </div>
        <div class="max-w-md mx-auto my-4 p-4 bg-transparent  border border-white rounded-md shadow-md">
     
     
      
      
      <Loading v-if="loading" />
      <form @submit.prevent="login">
        <h2 class=" text-center text-2xl font-extrabold text-orange-600">
          Sign in to your account 
        </h2>
        <div class="mb-4">
          <label class="block text-white font-medium mb-2" for="email"> Email </label>
          <input
            class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            id="email"
            v-model="email"
            type="email"
            placeholder="Enter your email"
          />
        </div>
        <div class="mb-4">
          <label class="block text-white font-medium mb-2" for="password">
            Password
          </label>
          <input
            class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            id="password"
            type="password"
            v-model="password"
            placeholder="Enter your password"
          />
        </div>
     <!--   <div class="mb-4">
          <label class="block text-white font-medium mb-2" for="password-confirm">
            Confirm Password
          </label>
          <input
            class="appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            id="password-confirm"
            v-model="passwordConfirm"
            type="password"
            placeholder="Confirm your password"
          />
        </div> -->
      
        <button
          class="bg-orange-600 hover:bg-black text-white font-medium py-2 px-4 rounded focus:outline-none focus:shadow-outline"
          type="submit"
        >
          login
        </button>
      </form>
      
      <p class="mt-4 justify-center items-center flex font-bold text-orange-600">
        Don't have an account?
        <NuxtLink to="/register" class="text-white hover:underline"> Sign up </NuxtLink>
      </p>
    </div>
  </div>
  </main>
</template>

<script setup>
import { ref } from "vue";
const auth = useSupabaseAuthClient();
let email = ref("");
let password = ref("");
let passwordConfirm = ref("");
const router = useRouter();
let errMsg = ref(null);
let loading = ref(false);
let success = ref("");

const login = async () => {
 /*  if (password.value !== passwordConfirm.value) {
    errMsg.value = "Passwords do not match";
    return;
  } */
  try {
    loading.value = true;
    errMsg.value = null;
    const { data, error } = await auth.auth.signInWithPassword({
      email: email.value,
      password: password.value,
    });
    if (error) {
      loading.value = false;
      errMsg.value = "Invalid email or password";
       
    }
    if (data) {
      //success.value = `Welcome ${data.user.email?.split("@")[0]}`;
      success.value="logged in successfully"

      setTimeout(() => {
        loading.value = false;
      }, 3000);
      email.value = "";
      password.value = "";
      passwordConfirm.value = "";
      window.location.href = "/";
      router.push("/");
    }
  } catch (err) {
    loading.value = false;
    errMsg.value = "Invalid email or password";
    
    
  }
};
/* signin with github */
const loginWithGithub = async () => {
  const { error } = await auth.auth.signInWithOAuth({
    provider: "github",
  });
  if (error) {
    errMsg.value = error.message;
  } else {
    setTimeout(() => {
      loading.value = false;
    }, 3000);
    email.value = "";
    password.value = "";
    passwordConfirm.value = "";
    router.push("/");
  }
};
</script>

<style scoped></style>
