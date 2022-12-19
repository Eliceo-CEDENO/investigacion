<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">
                   <h3 class="verde">Iniciar Sesión</h3> 
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
               v-model="password"
            :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
            :rules="[rules.required, rules.min]"
            :type="show1 ? 'text' : 'password'"
            name="input-10-1"
            label="Contraseña"
            hint="Debe contener mínimo 8 caracteres"
            counter
            @click:append="show1 = !show1"
          ></v-text-field>



             <router-link class="p" to="/"> <p class="p">

                   <v-btn
                   :disabled="!valid"
                   color="success"
                   class="mr-4"
                   required
                
                 >
                  Iniciar sesión
                 </v-btn>
             

             </p></router-link>  
             <router-link class="p" to="/registrarse"> <p class="p">

                   <v-btn
                   :disabled="!valid"
                   color="blue"
                   class="mr-4"
                   required
                
                 >
                  Crear cuenta
                 </v-btn>
             

             </p></router-link>  

 
    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Olvide mi contraseña
    </v-btn>

  </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>


<script>
    export default{
        name:"Login",
        data: () => ({
            show1: false,
            show2: true,
            show3: false,
            show4: false,
            password: '',
            rules: {
              required: value => !!value || 'Contraseña requerida.',
              min: v => v.length >= 8 || 'Min 8 characters',
              emailMatch: () => (`The email and password you entered don't match`),
            },
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

  .p{
  text-decoration: none; 
  color: inherit;
  padding: 2%;
 }

 .verde{
  color:green
 }
</style>