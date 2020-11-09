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
            archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: 'true'
        }
    }
}
