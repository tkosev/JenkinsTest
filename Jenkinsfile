pipeline {
    agent any

    stages {
        stage("Checkout"){
            echo 'Checkout....'
            steps {
               checkout scm
            }
        }

         stage ("Prepare"){
            echo 'Preparing....'
            steps {
                sh 'chmod +x ./gradlew'
            }
        }

         stage("Build"){
           echo 'Preparing....'
           steps {
             sh './gradlew clean assembleDebug' // builds app/build/outputs/apk/app-debug.apk

            }
        }

        
    }
}

