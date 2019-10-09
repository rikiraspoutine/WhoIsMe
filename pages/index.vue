<template>
  <div class="pa-12">
    <v-layout wrap id="main">
      <v-flex xs12 md7 class="mt-12 text-sm-center text-md-left">
        <h1>
          I'm Borni Ahmed Rami
        </h1>
        <br/>
        <p>
          Hello, I'm Borni Ahmed Rami, I'm 20 years old, <br/>
          Algerian . I'm Developer, Designer, Computer<br/> Science Student in Biskra Mohamed Khider <br/>Unversity .
          I've been developing and learning <br/>new technologies for 3 years to get ready for<br/> any project


        </p>
        <div class="text-sm-center justify-sm-center text-md-left">
          <v-btn rounded class="hidden-sm-and-down" color="success" href="#skills"> scroll down
            <v-icon>mdi-arrow-down</v-icon>
          </v-btn>
          <div style="height: 25px"></div>
        </div>

      </v-flex>
      <v-flex xs12 md5>
        <v-img src="/undraw_work_time_lhoj.svg"></v-img>
      </v-flex>
    </v-layout>

    <div style="height: 80px"></div>

    <div id="skills" class="text-center justify-center">
      <h1>
        Skills
      </h1>
      <br/>
      <v-layout wrap class="justify-center">
        <v-flex xs12 md6 lg3 v-for="skill in skills" class="pa-2">
          <v-card dark :color="skill.color" class="text-center justify-center">
            <v-card-title class="text-center justify-center">{{skill.name}}</v-card-title>
            <br/>
            <v-card-text class="justify-center text-center">
              <img height="150px" width="100%" :src="skill.icon"/>
              <div style="height: 10px"></div>
              <h2>Frameworks</h2>
              <br/>
              <v-layout wrap class="justify-center text-center">
                <v-flex xs12 md6 class="justify-center text-center" v-for="framework in skill.framworks">
                  <v-card color="transparent" flat class="pa-2" link role="link" :href="framework.link">

                    <v-card-title class="justify-center">
                      <v-avatar color="white">
                        <v-img :src="framework.icon"></v-img>
                      </v-avatar>
                    </v-card-title>
                    <v-card-text>
                      <h3>{{framework.name}}</h3>
                      <div style="height: 2px"></div>
                      <v-progress-linear
                        height="15"
                        :value="framework.percent"
                        striped
                      >
                        <br/>
                        <strong>{{ Math.ceil(framework.percent) }}%</strong>

                      </v-progress-linear>
                    </v-card-text>

                  </v-card>

                </v-flex>
              </v-layout>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </div>
    <div style="height: 150px"></div>

    <div id="languages" class="text-center justify-center">
      <h1>Programming Languages</h1>
      <v-layout class="justify-center text-center" wrap>
        <v-flex xs6 md4 lg3 xl2 v-for="lang in languages" class="pa-2 justify-center text-center">
          <br/>
          <v-card class="pa-12 justify-center text-center">
            <v-card-title class="justify-center text-center">
              <v-avatar color="white">
                <v-img :src="lang.icon"></v-img>

              </v-avatar>

            </v-card-title>
            <v-card-text>
              <h2>{{lang.language}}</h2>
              <br/>
              <v-progress-linear
                height="15"
                :value="lang.percent"
                striped
              >
                <br/>
                <strong>{{ Math.ceil(lang.percent) }}%</strong>

              </v-progress-linear>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </div>
    <div style="height: 150px"></div>
    <div id="projects" class="text-center justify-center">
      <h1>Projects</h1>        <br/>

      <v-layout wrap class="justify-center text-center">
        <v-card flat color="transparent" class="pa-12">
          <v-card-text class="text-center justify-center">
            <img height="250px" width="100%" src="undraw_under_construction_46pa.svg"/>
            <div style="height: 50px"></div>
            <h1>
              Coming soon ..
            </h1>

          </v-card-text>
        </v-card>
      </v-layout>

    </div>
    <div style="height: 150px"></div>

    <div id="contact me"  class="text-center justify-center">
      <v-card dark color="#303F9F" class="pa-12">

        <v-card-text>
          <v-layout wrap class="text-left ">
            <v-flex xs12 md8>
              <br/>
              <h1>Contact me</h1>
              <br/>
              <p class="">
                If you wanna more information, hire me, do a project for you? <br>
                Contact me with
              </p>
              <v-btn fab  color="white" href="https://www.facebook.com/riki.ramy99"> <v-icon class="blue--text text--darken-3">mdi-facebook</v-icon></v-btn>
              <v-btn fab  color="white" href="https://twitter.com/RRaspoutine"> <v-icon class="blue--text">mdi-twitter</v-icon></v-btn>
              <v-btn fab  color="white" href="https://www.instagram.com/riki_raspoutine/"> <v-icon class="pink--text">mdi-instagram</v-icon></v-btn>
              <v-btn fab  color="white" href="mailto:rikiraspoutine@gmail.com"> <v-icon class="grey--text text--darken-2">mdi-email</v-icon></v-btn>
            </v-flex>
            <v-flex xs12 md4>
              <v-img src="/undraw_contact_us_15o2 (1).svg"></v-img>
            </v-flex>

          </v-layout>


        </v-card-text>
        <v-card-actions class="justify-center text-center">
        </v-card-actions>
      </v-card>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'index',
    data: function() {
      return {
        languages: [
          {
            language: 'Java',
            icon: 'https://www.stickpng.com/assets/images/58480979cef1014c0b5e4901.png',
            percent: 88
          },
          {
            language: 'C#',
            icon: 'https://www.vippng.com/png/detail/398-3984434_c-language-circle.png',
            percent: 86
          },
          {
            language: 'Dart',
            icon: 'data:image/png;base64,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',
            percent: 85
          },
          {
            language: 'Javascript',
            icon: 'https://cdn.freebiesupply.com/logos/large/2x/javascript-logo-png-transparent.png',
            percent: 83
          },
          {
            language: 'Kotlin',
            icon: 'https://kotlinexpertise.com/wp-content/uploads/2018/04/pCfEzr6L_400x400.png',
            percent: 73
          },
          {
            language: 'C/C++',
            icon: 'https://raw.githubusercontent.com/isocpp/logos/master/cpp_logo.png',
            percent: 67
          },
          {
            language: 'Php',
            icon: 'http://pngimg.com/uploads/php/php_PNG26.png',
            percent: 53
          }


        ],
        skills: [
          {
            color: '#303F9F',
            name: 'Front-End Developement',
            icon: '/undraw_static_assets_rpm6.svg',
            framworks: [
              {
                name: 'VueJs',
                icon: 'https://cdn2.auth0.com/blog/vuejs/logo.png',
                link: 'https://vuejs.org/',
                percent: 95
              }, {
                name: 'NuxtJS',
                icon: 'https://nuxtjs.org/logos/nuxt-emoji.png',
                link: 'https://nuxtjs.org',
                percent: 86
              }, {
                name: 'Vuetify',
                icon: 'https://styles.redditmedia.com/t5_3nu8v/styles/communityIcon_zuqnf4r5ml111.png',
                link: 'https://vuetifyjs.com',
                percent: 97
              }
            ]
          },
          {
            color: '#78909C',
            name: 'Back-End Developement',
            icon: '/Web_hosting_SVG.svg',
            framworks: [{
              name: 'Asp.net Core',
              icon: 'https://dwz6w0xm5nwrx.cloudfront.net/akl/staticfiles/icons/aspcore.png',
              link: 'https://docs.microsoft.com/en-us/aspnet/core/?view=aspnetcore-3.0',
              percent: 84
            }]
          },
          {
            color: '#00838F',
            name: 'Mobile Developement',
            icon: '/undraw_mobile_prototyping_grmd.svg',
            framworks: [{
              name: 'Android Framework',
              icon: 'https://whatsnew2day.com/wp-content/uploads/2019/08/1566479220_Google-deserts-desserts-Android-10-is-the-official-name-for.png',
              link: 'https://developer.android.com/',
              percent: 76
            }, {
              name: 'Flutter Framework',
              icon: 'https://miro.medium.com/max/1000/1*ilC2Aqp5sZd1wi0CopD1Hw.png',
              link: 'https://flutter.dev/',
              percent: 82
            }]
          },
          {
            color: '#A1887F',
            name: 'Desktop Developement',
            icon: '/undraw_programmer_imem.svg',
            framworks: [{
              name: '.Net Framework',
              icon: 'https://upload.wikimedia.org/wikipedia/commons/0/0e/Microsoft_.NET_logo.png',
              link: 'https://dotnet.microsoft.com/',
              percent: 76
            }]
          }
        ]
      }
    }
  }
</script>

<style>
  * {
    font-family: "Roboto", sans-serif;
  }
</style>
