pipeline {
  agent any
  stages {
      stage("frontend") {
          steps {
            echo "building in progress..." 
            echo "Added polling method"
            echo "Adding Gradle Wrapper"
            withGradle() {
              sh './gradlew -v'
            }
          }
      }
      stage("test") {
          steps {
            echo "testing in progress..." 
            echo "Added polling method"
            echo "Adding NodeJS wrapper"
            nodejs('Node 20.0.0') {
                sh 'npm config ls'
                sh 'yarn install'
            }
          }
      }
      stage("deploy") {
          steps {
            echo "deploying in progress..." 
          }
      }
  }
}
