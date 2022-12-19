<template>
    <Contacto />

  </template>
  
  <script>
  import { defineComponent } from 'vue';
  
  // Components
  
import Contacto from '../components/Suscribirse.vue';
export default defineComponent({
    name: 'ContactoView',
  
    components: {
        Contacto
    },
  });
  </script>
  