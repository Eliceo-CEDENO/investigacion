<template>
    <v-container class="pt-15">
        <v-row>
            <v-col lg="6">
                <h2 class="title-main">Contacto</h2>
            <p class="description"> <strong>Correo:</strong>proyectos_uleam@uleam.edu.ec</p>
            <p class="description"> <strong>Teléfono:</strong>05-287-4171</p>
            <p class="description"> <strong>Dirreción:</strong>Av. Circunvalación - Vía a San Mateo Manta-Manabí-Ecuador</p>
               
            
            </v-col>
        
            <v-col lg="6">
                <v-img
                :src="require('../assets/contacto.png')"
                class="my-3"
                contain
                width="100%"
               
              />
            </v-col>
        </v-row>

    </v-container>


</template>

<script>
     
  export default {
    name: "PrincipalHeader",
  };    


</script>

<style scoped>
    h2.title-main {
        font-size: 60px;
        font-weight:bold;
        font-family: cursive;
        color:rgb(24, 219, 54);
    }
    p.description {
        font-size: 30px;
        font-family: cursive;
        margin:32px 0px;
        color:#000000;
    }

    .white--text{
        font-size: 20px;
    }
</style>