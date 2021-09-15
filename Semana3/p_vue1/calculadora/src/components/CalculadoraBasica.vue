<template>
  <div>
  <h1>Calculadora Básica</h1>

  <v-text-field
      type = "number"
      label="Número 1"
      :rules="rules"
      hide-details="auto"
      v-model="n1"
    ></v-text-field>

  <v-text-field
      type = "number"
      label="Número 2"
      :rules="rules"
      hide-details="auto"
      v-model="n2"
    ></v-text-field>

  <v-btn
    color="accent"
    elevation="5"
    rounded
    text
    @click="suma(n1,n2)"
  >Sumar</v-btn>

  <v-btn
    color="accent"
    elevation="5"
    rounded
    text
    @click="resta(n1,n2)"
  >Restar</v-btn>
  <br />
  <span>{{ resultado }}</span>
  </div>
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
        suma(n1,n2) {
            this.resultado = parseFloat(this.n1) + parseFloat(this.n2);
        },
        resta(n1,n2) {
            this.resultado = parseFloat(this.n1) - parseFloat(this.n2);
        },
    },
}
</script>

<style>

</style>