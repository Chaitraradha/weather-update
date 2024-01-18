pipeline {
    agent { label 'slave4' }
    stages {
        stage('checkout') {
            steps {
                sh 'rm -rf weather-update'
                sh 'git clone https://github.com/Chaitraradha/weather-update.git'
            }
        }
       stage('build') {
            steps {
                    sh 'mvn --version'
                    sh 'mvn clean install'
                  }
       }
    }
}



        
             
         
