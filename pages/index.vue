<template>
    <div>
      <div class="grid grid-cols gap-4 mt-5">
    <div class=" flex justify-center items-center p-3">
      <h1>Register Form</h1>
    </div>
  
    <div class=" flex justify-center p-5 sm:p-0">
      <form @submit.prevent="submitForm" class=" p-5 bg-white rounded-lg frm">
        <div class="mb-4">
          <label for="username" class="block text-xl font-medium text-black-600" >Username</label>
          <input v-model="username" type="text" id="username" name="username" class="mt-1 p-2 w-full border rounded-md" placeholder="Enter your username">
        </div>
  
        <div class="mb-4">
          <label for="email" class="block text-xl font-medium text-black-600">Email</label>
          <input v-model="email" type="email" id="email" name="email" class="mt-1 p-2 w-full border rounded-md"  placeholder="Enter your email">
        </div>
  
        <div class="mb-4">
          <label for="text" class="block text-xl font-medium text-black-600" >Phone Number</label>
          <input v-model="mobile" type="text" id="text" name="text" class="mt-1 p-2 w-full border rounded-md" placeholder="Enter your phone number">
        </div>
  
        <div class="mb-4">
          <label for="date" class="block text-xl font-medium text-black-600">Date of birth</label>
          <input v-model="dob" type="date" id="date" name="date" class="mt-1 p-2 w-full border rounded-md"  placeholder="Date of birth">
        </div>
        <div class="mb-4">
          <label class="block text-xl font-medium text-black-600  mb-2" >Gender</label>
          <div class="flex">
            <label class="inline-flex items-center mr-4">
              <input v-model="gender" type="radio" name="gender" value="male" class="form-radio text-blue-500">
              <span class="ml-2">Male</span>
            </label>
            <label class="inline-flex items-center">
              <input v-model="gender" type="radio" name="gender" value="female" class="form-radio text-pink-500">
              <span class="ml-2">Female</span>
            </label>
          </div>
        </div>
        <div class="mb-4">
          <label for="text" class="block text-xl font-medium text-black-600" >Address</label>
          <input v-model="address" type="text" id="text" name="text" class="mt-1 p-2 w-full border rounded-md" placeholder="Address">
        </div>
  
        <div class="mb-4">
          <label for="text" class="block text-xl font-medium text-black-600" >Country</label>
          <input v-model="country" type="text" id="text" name="text" class="mt-1 p-2 w-full border rounded-md" placeholder="country">
        </div>
        <div class="mb-4">
          <label for="text" class="block text-xl font-medium text-black-600" >Postal number</label>
          <input v-model="postal" type="text" id="text" name="text" class="mt-1 p-2 w-full border rounded-md" placeholder="Postal number">
        </div>
        <button type="submit" class="w-full bg-red-500 text-white py-2 px-4 rounded-md hover:bg-blue-600 focus:outline-none focus:ring focus:border-blue-300">Register</button>
      </form>
    </div>
  </div>
    </div>
  </template>
  
  <script>
     export default{
          methods:{
              submitForm(){
                  const formData={
                      username:this.username,
                      email:this.email,
                      mobile:this.mobile,
                      dob:this.dob,
                      gender:this.gender,
                      address:this.address,
                      country:this.country,
                      postal:this.postal
                  };
                  this.$router.push({
                      path:'/another-page',
                      query:formData
                  });
              },
          },
      };
  </script>
  
  <style scoped>
  h1{
    font-size: 2rem;
    color: aliceblue;
    font-weight: bold;
  }
  .frm{
    width: 50%;
  }
  @media(max-width:992px){
    .frm{
    width: 100%;
  }
  }
  </style>