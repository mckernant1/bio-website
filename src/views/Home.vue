<template>
  <v-container class="fill-height grid-list-md text-xs-left">
    <v-layout class="row align-top justify-center">
      <v-container>

        <!-- Header / Bio -->
        <v-card class="ma-3">
          <v-card-title class="display-1">Bio</v-card-title>
          <v-divider light></v-divider>
          <v-card-text class="headline">
            Software Engineer with 5+ years of experience in cloud infrastructure, DevOps automation, and distributed systems.
            Skilled in Java, Kotlin, Python, and Rust, with expertise in CI/CD pipelines, Kubernetes, Docker, Terraform, and AWS cloud-native solutions.
            Experienced in mentoring, troubleshooting, and delivering high-performance systems that improve reliability and availability.
          </v-card-text>
        </v-card>

        <!-- Skills -->
        <v-card class="ma-3">
          <v-card-title class="display-1">Skills</v-card-title>
          <v-divider light></v-divider>
          <v-card-text class="headline">
            <v-list dense>
              <v-list-item-title><strong>Programming:</strong> Java, Kotlin, Python, Rust, Bash</v-list-item-title>
              <v-list-item-title><strong>Cloud & DevOps:</strong> AWS (S3, DynamoDB, EKS, ECR, SQS), Kubernetes, Docker, Helm, CloudFormation, Terraform, GitHub Actions, Jenkins, CI/CD</v-list-item-title>
              <v-list-item-title><strong>Tools & Frameworks:</strong> Spring, Linux, TypeScript, Git, GRPC</v-list-item-title>
              <v-list-item-title><strong>Other:</strong> Agile, Scrum, Mentoring, Problem-Solving, Ownership</v-list-item-title>
            </v-list>
          </v-card-text>
        </v-card>

        <!-- Education -->
        <v-card class="ma-3" dark>
          <v-card-title class="display-1">Education</v-card-title>
          <v-divider light></v-divider>
          <v-card-text class="headline">
            <ul class="pl-5">
              <li>B.S. Computer Science, Minor in Mathematics</li>
              <li>University of Dayton, Aug 2016 – Dec 2019</li>
            </ul>
          </v-card-text>
        </v-card>

        <!-- Selected Projects -->
        <v-card class="ma-3">
          <v-card-title class="display-1">Selected Projects</v-card-title>
          <v-divider light></v-divider>
          <v-card-text class="headline">
            <ul class="pl-5">
              <li>
                <strong>League of Legends Esports Platform</strong> — Discord Bot, API Service, OpenAPI Spec
                <br/>Kotlin-based bot and backend API with structured OpenAPI specification. Provides match schedules, standings, and user predictions.
              </li>
              <li>
                <strong>Infrastructure Libraries & Tooling</strong> — Kotlin Utilities, Metrics, Public Infra
                <br/>Shared libraries for logging, configuration, and telemetry. CI/CD pipelines and AWS CDK deployments for internal tools.
              </li>
              <li>
                <strong>Auto-Updater & Personal Projects</strong> — Various personal apps
                <br/>Discord bots, Vue.js websites, AWS-deployed projects, and homebrew utilities. Full-stack and cloud-focused.
              </li>
            </ul>
          </v-card-text>
        </v-card>

        <!-- Fun Facts -->
        <v-card class="ma-3" dark>
          <v-card-title class="display-1">Fun Facts</v-card-title>
          <v-divider light></v-divider>
          <v-card-text class="headline">
            <ul class="pl-5">
              <li>Favorite languages: Kotlin and Rust</li>
              <li>Big fan of JetBrains IDEs (VSCode is cool too)</li>
              <li>Enjoy collaborating and sharing meals with fellow developers</li>
            </ul>
          </v-card-text>
        </v-card>

      </v-container>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'ResumeFirstPage'
}
</script>

<style scoped>
a.white--text {
  text-decoration: underline;
}
</style>
