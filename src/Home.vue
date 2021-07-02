<template>
  <div id="app">
    <v-container style="padding-top: 0;">
    <v-app-bar dark flat app>
      <v-avatar>
        <img
          src="og.png"
          alt="Daria Dankova"
        >
      </v-avatar>

      <div class="heading">
        <span>Daria Dankova</span>
        <span style="font-weight: 100;">Videographer</span>
      </div>


      <v-spacer></v-spacer>

      <v-btn-toggle
        v-model="tab"
        tile
        group
        v-show="!$vuetify.breakpoint.xs"
      >
        <v-btn value="videos">
          <v-icon left small>mdi-video</v-icon>
          <span class="ml-1">Videos</span>
        </v-btn>
        <v-btn value="photos">
          <v-icon left small>mdi-camera</v-icon>
          <span class="ml-1">Photos</span> 
        </v-btn>
        <v-btn value="pricing">
          <v-icon left small>mdi-cash</v-icon>
          <span class="ml-1">Pricing</span>
        </v-btn>
      </v-btn-toggle>

      <v-spacer></v-spacer>
      
      <div style="display: flex;" v-show="!$vuetify.breakpoint.xs">
        <v-btn href="https://www.instagram.com/dankovadash" target="_blank" icon>
          <v-icon>mdi-instagram</v-icon>
        </v-btn>
        <v-btn href="https://vimeo.com/user56218277" target="_blank" icon>
          <v-icon>mdi-vimeo</v-icon>
        </v-btn>
        <v-btn href="mailto:daria.dankova@gmail.com" target="_blank" icon>
          <v-icon>mdi-email-outline</v-icon>
        </v-btn>
      </div>

      <v-app-bar-nav-icon v-show="$vuetify.breakpoint.xs" @click="drawer = true"></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      dark
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    
    <v-tabs-items class="tabs" v-model="tab" style="margin-top: 75px;">
      <v-tab-item value="videos">
        <VideosTab />
      </v-tab-item>
    </v-tabs-items>
    </v-container>
  </div>
</template>

<script>
import VideosTab from './components/VideosTab.vue'

export default {
  name: 'Home',
  components: {
    VideosTab
  },
  data() {
    return {
      tab: 'videos',
      drawer: false
    }
  }
}
</script>

<style>
body {
  background: #2d2d2d;
  color: #eee;
  font-family: 'Roboto', sans-serif;
}

.tabs, .v-toolbar {
  background: #2d2d2d !important;
}

.heading {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 15px;
}
</style>
