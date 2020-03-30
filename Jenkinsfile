pipeline {
    agent {
        none
    }

    openshift.withCluster() {
        openshift.withProject( 'ben-test' ) {
            echo "Hello from project ${openshift.project()} in cluster ${openshift.cluster()}"
        }
    }
}