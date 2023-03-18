pipeline {
  agent any
  tools {
      gradle 'gradle'
  }
  stages {
      stage("Build") {
        steps {
           sh './gradlew clean build'
        }
        post {
            success {
                archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
            }
        }
      }
  }
}
