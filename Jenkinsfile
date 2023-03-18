pipeline {
  agent any
  tools {
      maven 'M3'
  }
  stages {
      stage("Build") {
        steps {
           sh 'mvn clean package'
           sh 'bin/makeindex'
        }
        post {
            success {
                archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
            }
        }
      }
  }
}
