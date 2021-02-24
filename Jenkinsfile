pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
             echo 'Compileing....'
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Deployment Stage') {
            steps {
               echo 'Building....'
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}