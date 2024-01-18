pipeline {
    agent { label 'slave4' }
    stages {
        stage('checkout') {
            steps {
                sh 'rm -rf 'weather-update'
                sh 'git clone https://github.com/Chaitraradha/weather-update.git'
            }
        }
       stage('build') {
            steps {
                    sh 'mvn --version'
                    sh 'mvn clean install'
                  }
            //stage('deploy') {
            steps {
                    sh 'scp /home/slave4/workspace/Pipeline1/target/ root@172.31.8.32:/opt/apache-tomcat-8.5.98/webapps'
                    }
       }
             }
         }
