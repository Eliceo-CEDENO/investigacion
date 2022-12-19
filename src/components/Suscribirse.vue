<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">
                   <h3 class="verde">Suscribirse</h3> 
                </v-subheader>

        
        

            </v-col>
            <v-col class="center" lg="6">
            <h1>Más detalles</h1>
            <ul>
              <li>
                Al suscribirse recibiras las últimas novedades
              </li>
              <li>
             Podras participar en proyectos
              </li>
              <li>
              Aprenderás como postular para gestionar proyectos
              </li>
            </ul>

                     
            </v-col>
     
            <v-col lg="6">
         <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-text-field
      v-model="name"
      :counter="10"
      :rules="nameRules"
      label="Usuario"
      required
    ></v-text-field>

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="Correo electrónico"
      required
    ></v-text-field>

    <v-select
      v-model="select"
      :items="items"
      :rules="[v => !!v || 'Sexo es requerido']"
      label="Sexo"
      required
    ></v-select>

    <v-checkbox
      v-model="checkbox"
      :rules="[v => !!v || 'Debes aceptar los términos para continuar!']"
      label="Aceptas los términos?"
      required
    ></v-checkbox>

    <v-btn
      :disabled="!valid"
      color="success"
      class="mr-4"
      @click="validate"
    >
      Validar
    </v-btn>

    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Resetear form
    </v-btn>

    <v-btn
      color="warning"
      @click="resetValidation"
    >
      Resetear Validaciones
    </v-btn>
  </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>


<script>
    export default{
        name:"Contacto",
        data: () => ({
            valid: true,
            name: '',
            nameRules: [
              v => !!v || 'Nombre es requerido',
              v => (v && v.length <= 10) || 'Nombre no debe pasar de los 10 caracteres',
            ],
            email: '',
            emailRules: [
              v => !!v || 'Correo es requerido',
              v => /.+@.+\..+/.test(v) || 'Correo debe ser válido',
            ],
            select: null,
            items: [
              'Hombre',
              'Mujer',
             
            ],
            checkbox: false,
          }),
      
          methods: {
            validate () {
              this.$refs.form.validate()
            },
            reset () {
              this.$refs.form.reset()
            },
            resetValidation () {
              this.$refs.form.resetValidation()
            },
          },
        }
      </script>

<style scoped>
  .center{


    padding-left: 150px;
    color: rgb(7, 159, 22);

  }

  .verde{
    color:green;
  }
</style>