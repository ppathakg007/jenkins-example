pipeline {
    agent any
    environment {
        MAVEN_HOME="/opt/apache-maven"
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : '/opt/apache-maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
