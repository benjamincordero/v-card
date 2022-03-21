<script>
  import profile_foto from "../assets/me.jpg";
  export default{
    data(){
      return {profile_foto:profile_foto}
    }
  }
</script>
<template>
  <div class="flex flex-col gap-3">
    <div class="flex justify-center">
      <img
        class="mt-6 w-1/4 xl:w-2/4 rounded-3xl drop-shadow-xl"
        :src="profile_foto"
        alt="profile_foto"
      />
    </div>
    <div class="mt-3">
      <p class="text-2xl text-center text-slate-900 dark:text-gray-50">
        Walter<span class="font-bold">&nbsp;Shaw</span>
      </p>
    </div>
    <div class="text-center">
      <span class="px-4 py-2 text-xs text-gray-100 dark:bg-slate-800 dark:text-gray-300 bg-blue-600 rounded-full">
        <i class="fa-solid fa-terminal"></i>&nbsp;Software Developer
      </span>
    </div>
    <div class="flex justify-center text-xl text-gray-600 dark:text-gray-400 gap-3">
        <a href="https://twitter.com/webonada" class="hover:text-blue-500 " target="_blank"><i class="fa-brands fa-twitter"></i></a>
        <a href="https://github.com/benjamincordero" class="hover:text-gray-800 dark:hover:text-gray-500" target="_blank"><i class="fa-brands fa-github"></i></a>
        <a href="https://www.instagram.com/benjamincordero/" class="hover:text-yellow-500" target="_blank"><i class="fa-brands fa-instagram"></i></a>
        <a href="https://www.linkedin.com/in/benjam%C3%ADn-josu%C3%A9-cordero-c%C3%A1rdenas-47a7b5ba/" class="hover:text-blue-800" target="_blank"><i class="fa-brands fa-linkedin-in"></i></a>
    <a href="https://t.me/benjamincordero" class="hover:text-blue-600" target="_blank"><i class="fa-brands fa-telegram"></i></a>

    </div>
    <div id="info" class="pt-2">
      <ul class="flex flex-wrap justify-center px-6 text-xs text-gray-600 dark:text-gray-400 xl:flex-col gap-3">
        <li><i class="fa fa-calendar-days"></i>&nbsp;28 March, 1992 </li>
        <li><i class="fa fa-location-dot"></i>&nbsp;Miami, Fl</li>
        <li><i class="fa fa-envelope"></i>&nbsp;contacto@mail.com</li>
        <li><i class="fa fa-phone"></i>&nbsp;305-509-6995</li>
      </ul>
    </div>
    <div class="flex justify-center">
      <a href="javascript:;" class="px-4 py-2 my-5 text-center text-white bg-blue-600 xl:w-full rounded-xl drop-shadow-xl hover:bg-blue-500">
        <i class="fa fa-download"></i>&nbsp;Download CV
      </a>
    </div>
    
  </div>
</template>

