<template>
    <Registrarse />

   
  
  </template>
  
  <script>
  import { defineComponent } from 'vue';
  
  // Components
  
  
import Registrarse from '../components/Registrarse.vue';

  
  export default defineComponent({
    name: 'RegistrarseView',
  
    components: {
        Registrarse,

    },
  });
  </script>
  