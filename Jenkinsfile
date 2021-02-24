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






// Uncomment this stage if your keystore is external to your source code.
//  stage("Sign"){
//    if (params.BUILD_CONFIG == 'release') {
//        signAndroidApks (
//            keyStoreId: keyStoreId,
//            keyAlias: keyAlias,
//            apksToSign: "**/*-unsigned.apk",
            // uncomment the following line to output the signed APK to a separate directory as described above
            // signedApkMapping: [ $class: UnsignedApkBuilderDirMapping ],
            // uncomment the following line to output the signed APK as a sibling of the unsigned APK, as described above, or just omit signedApkMapping
            // you can override these within the script if necessary
            // androidHome: '/usr/local/Cellar/android-sdk'
       // )
//    } else {
//      println('Debug Build - Using default developer signing key')
//    }
// }
    }
}

