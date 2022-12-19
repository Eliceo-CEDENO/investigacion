<template>
        <v-app-bar
      style="padding: 0px 100px"
      app
      color="white"
      light
      elevation="6"
      elevate-on-scroll
    >
     <v-toolbar-title class="v-toolbar-title">U_Proyecto</v-toolbar-title>
          <v-spacer />
            <router-link class="p" to="/"> <p class="p">Inicio</p></router-link>  
                <router-link class="p"  to="/proyecto">Proyecto</router-link>
                <router-link class="p"  to="/suscribirse">Suscribirse</router-link>
                <router-link class="p"  to="/contacto">Contactos</router-link>
                <router-link class="p"  to="/misproyectos">Mis proyectos</router-link>
                <router-link class="p"  to="/login">     <v-btn  outlined color="success"> Iniciar sesión  </v-btn></router-link>
           
              
    </v-app-bar>
  

</template>
  
  <script>
  

  export default {
    name: "Header",
    data(){
      return {
        menus:[
          {title:'Home', route:'/proyecto'},
          {title:'Proyectos', route:'proyectos'},
          {title:'Suscribirse', route:'suscribirse'},
          {title:'Contactos', route:'contactos'},

  
        ]
      }
    }
  };
  </script>
  
<style scoped>
 .v-toolbar-title{
  font-size:32px;
  color:#4caf50;
  font-weight: 700;
  font-family: cursive;

 }

 .p{
  text-decoration: none; 
  color: inherit;
  padding: 2%;
 }
</style>