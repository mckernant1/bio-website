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
              <li v-for="(tech, tIndex) in experience.technologies" :key="tIndex">{{ tech }}</li>
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
  name: 'Experience',
  data: () => ({
    experiences: [
      {
        name: 'Senior Software Engineer at SS&C Advent',
        dateRange: 'Aug 2023 - Present',
        technologies: [
          'Python',
          'Java',
          'TypeScript',
          'Kubernetes',
          'Helm',
          'Terraform',
          'GitHub Actions',
          'CI/CD'
        ],
        desc: `Migrated CI systems from Jenkins to cloud-native pipelines with GitHub Actions and built TypeScript automation.
Managed Kubernetes deployments and maintained infrastructure-as-code workflows with Terraform and CloudFormation.
Maintained development environments with monitoring and alerting.
Mentored engineers on CI/CD practices and infrastructure.
Collaborated with customer support and account teams to troubleshoot and resolve client issues, ensuring high reliability.`
      },
      {
        name: 'Software Engineer II at Amazon Web Services',
        dateRange: 'Mar 2022 - Jul 2023',
        technologies: [
          'Java',
          'Python',
          'Rust',
          'AWS (S3, DynamoDB, EKS, ECR, SQS)',
          'GitHub Actions',
          'Jenkins',
          'CI/CD',
          'Terraform',
          'Distributed Systems'
        ],
        desc: `Optimized AWS S3 usage reducing monthly storage costs by 60%.
Designed high-performance Java data structures to improve CPU efficiency.
Implemented TTL system with distributed locking for database partitions.
Developed internal tooling in Python and Java for logs and metrics.
Automated global parity and scalability with CI/CD pipelines.
Served as on-call engineer, responding to production incidents and ensuring system reliability.
Mentored engineers and performed design reviews for new systems.`
      },
      {
        name: 'Software Engineer I at Amazon Web Services',
        dateRange: 'Feb 2020 - Mar 2022',
        technologies: [
          'Java',
          'Python',
          'CloudFormation',
          'DynamoDB',
          'CloudWatch',
          'Distributed Systems'
        ],
        desc: `Upgraded Python systems from 2.7 to 3.x to avoid EOL and security issues.
Built CloudWatch Contributor Insights dashboards for DynamoDB using CloudFormation.
Investigated and resolved DynamoDB throttling incidents.
Automated ticket data enrichment with custom tooling.
Served as on-call engineer for production systems.`
      },
      {
        name: 'Software Engineer Intern - Back End Team at Peapod Digital Labs',
        dateRange: 'May 2019 - Aug 2019',
        technologies: [
          'Kotlin',
          'Python',
          'Docker',
          'Kubernetes',
          'Gatling',
          'Vegeta'
        ],
        desc: `Built and maintained a sidecar service for Peapod microservices.
Researched Docker and Kubernetes for migration to microservices.
Conducted performance testing with Gatling and Vegeta.
Developed internal full-stack applications to automate CRUD operations.`
      },
      {
        name: 'Software Engineer Intern - Front End Team at Peapod Digital Labs',
        dateRange: 'Jun 2018 - Mar 2019',
        technologies: [
          'Vue.js',
          'Angular',
          'NativeScript',
          'Flutter',
          'Xamarin Forms'
        ],
        desc: `Developed a reusable Vue.js component library to standardize UI elements.
Researched integration strategies for Vue and Angular frameworks.
Investigated cross-platform frameworks including NativeScript, Xamarin Forms, and Flutter.
Collaborated with front-end team to implement unit tests.`
      },
      {
        name: 'Personal Projects',
        dateRange: 'Ongoing',
        technologies: [
          'Kotlin',
          'Rust',
          'AWS (ECS, Amplify, CDK, CodePipeline)',
          'Discord Bots',
          'Spring',
          'TypeScript',
          'Vue.js'
        ],
        desc: `Developed League of Legends Esports Platform including Discord Bot, backend API service, and OpenAPI specification.
Built shared Kotlin utility libraries, metrics framework, and public infrastructure tooling.
This site is built with Vue.js and deployed on AWS Amplify. Check out my GitHub for more projects!`
      }
    ]
  })
}
</script>

<style scoped>
</style>
