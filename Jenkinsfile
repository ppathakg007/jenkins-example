pipeline {
    agent any
    environment {
        MAVEN_HOME="/opt/apache-maven"
    }
    stages {
        stage ('Compile Stage') {

            steps {
              
                sh '${MAVEN_HOME}/bin/mvn clean compile'
               
            }
        }

        stage ('Testing Stage') {

            steps {
                
                    sh '${MAVEN_HOME}/bin/mvn test'
                
            }
        }


        stage ('Deployment Stage') {
            steps {
                
                    sh '${MAVEN_HOME}/bin/mvn deploy'
                
            }
        }
    }
}
