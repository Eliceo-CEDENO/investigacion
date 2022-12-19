<template>
    <Contacto />
    <About />
   
  
  </template>
  
  <script>
  import { defineComponent } from 'vue';
  
  // Components
  
  
import Contacto from '../components/Contacto.vue';

  
  export default defineComponent({
    name: 'HomeView',
  
    components: {
        Contacto,
 
    },
  });
  </script>
  