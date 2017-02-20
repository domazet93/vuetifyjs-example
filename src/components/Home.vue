<template>
  <div class="home">
      <v-toolbar class="grey darken-4">
          <v-toolbar-title class="text-xs-center">VUETIFY EXAMPLE</v-toolbar-title>
      </v-toolbar>
      <v-carousel icon="remove">
        <v-carousel-item  v-for="pic in pics" :src="pic.url"/>
      </v-carousel>
      <v-container fluid="fluid">
        <v-row >
          <v-col xs8="xs8"  offset-xs2 class="mt-3 text-xs-center">
              <v-btn flat v-tooltip:bottom="{ html: 'view week' }">
                <v-icon x-large class="grey--text text--darken-2">view_week</v-icon>
              </v-btn>
              <v-btn flat v-tooltip:bottom="{ html: 'radio' }">
                <v-icon x-large class="grey--text text--darken-2">radio</v-icon>
              </v-btn>
              <v-btn flat v-tooltip:bottom="{ html: 'bluetooth' }">
                <v-icon x-large class="grey--text text--darken-2">bluetooth</v-icon>
              </v-btn>
              <v-btn flat v-tooltip:bottom="{ html: 'pause' }">
                <v-icon x-large class="grey--text text--darken-2">pause</v-icon>
              </v-btn>
              <v-btn flat v-tooltip:bottom="{ html: 'add to queue' }">
                <v-icon x-large class="grey--text text--darken-2">add_to_queue</v-icon>
              </v-btn>
          </v-col>
        </v-row>
        <v-row class="mt-5">
          <v-col xs8="xs8" offset-xs2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          </v-col>
        </v-row>
        <v-row class="mb-5">
          <v-col xs4="xs4" offset-xs2>
            <p>Lorem ipsum dolor sit amet?</p>
            <v-checkbox id="test7" name="test7" label="Testing 7"></v-checkbox>
            <v-checkbox id="test8" name="test8" label="Testing 8" filled></v-checkbox>
            <v-checkbox id="test9" name="test9" label="Testing 9" indeterminate></v-checkbox>
            <v-checkbox id="test10" name="test10" label="Testing 10" disabled></v-checkbox>
            <v-checkbox id="test10" name="test10" label="Testing 10" checked disabled></v-checkbox>
            <v-chip label class="pink white--text">
              <v-icon left>label</v-icon>Tags
            </v-chip>
            <v-chip label class="red white--text">
              <v-icon left>label</v-icon>Tags
            </v-chip>
            <v-chip label class="purple white--text">
              <v-icon left>label</v-icon>Tags
            </v-chip>
          </v-col>
          <v-col xs4="xs4">
            <v-list>
              <v-list-group v-for="item in items" v-bind:active="item.active">
                <v-list-tile slot="item">
                  <v-list-tile-action>
                    <v-icon>{{ item.action.icon }}</v-icon>
                  </v-list-tile-action>
                  <v-list-tile-content>
                    <v-list-tile-title>{{ item.title }}</v-list-tile-title>
                  </v-list-tile-content>
                  <v-list-tile-action>
                    <v-icon>keyboard_arrow_down</v-icon>
                  </v-list-tile-action>
                </v-list-tile>
                <v-list-item v-for="subItem in item.items">
                  <v-list-tile>
                    <v-list-tile-content>
                      <v-list-tile-title>{{ subItem.title }}</v-list-tile-title>
                    </v-list-tile-content>
                    <v-list-tile-action>
                      <v-icon>{{ subItem.action }}</v-icon>
                    </v-list-tile-action>
                  </v-list-tile>
                </v-list-item>
              </v-list-group>
            </v-list>
        </v-col>
      </v-row>
      <v-row class="deep-orange pb-5 text-xs-center"  >
        <v-col xs8="xs8" offset-xs2>
          <v-row class="mt-5 white--text">
            <v-col xs4="xs4">
              <v-icon class="display-3">touch_app</v-icon>
              <p>Lorem ipsum amet, consect iscing elit Lorem ipsum dolor sit amet, consectetur adipiscing elitr sit amet, consectetur</p>
            </v-col>
            <v-col xs4="xs4">
                <v-icon class="display-3">store</v-icon>
                <p>Lorem ipsum amet, consect iscing elit Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
            </v-col>
            <v-col xs4="xs4">
              <v-icon class="display-3">shopping_cart</v-icon>
              <p>Lorem ipsum amet, consect iscing elit Lorem ipsum dolor sit amet, consectetur adipiscing elitr sit amet, consectetur</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-footer class="grey darken-4">
        <v-row>
          <v-col xs8="xs8" offset-xs2>
            2017 - Check <a href="https://vuetifyjs.com" class="white--text">Vuetify</a>
          </v-col>
        </v-row>
      </v-footer>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      items: [
        {
          action: {
            icon: 'restaurant',
            class: 'grey--text'
          },
          title: 'Dining',
          items: [
            { title: 'Breakfast & brunch' },
            { title: 'New American' },
            { title: 'Sushi' }
          ]
        },
        {
          action: {
            icon: 'tv',
            class: 'grey--text'
          },
          title: 'TV',
          items: [
            { title: 'Comedy' },
            { title: 'Thriller' },
            { title: 'Action' }
          ]
        }
      ],
      pics: [
        {
         url: "http://www.ultrahdwallpapers.net/images/6.jpg"
        },
        {
         url: "http://68.media.tumblr.com/06af998502b6b706b416a4069d682675/tumblr_o8v43ornWa1u9sex8o1_1280.jpg"
        }
      ]
    }
  }
}
</script>

