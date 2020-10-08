@Library('retort-lib') _
def label = "jenkins-${UUID.randomUUID().toString()}"
 
def ZCP_USERID = 'earth1223'
def DOCKER_IMAGE = 'earth1223/hellozcp'
def K8S_NAMESPACE = 'earth1223'
def VERSION = 'develop'
 
podTemplate(label:label, serviceAccount: "zcp-system-sa-${ZCP_USERID}") {
 
    node(label) {
        stage('SOURCE CHECKOUT') {
            def repo = checkout scm
            env.SCM_INFO = repo.inspect()
        }
    }
}
