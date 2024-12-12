pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                script {
                    sh "docker build -f Dockerfile -t caosbinario/homer_page:1.0.0-${BUILD_ID} . " 
                }
            }
        }
        stage('docker push') {
            steps {
                script {
                    sh "docker push javierburgos/jenkins:1.0.0-${BUILD_ID}"
                }
            }
        }
    }
}