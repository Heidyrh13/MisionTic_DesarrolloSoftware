<template>
  <v-container>
    <v-row>
      <v-col>
        <calculadora-basica/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// @ is an alias to /src
import CalculadoraBasica from '../components/CalculadoraBasica.vue'

export default {
  name: 'Home',
  components: {
    CalculadoraBasica
  },
  methods: {
  
  }

}
</script>
