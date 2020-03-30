pipeline {
    agent none
    
    stages {
        stage('start') {
            steps {
                script {
                    openshift.withCluster() {
                        openshift.withProject( 'ben-test' ) {
                            echo "Hello from project ${openshift.project()} in cluster ${openshift.cluster()}"
                        }
                    }
                }
            }
        }
    }
}