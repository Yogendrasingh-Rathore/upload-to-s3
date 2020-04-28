pipeline {
   agent any
   tools {
      maven "mvn3.6"
   }

   stages {
       
      stage('Upload Artifact to s3') {
          steps{

              git 'https://github.com/Yogendrasingh-Rathore/simple-java-maven-app.git'

              s3Upload(
                consoleLogLevel: 'INFO', 
                dontSetBuildResultOnFailure: false, 
                dontWaitForConcurrentBuildCompletion: false,
                entries: [[bucket: 'jenkins-artifacts-yuvi', 
                        excludedFile: '', 
                        flatten: false, 
                        gzipFiles: false, 
                        keepForever: false,
                        managedArtifacts: false,
                        noUploadOnFailure: false,
                        selectedRegion: 'ap-south-1',
                        showDirectlyInBrowser: false,
                        sourceFile: '**/webapp/target/*.war',
                        storageClass: 'STANDARD',
                        uploadFromSlave: false,
                        useServerSideEncryption: false]],
                pluginFailureResultConstraint: 'FAILURE',
                profileName: 'jenkins-artifacts',
                userMetadata: [] 
             )
          }
      }
   }
}
