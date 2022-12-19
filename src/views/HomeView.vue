<template>
  <PrincipalHeader />
  <About />
 

</template>

<script>
import { defineComponent } from 'vue';

// Components


import PrincipalHeader from '../components/PrincipalHeader.vue';
import About from '../components/About.vue';

export default defineComponent({
  name: 'HomeView',

  components: {

    PrincipalHeader,
    About,
  },
});
</script>
