<template>
  <section>
    <o-field rootClass="block mb-2 text-sm font-medium" label="First name">
      <o-input inputClass="border block w-full p-2.5 text-sm rounded-lg" placeholder="John" v-model="name"></o-input>
    </o-field>

    <o-field rootClass="block mb-2 text-sm font-medium" label="Password">
      <o-input inputClass="border block w-full p-2.5 text-sm rounded-lg" type="password" value="iwantmytreasure" placeholder="•••••••••" password-reveal>
      </o-input>
    </o-field>

    <o-field rootClass="block mb-2 text-sm font-medium" variant="success" label="Email" message="This email is invalid">
      <o-input inputClass="border block w-full p-2.5 text-sm rounded-lg"  type="email" value="john@" maxlength="30"> </o-input>
    </o-field>
    
    <o-field rootClass="block mb-2 text-sm font-medium" variant="danger" label="Email" message="This email is invalid">
      <o-input inputClass="border block w-full p-2.5 text-sm rounded-lg" type="email" value="john@" maxlength="30"> </o-input>
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
    @apply bg-green-50 border-green-500 text-green-900 dark:text-green-400 placeholder-green-700 dark:placeholder-green-500 focus:ring-green-500 focus:border-green-500 dark:bg-gray-700 dark:border-green-500
  }
  .o-input--danger {
    @apply bg-red-50 border-red-500 text-red-900 placeholder-red-700 focus:ring-red-500 dark:bg-gray-700 focus:border-red-500 dark:text-red-500 dark:placeholder-red-500 dark:border-red-500
  }
</style>
<!-- border text-sm rounded-lg block w-full p-2.5 -->