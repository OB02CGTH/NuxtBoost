<template>
  <section>
    <o-field label="First name" labelClass="block mb-2 text-sm font-medium text-gray-900 dark:text-white">
      <o-input inputClass="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"  placeholder="John" v-model="name"></o-input>
    </o-field>

    <o-field label="Password" labelClass="block mb-2 text-sm font-medium text-gray-900 dark:text-white">
      <o-input type="password" value="iwantmytreasure" inputClass="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="•••••••••" password-reveal>
      </o-input>
    </o-field>

    <o-field label="Email" variant="success" message="This email is invalid">
      <o-input type="email" value="john@" maxlength="30"> </o-input>
    </o-field>
    
    <o-field label="Email" variant="danger" message="This email is invalid">
      <o-input type="email" value="john@" maxlength="30"> </o-input>
    </o-field>
  </section>
</template>

<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({
  setup() {
    const email = ref('');
    
    function searchIconClick() {
      alert('You wanna make a search?');
    }
    
    function clearIconClick() {
      email.value = '';
      alert('Email cleared!');
    }

    return {
      email,
      searchIconClick,
      clearIconClick,
    };
  },
});
</script>

<style>
  .o-input--success {
    @apply bg-green-50 border border-green-500 text-green-900 dark:text-green-400 placeholder-green-700 dark:placeholder-green-500 text-sm rounded-lg focus:ring-green-500 focus:border-green-500 block w-full p-2.5 dark:bg-gray-700 dark:border-green-500
  }
  .o-input--danger {
    @apply bg-red-50 border border-red-500 text-red-900 placeholder-red-700 text-sm rounded-lg focus:ring-red-500 dark:bg-gray-700 focus:border-red-500 block w-full p-2.5 dark:text-red-500 dark:placeholder-red-500 dark:border-red-500
  }
  .o-input--primary {
    @apply w-4 h-4 text-blue-600 bg-blue-100 border-blue-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-blue-800 focus:ring-2 dark:bg-blue-700 dark:border-blue-600
  }
</style>