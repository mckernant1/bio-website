<template>
  <v-app>
    <v-card class="bg-blue-grey-darken-1">
      <v-toolbar class="bg-grey-darken-3">
        <v-toolbar-title>Tom McKernan</v-toolbar-title>

          <v-spacer/>

          <v-tabs class="bg-grey-darken-3">
            <v-tabs
              v-model="currentItem"
            >
              <v-tab value="home">
                Home
              </v-tab>
              <v-tab value="skills">
                Skills & Experience
              </v-tab>
            </v-tabs>
          </v-tabs>
          <v-spacer/>

        <v-toolbar-items>
          <v-btn @click="openGithub" flat>
            <i class="fab fa-github fa-2x"></i>
          </v-btn>
          <v-btn @click="openLinkedIn" flat>
            <i class="fab fa-linkedin fa-2x"></i>
          </v-btn>
          <v-btn @click="downloadPDF" flat>
            <i class="fas fa-file-alt fa-2x"></i>
          </v-btn>
          <v-btn @click="sendEmail" flat>
            <i class="fas fa-envelope-square fa-2x"></i>
          </v-btn>
        </v-toolbar-items>

      </v-toolbar>

      <v-window v-model="currentItem">
        <v-window-item :value="'home'">
          <Home></Home>
        </v-window-item>
        <v-window-item :value="'skills'">
          <Skills></Skills>
        </v-window-item>
      </v-window>
    </v-card>
  </v-app>
</template>

<script>
// import Header from './components/Header'
import Home from './views/Home'
import Skills from './views/Skills'

export default {
  name: 'App',
  components: {
    // Header,
    Skills,
    Home
  },
  data: () => ({
    currentItem: 'home'
  }),
  methods: {
    downloadPDF() {
      window.open('./Tom-McKernan-Resume-Web.pdf', '_blank')
    },
    openLinkedIn() {
      window.open('https://www.linkedin.com/in/thomas-mckernan/', '_blank')
    },
    openGithub() {
      window.open('https://github.com/mckernant1', '_blank')
    },
    sendEmail() {
      window.open('mailto:tmckernan36@gmail.com', '_blank')
    }
  }
}
</script>
