#!groovy
@Library('dynamo-workflow-libs') _

pipeline {
  agent any
  options {
    // Only keep the 10 most recent builds
    buildDiscarder(logRotator(numToKeepStr:'10'))
  }
  stages {

    stage ('Start') {
      steps {
        sendNotifications 'STARTED'
        sh 'env'
      }
    }

    stage ('Docker Build & Deploy') {
      steps {
        dockerBuildAndDeploy(env.REGISTRY_SERVER, 'usefdynamo/dynamo-libsodium', "ci-${env.BUILD_TIMESTAMP}")
      }
    }

  }
  post {
    always {
      sendNotifications currentBuild.result
    }
  }
}



//def buildParameterMap = [:]
//buildParameterMap['appName'] = 'dynamo-libsodium'

//buildAndDeployGeneric(buildParameterMap)
