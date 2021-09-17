<template>
  <v-container>
    <v-row>
      <v-col class="purple darken-2  text-center">
        <h1 class="white--text">Calculadora Básica</h1>
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col>
        <v-text-field
          type = "number"
          label="Número 1"
          :rules="rules"
          hide-details="auto"
          v-model="n1"
        ></v-text-field>
      </v-col>
      <v-col>
        <v-text-field
          type = "number"
          label="Número 2"
          :rules="rules"
          hide-details="auto"
          v-model="n2"
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-btn
          color="accent"
          elevation="5"
          rounded
          text
          @click="suma(n1,n2)"
        >Sumar</v-btn>
      </v-col>
      <v-col>
        <v-btn
          color="accent"
          elevation="5"
          rounded
          text
          @click="resta(n1,n2)"
        >Restar</v-btn>
      </v-col>
      <v-col>
        <v-btn
          color="accent"
          elevation="5"
          rounded
          text
          @click="multiplicacion(n1,n2)"
        >Multiplicar</v-btn>
      </v-col>
      <v-col>
        <v-btn
          color="accent"
          elevation="5"
          rounded
          text
          @click="division(n1,n2)"
        >Dividir</v-btn>
      </v-col>
    </v-row>
  <br />
    <v-row class="text-center">
      <v-col>
        <h3 class="pink darken-1--text">Resultado:</h3>
        <span class="red--text">{{ resultado }}</span>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
    name: "CalculadoraBasica",
    data:() =>{
        return {
            n1:null,n2:null, resultado:"",
            rules: [
                value => !!value || 'Requerido.',
                value => (value && value.length >= 2) || 'Mínimo 2 caracteres',
      ],
        };
    },
    methods: { 
        suma() {
            this.resultado = parseFloat(this.n1) + parseFloat(this.n2);
        },
        resta() {
            this.resultado = parseFloat(this.n1) - parseFloat(this.n2);
        },
        multiplicacion() {
            this.resultado = parseFloat(this.n1) * parseFloat(this.n2);
        },
        division() {
          if (this.n2 == 0){
            alert("No es un número");
          }else{
            this.resultado = parseFloat(this.n1) / parseFloat(this.n2);
          }   
        },
    },
}
</script>

<style>

</style>