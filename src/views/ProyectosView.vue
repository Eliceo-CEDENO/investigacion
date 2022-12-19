<template>
    <Proyecto />

  </template>
  
  <script>
  import { defineComponent } from 'vue';
  
  // Components
  
import Proyecto from '../components/Proyecto.vue';
export default defineComponent({
    name: 'ProyectoView',
  
    components: {
        Proyecto
    },
  });
  </script>
  