@Library('jenkins-workflow-libs@v2-generic') _

def buildParameterMap = [:]
buildParameterMap['appName'] = 'docker-dynamo-libsodium'
buildParameterMap['buildClosure'] = buildClosure
buildParameterMap['buildStrategy'] = [
 'forza': [ 'checkout', 'containerize'
  ]
]

buildAndDeployGeneric(buildParameterMap)

// vim: set ft=groovy:
