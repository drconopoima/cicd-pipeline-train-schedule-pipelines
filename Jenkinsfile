pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                script {
                    sh './gradlew build --no-daemon'
                }
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md', fingerprint: 'true'
        }
    }
}
