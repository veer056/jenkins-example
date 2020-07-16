pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                tool name: 'maven_3_5_0', type: 'maven' {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
               tool name: 'maven_3_5_0', type: 'maven' {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
               tool name: 'maven_3_5_0', type: 'maven' {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
