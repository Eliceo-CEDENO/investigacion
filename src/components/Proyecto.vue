<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h2 ">
                   <h3 class="verde">Proyectos</h3>
                </v-subheader>
                <p class="text-h3">Aquí encontraras los proyectos de la ULEAM, de distintas facultades con su respectiva información.
                </p>
            </v-col>
            <v-col lg="12">
                <div class="text-center ">  
                    <v-chip @click="activeProyecto"  :color="activeProyecto === 'proyectoapp'? 'success':''" class="mx-5 text-h5">
                        Innovación
                    </v-chip>
                    <v-chip @click="activeProyecto"  :color="activeProyecto === 'proyectoapp'? 'success':''" class="mx-5 text-h5" >
                        Creación
                    </v-chip>
                    <v-chip @click="activeProyecto"  :color="activeProyecto === 'proyectoapp'? 'success':''" class="mx-5 text-h5">
                       Avances tecnológicos
                    </v-chip>
                    
                </div>

          

            </v-col>
            <slot v-if="activeProyecto === 'proyectoapp'">
                           <v-col lg="3">
                            <v-card
                       class="mx-auto"
                       max-width="400"
                       v-for="(proyecto, index) in proyectosList" :key="proyectoindex"
                   
                     >
                       <v-img
                         class="white--text align-end"
                         height="200px"
                         :src=proyecto.image
                       >

                       
                         <v-card-title>{{proyecto.title}}</v-card-title>
                       </v-img>
                   
                       <v-card-subtitle class="pb-0">
                         {{proyecto.facultad}}
                       </v-card-subtitle>
                   
                       <v-card-text class="text--primary">
                         <div> <strong>Líder:</strong>{{proyecto.lider}}</div>
                         <br>
                   
                         <div>{{proyecto.descripcion}}</div>
                       </v-card-text>
                   
                       <v-card-actions>
                         <v-btn
                           color="blue"
                           text
                         >
                           Seguir
                         </v-btn>
                   
                         <v-btn
                           color="success"
                           text
                         >
                           Leer
                         </v-btn>
                       </v-card-actions>
                     </v-card>
                   
                               </v-col>
            </slot>
        </v-row>
    </v-container>
</template>


<script>
    export default{
        name:"Proyecto",
        data(){
            return{
                activeProyecto:'proyectoapp',
                proyectosList:
            [
                {title:'Proyecto Informática', facultad:'Facultad Informática' , lider:'Dr. Jorge Herrera Tapia', descripcion:'Aplicaciones tecnológicas para personas con discapacidad.' , image:'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRnSHjFec9Q8GlzOf7vNi3PDSy-alq0engsml8BcIn7Dw&s'},   
                {title:'Proyecto Arquitectura',facultad:'Facultad arquitectura',lider:'Dr. Fernando Represa' ,descripcion:'Proyecto para la incidencia del rendimiento de la mano de obra y materiales en el costo de la construcción en Manta(Zona 4 de planificación).',image:'https://www.masqueteclas.com/wp-content/uploads/2019/04/cat-s61_8.jpeg'}   
            ],
         

            }
        }
    }
</script>

<style scoped>
.text-h4{
    color : green;
}

.verde{
  color: green;
}
</style>