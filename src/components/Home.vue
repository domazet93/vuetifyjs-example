<template>
  <div class="home">
  <main>
  <v-sidebar id="sidebar" class="white" >
    <h2 >Users</h2>
    <p>{{credentials.name}} {{credentials.surname}}</p>
  </v-sidebar>
    <v-container class="text-xs-center">

            <v-row>
                <v-col xs12 sm8 offset-sm2 offset-md3 md6 offset-lg4 lg4>
                    <h4>Add user</h4>

                    <v-text-input
                    placeholder="Name"
                    label="NAME"
                    v-model="credentials.name">
                    </v-text-input>

                    <v-text-input
                    placeholder="Surname"
                    label="SURNAME"
                    v-model="credentials.surname">
                    </v-text-input>

                    <v-btn block class="primary" @click.native="submit()">ADD</v-btn>
                </v-col>
            </v-row>
        </v-container>
        </main>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
       credentials: {
            name: "",
            surname: ""
        },
        error: ""
    }
  },
  methods: {
    submit () {
        var credentials = {
            name: this.credentials.email,
            surname: this.credentials.password
        }
    }
  }
}
</script>

