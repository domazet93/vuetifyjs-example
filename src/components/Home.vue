<template>
  <div class="home">

    <header>
      <v-parallax :height="screenHeight" src="/static/img/header_img.png" 
      alt="parallax-img">
        <v-layout column align-center justify-center>
          <v-breadcrumbs class="pt-5 pb-5">
            <v-breadcrumbs-item
              v-for="page in pages" 
              :key="page.text" >
              <span class="white--text subheading">{{ page.text }}</span>            
            </v-breadcrumbs-item>
          </v-breadcrumbs>          
          <h1 class="white--text">Black Blob</h1>
          <h4 class="white--text">Perfect Web Agency</h4>
          <v-btn round color="light-blue lighten-4" 
          class="pl-5 pr-5" large outline dark>
            Learn more
          </v-btn>
        </v-layout>        
      </v-parallax>
    </header>>
    <section class="services">
      <v-container class="pt-5 pb-5">
        <v-layout row wrap>
          <v-flex md6>
            <img src="/static/img/office_worker.png" width="100%">
          </v-flex>
          <v-flex md6>
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
    </section>
    <footer>
       <v-container grid-list-md text-xs-center class="pt-5 pb-5">
          <v-layout row wrap>
            <v-flex xs12>
              <h4>Black Blob</h4>
            </v-flex>  
                <v-flex xs12><p>17th avenue / Zagreb 10000</p></v-flex>
                <v-flex xs12><p>info@blackblob.com</p></v-flex>
                <v-flex xs12><p>© 2017 Black Blob</p></v-flex>
             
          </v-layout>
        </v-container>
    </footer>
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
        ],
        pages: [
          { text: "Services"},
          { text: "Clients" },
          { text: "Blog"},
          { text: "Careers"}
        ]
      }
    },
  } 
</script>

<style type="text/css">

  .parallax__image {
    opacity: 1 !important;
  }
  footer {
    background-color: #0d1319;
    color: #fff;
  }

</style>