<template>
  <div class="mt-4">
    <h1 class="text-2xl font-semibold text-gray-700 dark:text-gray-300">About me</h1>
    <p class="text-sm dark:text-gray-400 text-gray-700">
    Amet delectus commodi repudiandae cupiditate officiis consectetur. Harum perspiciatis culpa a amet earum Praesentium libero voluptas quaerat amet enim. Rem ipsa sapiente ad labore aliquid Recusandae quaerat iure aspernatur numquam.

      <br>
      <br>

      Dolor quasi error in vitae exercitationem Velit officia cumque blanditiis accusantium animi iusto. Similique nam delectus aliquam repellendus enim ab perferendis In odit perspiciatis aliquam libero velit? Explicabo animi exercitationem.
      <br />
      <br />
      Dolor enim nulla dolorem numquam possimus? Deleniti officiis similique sint soluta maxime rerum iusto, nesciunt? Assumenda hic blanditiis fuga illum rerum, architecto. Neque reiciendis labore iste accusantium soluta adipisci numquam

      <br />
      <br />
      <div>Sit et laudantium voluptatum debitis placeat illum ab. Voluptas harum consequuntur quas consequuntur quia? Soluta hic ab et laborum veritatis expedita fugit vel. Vitae maxime esse architecto nam error eveniet?</div>
      <div>Adipisicing rem dolor autem quam tenetur? Consequuntur distinctio eum eveniet expedita nemo, doloribus aspernatur In ad aliquid voluptates blanditiis sapiente, quibusdam? Veritatis totam nobis quia fuga placeat. Nam culpa mollitia</div>
      
    </p>

  </div>
  <main-skills />
  <div class="flex justify-end">
    <router-link to="/skills" class="px-6 py-2 font-semibold text-gray-700 dark:text-gray-300  hover:text-blue-600 drop-shadow-lg rounded-xl">More Skills...</router-link>
  </div>
  <experience/>
  <education/>
</template>
<script>
import MainSkills from "../components/Home/MainSkills.vue";
import Education from "../components/Home/Education.vue";
import Experience from "../components/Home/Experience.vue";

export default {
  components: { MainSkills, Experience, Education },
};
</script>
