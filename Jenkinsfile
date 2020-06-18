pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'building'
        sh 'mvn -B -DskipTests clean package'
      }
    }

    stage('Test') {
      steps {
        echo 'testing'
        sh 'mvn test'
      }
    }

    stage('Deploy') {
      steps {
        echo 'deploying'
      }
    }

  }
}