pipeline {
    agent {
         label 'jenkins_agent'
    }
    stages {
        stage('Pull') {
            steps {
                sh 'docker pull nginx'
            }
        }
        stage('Push') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'docker-hub', usernameVariable: 'username', passwordVariable: 'pass')]) {
                sh 'docker login -u ${username} -p ${pass}'
                sh 'docker tag nginx ranahesham/nginx:on_jenkins_slave'
                sh 'docker image push ranahesham/nginx:on_jenkins_slave'
                }
            }
        }

    }
}
