<template>
  <v-container fill-height grid-list-md text-xs-left >
    <v-layout row align-top justify-center>
      <v-flex xs6 sm6 class="pa-3">
        <v-card-title class="display-1">Skills</v-card-title>
        <v-card class="mb-3" dark v-for="(skill, index) in skills" :key="index" flat>
          <v-card-title class="headline">
            {{ skill.name }}
            <v-spacer></v-spacer>
            Proficiency: {{ skill.proficiency }}
          </v-card-title>
          <v-divider></v-divider>
          <v-card-text class="title">
            {{ skill.desc }}
          </v-card-text>
        </v-card>
      </v-flex>
      <v-flex xs6 sm6 class="pa-3">
        <v-card-title class="display-1">Experience</v-card-title>
        <v-card class="mb-3" dark v-for="(project, index) in projects" :key="index" flat >
          <v-card-title class="headline">
            {{ project.name }}
          </v-card-title>
          <v-divider></v-divider>
          <v-card-text class="title" v-html="project.desc">
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>

export default {
  name: 'Skills',
  data: () => ({
    skills: [
      {
        name: 'Java',
        desc: `As of right now I don't use Java a whole ton,
        but it was the language I started on.
        I have used a lot of the Java collections and other pieces the JDK provides.
        I have also used a lot of external libraries with Gradle.`,
        proficiency: 9
      },
      {
        name: 'Python',
        desc: `It seems required that everyone knows at
        least a little bit of python these days,
        so I have followed suit.
        I have an understanding of the general syntax and structure.
        However, I haven't used a lot of the packages that it can offer`,
        proficiency: 6
      },
      {
        name: 'Spring',
        desc: `I got curious about Spring when I saw it and had no idea what it did.
        I thought the concept of IoC was really cool so I pushed for Spring Boot in our Capstone Project.
        I have been able to work with it more and more throughout the project
        and I'm finding it very fun to work with. I also used Spring Cloud Gateway at peapod to create a
        flexible sidecar that offers the filters as middleware`,
        proficiency: 6
      },
      {
        name: 'Rust',
        desc: `Rust is my favorite language that I haven't had an opportunity to use.
        I took operating systems and then I heard about rust. I looked at it and the way that
        they handled data racing was insane to me. They found a simple solution to a
        complex problem. I have used it to mess around and make some command line tools on my homebrew tap.`,
        proficiency: 5
      },
      {
        name: 'Kotlin',
        desc: `Kotlin is the Java replacement I didnt know I needed. The Rest API for Headway
        is written in Kotlin and I find new cool tools in it every time I work with it.
        I also used it along with spring while at Peapod`,
        proficiency: 7
      },
      {
        name: 'Vue.js',
        desc: `Ever since I was introduced to Vue at Peapod I have loved it.
        It is my ideal front end because I don't have to do CSS when using Vuetify.
        This site was made with Vue/Vuetify!`,
        proficiency: 8
      },
      {
        name: 'Angular',
        desc: 'I tried out Angular as a Vue alternative over the summer. I really like the additional organization it offers.',
        proficiency: 5
      }
    ],
    projects: [
      {
        name: 'Peapod | Work Experience | June 2018 - Present',
        desc: `Peapod is a company located in downtown Chicago.
        I had the pleasure of having an internship program over the 2018 Summer.
        I started working on a Vue project initially,
        and then they offered me a remote position for while I was at school.
        I have worked on a number of different things including: Angular and Vue Integration,
        Cross platform webview App research, the peapod Vue component library, Creating a sidecar with
        Spring Cloud Gateway, researching Kubernetes and Docker, performance testing various applications with
        Gatling (Scala) and Vegeta (Go), and creating small front to back applications with Angular and Spring`
      },
      {
        name: 'Homebrew tools',
        desc: 'I have a homebrew tap where I make my own command line tools.' +
          '<ul>' +
          '<li><a href="https://github.com/mckernant1/project_manager">Git Repo Manager</a></li>' +
          '<li><a href="https://github.com/mckernant1/timeit">Command Line Timer</a></li>' +
          '<li><a href="https://github.com/mckernant1/hasher">File Hasher</a></li>' +
          '</ul>'
      },
      {
        name: 'Flyer Enterprises | Work Experience | November 2017 - August 2018',
        desc: `Flyer Enterprises (FE) is the student run business at our school.
        I applied and was accepted to a development position. I was assigned to App development
        and contracting on Shopify. I quit only after Peapod offered me the remote position`
      },
      {
        name: 'Headway | Capstone Project | January 2019 - Present',
        desc: `This is my Capstone Project. It is a site for interactive classroom use.
        Every account can be both an instructor and a student.
        I am working in a group with 3 of my friends,
        and we are collaborating through discord constantly to accomplish our weekly goals.
        Now Accessible at <a target="_blank" href="https://headway.dev">headway.dev</a>`
      },
      {
        name: 'My Bio Site | Personal Project | Updated often',
        desc: 'This Site! The repo can be seen <a target="_blank" href="https://bitbucket.org/mckernant1/me.simplycomplicated.dev/src/master/">here</a>'
      },
      {
        name: 'Code Snip',
        desc: 'This is where i keep all my code snippets that I use a ton. ' +
          'Can be seen  <a href="https://cs.simplycomplicated.dev/" target="_blank">Here</a>'
      }
    ]
  })
}
</script>

<style scoped>

</style>
