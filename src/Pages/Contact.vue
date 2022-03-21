<template>
  <div class="lg:px-8">
    <h1 class="mt-5 text-xl font-bold text-gray-700 dark:text-gray-300"><i class="fa-solid fa-envelope"></i> Contact</h1>
    <p class="mb-4 text-sm text-gray-600 dark:text-gray-300">Elit cupiditate libero similique voluptas repellat quibusdam</p>
    <form @submit.prevent="sendMail">
      <div class="flex flex-wrap">
        <div class="w-full lg:pr-1 lg:w-1/2">
          <span class="text-sm font-bold text-gray-600 dark:text-gray-300 uppercase" :class="[fullname_validate ? 'text-red-500' : '']">Name</span>
          <input class="w-full p-3 mt-2 text-gray-900 dark:bg-blue-200 bg-gray-200 rounded-lg focus:bg-gray-300 focus:outline-none focus:shadow-outline"
            type="text" @keyup="validate" placeholder="Your Name" :class="[fullname_validate ? 'bg-red-200' : '']" v-model="fullname">
          <span class="mt-1 text-sm text-red-500" :class="[fullname_validate ? 'block' : 'hidden']">Required field</span>
        </div>
        <div class="w-full lg:pl-1 lg:w-1/2">
          <span class="text-sm font-bold dark:text-gray-300 text-gray-600 uppercase" :class="[email_validate ? 'text-red-500' : '']">Email</span>
          <input class="w-full p-3 mt-2 text-gray-900 dark:bg-blue-200 bg-gray-200 rounded-lg focus:bg-gray-300 focus:outline-none focus:shadow-outline"
            type="email" @keyup="validate" placeholder="Email" :class="[email_validate ? 'bg-red-200' : '']" v-model="email">
          <span class="mt-1 text-sm text-red-500" :class="[email_validate ? 'block' : 'hidden']">Required field</span>
        </div>
      </div>
      <div class="mt-8">
          <span class="text-sm font-bold text-gray-600 dark:text-gray-300 uppercase" :class="[subject_validate ? 'text-red-500' : '']">Subject</span>
          <input class="w-full p-3 mt-2 text-gray-900 bg-gray-200 dark:bg-blue-200 rounded-lg focus:bg-gray-300 focus:outline-none focus:shadow-outline"
            type="text" @keyup="validate" placeholder="Subject" :class="[subject_validate ? 'bg-red-200' : '']" v-model="subject">
          <span class="mt-1 text-sm text-red-500" :class="[subject_validate ? 'block' : 'hidden']">Required field</span>
        </div>
      <div class="mt-8">
        <span class="text-sm font-bold text-gray-600 dark:text-gray-300 uppercase" :class="[message_validate ? 'text-red-500' : '']">Message</span>
        <textarea
          class="w-full h-32 p-3 mt-2 text-gray-900 bg-gray-200 rounded-lg dark:bg-blue-200 focus:bg-gray-300 focus:outline-none focus:shadow-outline" :class="[message_validate ? 'bg-red-200' : '']" v-model="message" @keyup="validate" placeholder="Your message"></textarea>
          <span class="mt-1 text-sm text-red-500" :class="[message_validate ? 'block' : 'hidden']">Requiered field</span>
      </div>
      <div class="flex justify-end mt-8 mb-4">
        <button
          type="submit"
          class="px-4 py-3 text-sm font-bold tracking-wide text-gray-100 uppercase bg-blue-600 rounded-lg hover:bg-blue-500 focus:outline-none focus:shadow-outline">
          Send Message 
        </button>
      </div>
  </form>
  </div>
</template>
<script>
  export default{

    name:'Contact',
    data(){
      return {
        fullname:'',
        email:'',
        message:'',
        asunto:'',
        fullname_validate:false,
        email_validate:false,
        subject_validate:false,
        error:[],
      }
     },
    methods:{
      validate(){
        this.email_validate = false;
        this.fullname_validate = false;
        this.message_validate = false;
        this.subject_validate = false;
        let validated = true;
        if(!this.fullname){
          this.fullname_validate = true; 
          validated = false;
        }
        if(!this.email){
          this.email_validate = true; 
          validated = false;
        }
        if(!this.message){
          this.message_validate = true; 
          validated = false;         
        }
        if(!this.subject){
          this.subject_validate = true; 
          validated = false;        
        }
        return validated;
      },
      sendMail(){
        console.log(this.validate());
      }
    },
  }

</script>
