<template>
      <v-app>
        <nav>
          <v-toolbar flat color="transparent">
            <v-toolbar-title>
              Who is me?
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-items class="text-right">
              <v-btn icon @click="ThemeChange()">
                <v-icon>mdi-theme-light-dark</v-icon>
              </v-btn>
            </v-toolbar-items>
          </v-toolbar>
        </nav>
        <nuxt/>
        <footer>
          <v-footer class="pa-12">
            <v-layout wrap>
                <v-flex xs4>
                  <a href="https://nuxtjs.org/">
                    <img width="280"  src="https://nuxtjs.org/logos/built-with-nuxt.svg"/>

                  </a>
                </v-flex>
                <v-flex xs8 class="justify-end text-right">
                  <a href="https://github.com/rikiraspoutine/WhoIsMe">
                    <img height="40" :src="(this.$vuetify.theme.dark) ? 'https://joshuapenalba.files.wordpress.com/2014/12/github-icon.png':'https://github.githubassets.com/images/modules/logos_page/GitHub-Logo.png'" />

                  </a>
                </v-flex>

            </v-layout>


          </v-footer>
        </footer>
      </v-app>
</template>

<script>
  export default {
    name: 'default',
    methods:{
      ThemeChange:function() {
        this.$vuetify.theme.dark=!this.$vuetify.theme.dark;
      }
    }
  }
</script>

<style scoped>

</style>
