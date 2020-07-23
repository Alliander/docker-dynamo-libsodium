@Library('jenkins-workflow-libs@v2-generic')

def buildClosure = {

}

def buildParameterMap = [:]
buildParameterMap['appName'] = 'docker-dynamo-libsodium'
buildParameterMap['buildClosure'] = buildClosure
buildParameterMap['buildStrategy'] = [
  'forza': ['checkout', 'containerize']
]

buildAndDeployGeneric(buildParameterMap)
