@Library('jenkins-workflow-libs@v2-generic')

def buildClosure = {
  container("node-14-alpine") {
    stage('containerize')
  }
}

def buildParameterMap = [:]
buildParameterMap['appName'] = 'docker-dynamo-libsodium'
buildParameterMap['buildClosure'] = buildClosure
buildParameterMap['buildStrategy'] = [
  "forza": ['checkout', 'containerize']
]
buildParameterMap['customPodTemplate'] = """
apiVersion: v1
kind: Pod
spec:
  containers:
  - name:  node-14-alpine
    image: node:14-alpine
    command:
    - /bin/cat
    tty: true
    resources:
      limits:
        cpu: 4
        memory: 4Gi
      requests:
        cpu: 200m
        memory: 4Gi
"""

buildAndDeployGeneric(buildParameterMap)
