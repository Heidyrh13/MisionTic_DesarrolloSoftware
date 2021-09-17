<template>
  <v-container>
    <h1>This is an about page</h1>
    <v-row>
      <v-col>
        <v-btn
          color ="primary"
          elevation ="2"
          @click="paso2()"
          >Home</v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card
      class="mx-auto"
      max-width="344">
      <v-img
        src="https://es.investinbogota.org/sites/default/files/node/news/field_news_imagen/Emprendimientos%20en%20Bogota%CC%81.jpg"
        height="200px"
      ></v-img>

      <v-card-title>
        Bogotá  
      </v-card-title>

      <v-card-subtitle>
        2600 metros más cerca de las estrellas
      </v-card-subtitle>

      <v-card-actions>
        <v-btn
          color="orange lighten-2"
          text
        >
          Explore
        </v-btn>

        <v-spacer></v-spacer>

        <v-btn
          icon
          @click="show = !show"
        >
          <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>

          <v-card-text>
            I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card>
  </v-col>
  <v-col>
        <v-card
      class="mx-auto"
      max-width="344">
      <v-img
        src="https://www.semana.com/resizer/2noyXlnQe0xA-d-VdDa6-acgYhk=/1200x675/filters:format(jpg):quality(50)//cloudfront-us-east-1.images.arcpublishing.com/semana/KI2722K53VBFVN7BR7OMCXSPWM.jpg"
        height="200px"
      ></v-img>

      <v-card-title>
        Medellín 
      </v-card-title>

      <v-card-subtitle>
        La ciudad de la eterna primavera
      </v-card-subtitle>

      <v-card-actions>
        <v-btn
          color="orange lighten-2"
          text
        >
          Explore
        </v-btn>

        <v-spacer></v-spacer>

        <v-btn
          icon
          @click="show = !show"
        >
          <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>

          <v-card-text>
            I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card>
  </v-col>
  </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
      show: false,
    }),
  methods: {
    paso2() {
      console.log("Ir al Home...")
      this.$router.push("/");
    }
  }
}
</script>
