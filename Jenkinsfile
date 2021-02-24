pipeline {
    agent any

    stages {
        stage("Checkout"){
            steps {
               echo 'Checkout...'
               checkout scm
            }
        }

         stage ("Prepare"){
            steps {
                echo 'Prepareing...'
                sh 'chmod +x ./gradlew'
            }
        }

         stage("Build"){
           steps {
                echo 'Building...'
                sh './gradlew clean assembleDebug' // builds app/build/outputs/apk/app-debug.apk
            }
        }

        
    }
}

