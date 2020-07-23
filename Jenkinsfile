@Library('jenkins-workflow-libs@v2-generic') 
def buildParameterMap = [:]
buildParameterMap['appName'] = 'docker-dynamo-libsodium'
buildParameterMap['buildStrategy'] = [
  "forza": ["checkout", "containerize"]
]
buildAndDeployGeneric(buildParameterMap)
