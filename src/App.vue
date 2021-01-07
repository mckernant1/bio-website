<template>
  <v-app class="grey lighten-2">
    <v-toolbar dark tabs>
        <v-toolbar-title class="pr-3">Tom McKernan</v-toolbar-title>
      <v-flex>
        <v-tabs
          centered
          v-model="currentItem"
          color="transparent"
          slider-color="white"
          icons-and-text
        >
          <v-tab href="#home">
            Home
          </v-tab>
          <v-tab href="#skills">
            Skills & Experience
          </v-tab>
        </v-tabs>
      </v-flex>

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
    <v-tabs-items v-model="currentItem">
      <v-tab-item :value="'home'">
        <Home></Home>
      </v-tab-item>
      <v-tab-item :value="'skills'">
        <Skills></Skills>
      </v-tab-item>
    </v-tabs-items>
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
