pipeline {
    agent {
        node {
            label 'nodejs'
        }
    }

    stages {
        stage('start') {
            steps {
                script {
                    openshift.withCluster() {
                        openshift.withProject() {
                            echo "Hello from project ${openshift.project()} in cluster ${openshift.cluster()}"
                        }
                    }
                }
            }
        }
    }
}