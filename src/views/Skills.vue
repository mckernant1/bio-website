<template>
  <v-container class="fill-height grid-list-md text-xs-left">
    <v-layout class="row align-top justify-center">
      <v-container>
        <v-card-title class="display-1">Experience</v-card-title>
        <v-card class="mb-3" dark v-for="(experience, index) in experiences" :key="index" flat>
          <v-card-title class="headline">
            {{ experience.name }}
            <v-spacer/>
            {{ experience.dateRange }}
          </v-card-title>
          <v-divider></v-divider>
          <v-card-text>
            <h3>Technologies Used</h3>
            <ul class="pl-5">
              <li v-for="(tech, index) in experience.technologies" :key="index">{{ tech }}</li>
            </ul>
            <br/>
            <h3>Description</h3>
            <br/>
            <p class="pl-3 pr-3 ">{{ experience.desc }}</p>
          </v-card-text>
        </v-card>
      </v-container>
    </v-layout>
  </v-container>
</template>

<script>

export default {
  name: 'Skills',
  data: () => ({
    experiences: [
      {
        name: 'Senior Software Engineer at SS&C Advent',
        dateRange: 'August 2023 - Present',
        technologies: [
          'Python',
          'Java',
          'Jenkins',
          'Github Actions'
        ],
        desc: `Working on Genevaweb on DevOps and install scripts. Assisting in complex customer issues. Assisting in design and implementation of genevaweb services.`
      },
      {
        name: 'SDE II at Amazon Web Services',
        dateRange: 'March 2022 - July 2023',
        technologies: [
          'Rust',
          'Java',
          'Aws Cdk'
        ],
        desc: `A Slightly larger role where I started to mentor other people who have joined the org.
        More design reviews and looking over other peoples work. As well as building out new canaries with Aws CDK.`
      },
      {
        name: 'SDE I at Amazon Web Services',
        dateRange: 'February 2020 - March 2022',
        technologies: [
          'Java',
          'Python',
          'Apache Spark'
        ],
        desc: `I am an SDE at AWS currently working on DynamoDB. Lots of working on distributed systems.
        Lots of complicated design docs and review processes to make sure the cloud is safe.`
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
        desc: `I work on a lot of personal projects from discord bots to websites.
        Check out my Github in the top right!
        This site was created with Vue.js and deployed with AWS Amplify`
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
      },
      {
        name: 'Assistant Database Administrator at Northwestern University',
        dateRange: 'June 2016 - February 2020',
        technologies: [
          'Excel',
          'Python',
          'AutoCAD'
        ],
        desc: `My High School job. Did a lot of data entry, used python to help!`
      }
    ]
  })
}
</script>

<style scoped>

</style>
