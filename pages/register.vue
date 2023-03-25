<template>
    <main class="">
      
      <div class="  p-12 min-h-screen bg-slate-900">
        <h2 class="mt-4 m-6 text-center text-2xl font-extrabold text-orange-600">
          Sign up to your account 
        </h2>
   
        <form @submit.prevent="onSubmit"   class="  py-4 md:border border-white mt-1 flex flex-col gap-y-2  mx-auto justify-center items-center max-w-lg
            bg-transparent text-black rounded-md">
            <img src=" https://cdn.pixabay.com/photo/2015/07/17/22/43/student-849825_960_720.jpg" alt="" class="  flex justify-center items-center mx-auto h-8 w-8 rounded-full bg-white"> 
          
        <label class="text-white">First Name</label>
        <input  v-model="firstName" name="firstName" type="text" class=" p-2 px-10   rounded-md " required placeholder="Enter your first name"/>
        <span name="firstName" class="text-red-600" />
        
        <label class="text-white">last Name</label>
        <input  v-model="lastName" name="lastName" type="text"  class=" p-2 px-10   rounded-md " required placeholder="Enter your last name"/>
        <span name="lastName" class="text-red-600" />   
        
        

        <label class="text-white">Email Address</label>
        <input  v-model="email" name="Email" type="email" class=" p-2 px-10    rounded-md   " autocomplete   required placeholder="Enter your email"/>
        <span name="Email"  class="text-red-600"/>

        <label class="text-white">Password</label>
        <input  v-model="password" name="password" type="password"  class=" p-2 px-10   rounded-md " autocomplete placeholder="Enter your password"/>
        <span name="password"  class="text-red-600" v-show="passErrorActivate">{{passwordError}}</span>  

        <label class="text-white">confirm Password</label>
        <input  v-model="confirmPassword" name=" confirmPassword" type="password"  class=" p-2 px-10   rounded-md " autocomplete placeholder="Confirm your password"/>
        <span name="password"  class="text-red-600" v-show="passErrorActivate">{{passwordError}}</span>
        <button class=" rounded-lg px-6 py-2 p-4 gap-2 text-orange-600 hover:text-black hover:bg-orange-600 bg-black" type="submit">Submit</button>
        <div class="  text-orange-600  font-bold"> Already have an account? <span><router-link to="/signup" class="  text-white">login</router-link></span></div>
      </Form>
      </div>
    </main>
  </template>
  
  <script>   
  export default{
    data(){
      return{
       firstName:"",
       lastName:"",
       phoneNumber:"",
       email:"",
       password:"",
       confirmPassword:"",
       passwordError:"password must be atleast 8 characters",
       passErrorActivate:false
  
      }
    },
    methods:{
      
      async onSubmit(){
        const pattern="^0(7(?:(?:[129][0-9])|(?:0[0-8])|(4[0-1]))[0-9]{6})$"
        let num="0768982944"
         const found = num.match(pattern);
      if(this.password.length<8 && this.confirmPassword.length<8){
        this.passErrorActivate=true
      }/* else if(found){
         alert("wrong phone number")
         console.log(found);
      } */
      else{
        /* let url="http://localhost:7000/signup/" */
        let url="api/v1/signup/"
         let data=JSON.stringify({
          firstName: this. firstName,
                      lastName: this.lastName,
                      phoneNumber:this.phoneNumber,
                      email: this.email,
                      password: this.password,
                      confirmPassword: this.confirmPassword,
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
           this.$router.push("/login")
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