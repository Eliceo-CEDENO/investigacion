<template>
    <v-container class="pt-15">
        <v-row>
            <v-col lg="6">
                <h2 class="title-main">Conoce los avances investigativos con un solo click</h2>
                <p class="description"> <strong>Contacto:</strong>05-287-4171</p>
             

                 <router-link class="p" to="/proyecto">  <p class="p">
                    <v-btn color="green darken-3" class="white--text mr-10" rounded>
                        <v-icon>mdi-eye</v-icon>  Dar un vistazo
                      </v-btn>

                 </p></router-link>  
            </v-col>
            <v-col lg="6">
                <v-img
                :src="require('../assets/persona_investigadora.jpg')"
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

    .p{
  text-decoration: none; 
  color: inherit;
  padding: 2%;
 }
</style>