/**
* Android Jenkinsfile
*/
node("android"){
  stage("Checkout"){
    checkout scm
  }

  stage ("Prepare"){
    sh 'chmod +x ./gradlew'
  }

    stage("Build"){
    if (params.BUILD_CONFIG == 'release') {
      sh './gradlew clean assembleRelease' // builds app/build/outputs/apk/app-release.apk file
    } else {
      sh './gradlew clean assembleDebug' // builds app/build/outputs/apk/app-debug.apk
    }
  }

  def keyStoreId = params.BUILD_CREDENTIAL_ID
  def keyAlias = params.BUILD_CREDENTIAL_ALIAS ?: ''

}