<template>
  <div class="home">
    <v-app top-navbar footer right-fixed-sidebar>
      <main>
        <v-sidebar id="sidebar" fixed right>
           <img src="../assets/vuetify.png" class="mb-5">
        </v-sidebar>
        <v-content>
          <v-container>
            <h2>Content</h2>
          </v-container>
        </v-content>
      </main>
    </v-app>
  </div>
</template>

<script>
export default {
  name: 'home'
}
</script>

