<template>
    <main class="  p-24 min-h-screen bg-slate-900  ">
      <div class=" m-3 md:max-w-md max-w-4xl justify-center items-center  mx-auto rounded-lg  ">
        
        
        <h2 class="mt-6 m-3 text-center text-2xl font-extrabold text-orange-600">
          Sign in to your account 
        </h2>
      <form  @submit.prevent="onSubmit"  class=" rounded-lg md:border border-white flex-col gap-y-2 bg-transparent flex justify-center items-center  py-4 mx-auto">
        <img src="https://cdn.pixabay.com/photo/2015/07/17/22/43/student-849825_960_720.jpg" alt="" class=" h-8 w-8 flex justify-center items-center mx-auto  rounded-full bg-white">
        
          <label  class=" m-2  text-white font-extrabold">Email Address</label>
          <input  v-model="email" name="Email" type="email" class=" px-10 py-2 rounded-md flex justify-center items-center gap-2 flex-col" required placeholder="Enter your email"/>
        <span   name="Email"  class="text-red-600"/>
        <label  class=" m-3  text-white font-extrabold"> password</label>
        <input v-model="password" name="password" type="password"  class="  px-10 py-2 rounded-md flex justify-center items-center gap-2 flex-col"  required placeholder="Enter your password"/>
        <span name="password"  class="text-red-600" v-show="passErrorActivate">{{passwordError}}</span>  
        <div class="">
          <input type="checkbox" class=" bg-orange-600 h-4 w-4 m-1"><span class="text-white">Remember me</span>
         </div>
  
  
        <button class=" px-6 py-2 m-3  font-bold text-orange-600  text-lg hover:text-black  hover:bg-orange-600 bg-black rounded-md">submit</button>
        
         
        <div class="  text-orange-600  font-bold"> Don't have an account? <span><router-link to="/signup" class="  text-white">Signup</router-link></span></div>
  
         
      </form>
    </div>
    </main>
  
  
          
  <main/>
  </template>
  
  <script>   
  export default{
    data(){
      return{
        
       email:"",
       password:"",
       confirmPassword:"",
       passwordError:"password must be atleast 8 characters",
       passErrorActivate:false
  
      }
    },
    methods:{
      
      async onSubmit(){
       
      if(this.password.length<8 && this.confirmPassword.length<8){
        this.passErrorActivate=true
      }
      else{
        /* let url="http://localhost:7000/login/" */
        let url="api/v1/login/"
         let data=JSON.stringify({
         
                      email: this.email,
                      password: this.password,
                     
         })
         let res= await fetch(url,{
           headers:{
             "Content-type":"application/json"
           },
           method:"POST",
           body:data
         })
         if(res.ok){
           let data=await res.json()
           console.log(data);
           alert(data.message)
           this.$router.push("/services")
         }
         else{
           let data=await res.json()
           console.log(data)
           alert(data.message)
         }
      }
        
     }
    }
  }
  
  
  </script>
  
  
  <style>
  
  </style>