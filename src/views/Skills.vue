<template>
  <v-container fill-height grid-list-md text-xs-left>
    <v-layout row align-top justify-center>
      <v-flex xs12 sm12 class="pa-3">
        <v-card-title class="display-1">Experience</v-card-title>
        <v-card class="mb-3" dark v-for="(experience, index) in experiences" :key="index" flat>
          <v-card-title class="headline">
            {{ experience.name }}
            <v-spacer/>
            {{experience.dateRange}}
          </v-card-title>
          <v-divider></v-divider>
          <v-card-text class="title">
            <h3>Technologies Used</h3>
            <ul>
              <li v-for="(tech, index) in experience.technologies" :key="index">{{tech}}</li>
            </ul>
            <br/>
            <h3>Description</h3>
            <br/>
            <p>{{experience.desc}}</p>
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
    experiences: [
      {
        name: 'SDE I at Amazon Web Services',
        dateRange: 'February 2020 - Present',
        technologies: [
          'Java',
          'Python',
          'Apache Spark'
        ],
        desc: `I am an SDE at AWS currently working on DynamoDB`
      },
      {
        name: 'Personal Projects',
        dateRange: 'Always :]',
        technologies: [
          'Kotlin',
          'Rust',
          'AWS (ECS, Amplify, CodePipeline, and a mix of others)',
          'Homebrew',
          'Angular'
        ],
        desc: `I work on a lot of personal projects from discord bots to websites`
      },
      {
        name: 'SDE Intern at Peapod',
        dateRange: 'June 2018 - August 2019',
        technologies: [
          'Kotlin',
          'Rust',
          'Vue.js',
          'Spring Framework'
        ],
        desc: `I worked at Peapod with the Platform team to improve some internal tools`
      }
    ]
  })
}
</script>

<style scoped>

</style>
