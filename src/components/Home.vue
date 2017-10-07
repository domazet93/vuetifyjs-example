<template>
  <div class="home">
    <v-parallax src="/static/img/header_img.jpeg"     
    jumbotron :height="screenHeight">
      <v-layout column align-center justify-center>
        <h1 class="white--text">Black Blob</h1>
        <h4 class="white--text">Perfect Web Agency</h4>
        <v-btn round color="light-blue lighten-4" 
        class="pl-4 pr-4" large outline dark>
          Learn more
        </v-btn>
      </v-layout>        
    </v-parallax>
    <v-container class="pt-5 pb-5">
      <v-layout row wrap>
        <v-flex xs6>
          <img src="/static/img/office_worker.png" width="500">
        </v-flex>
        <v-flex xs6>
          <v-flex xs12>
          <h4 class="grey--text text--darken-2">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
            tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
            quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
            consequat.
          </h4>
          </v-flex>
          <v-layout class="mt-5">
            <v-flex xs4 class="pr-2" v-for="service in services">
              <v-card :class="service.color" class="white--text" >
                <v-card-title primary-title>
                  <div class="headline">{{ service.name }}</div>
                  <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</div>
                </v-card-title>
                <v-card-actions>
                  <v-btn flat>Check now</v-btn>
                </v-card-actions>
              </v-card>
            </v-flex>            
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
  export default {
    name: 'home',
    data () {
      return {
        screenHeight: window.innerHeight,
        services: [
          {
            name: "Branding",
            color: "blue-grey",
          },
          {
            name: "Design",
            color: "purple"
          },
          {
            name: "Stragegy",
            color: "cyan"
          }
        ]
      }
    },
  } 
</script>

