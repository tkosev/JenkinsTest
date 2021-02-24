pipeline {
    agent any

    stages {
        stage("Checkout"){
            steps {
               checkout scm
            }
        }

         stage ("Prepare"){
            steps {
                sh 'chmod +x ./gradlew'
            }
        }

         stage("Build"){
           steps {
             sh './gradlew clean assembleDebug' // builds app/build/outputs/apk/app-debug.apk

            }
        }

        
    }
}

