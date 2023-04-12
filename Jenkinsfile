pipeline {
    agent any
    stages {
        stage( 'Installing Maven') {
            steps {
                sh 'sudo apt-get update -y && sudo apt-get upgrade -y'
            //    sh "sudo apt-get install -y wget tree unzip maven'
            }
        }
        stage( 'Compililing and riunning test case') {
            steps {
              sh 'mvn clean'
              sh 'mvn compile'
              sh 'mvn test'
            }
        }
        stage('Creating package') {
            steps {
                sh 'mvn package'
            }
        }
     }
}
