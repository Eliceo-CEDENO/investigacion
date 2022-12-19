<template>
    <v-container>
        <v-row>
            <v-col lg="7">
                <v-img
                :src="require('../assets/about2.png')"
                class="my-3"
                contain
                width="100%"
               
              />
                
            </v-col>
            <v-col>
                <v-spacer/>
                <v-subheader class="text-h3">
                       Sobre nosotros
                </v-subheader>

                <p class="text-h5">La UNIVERSIDAD LAICA ELOY ALFARO DE MANABÍ busca apoyar en proyectos hacia la comunidad con el motivo de fomentar el desarrollo y la investigación.
                 Nuestros indicadores para el Plan Estratégic de Investigación:
                </p>

                <v-list>
                    <v-list-item>
                        <v-list-item-subtitle>
                            <li>Número de programas por carreras-facultad por dominios académicos de la ULEAM aplicados en los campos o áreas del conocimiento con aporte al desarrollo de la zona 4. </li>
                        </v-list-item-subtitle>
                        <v-list-item-subtitle>
                            <li>Número de proyectos de investigación aprobados.</li>
                        </v-list-item-subtitle>
                        <v-list-item-subtitle>
                            <li>Número de grupos de investigación por programas y proyectos, conformados por profesores y estudiantes.</li>
                        </v-list-item-subtitle>
                    </v-list-item>
                </v-list>
                 
            </v-col>
        </v-row>
    </v-container>
</template>


<script>
    export default{
        name:'About'
    }

</script>


<style scoped>
  
</style>