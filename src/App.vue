<template>
  <v-app id="inspire">
    <v-navigation-drawer fixed v-model="drawer" app>
      <v-list dense>
        <router-link v-bind:to="{name: 'Home'}" class="side_bar_link">
          <v-list-tile>
            <v-list-tile-action>
              <v-icon>home</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>Home</v-list-tile-content>
          </v-list-tile>
        </router-link>

        <router-link v-bind:to="{name: 'Contact'}" class="side_bar_link">
          <v-list-tile>
            <v-list-tile-action>
              <v-icon>contact_mail</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>Contact</v-list-tile-content>
          </v-list-tile>
        </router-link>
      </v-list>
    </v-navigation-drawer>

    <v-toolbar color="indigor" dark fixed app>
      <v-toolbar-side-icon @click.stop="drawer != drawer">
      </v-toolbar-side-icon>
      <v-toolbar-title>Home</v-toolbar-title>
    </v-toolbar>

    <v-content>
      <v-container-fliud>
        <div id="app">
          <router-view/>
        </div>
      </v-container-fliud>
    </v-content>
  </v-app>
</template>

<script>
import './assets/stylesheets/main.css';

export default {
  data: () => ({
    drawer: null,
  }),
  props: {
    source: String,
  },
};
</script>
