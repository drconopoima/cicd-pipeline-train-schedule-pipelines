pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                script {
                    echo 'Running build automation'
                    sh './gradlew build --no-daemon'
                }
            }
        }
    }
    post {
        always {
            script {
                echo 'Archiving build artifacts'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: 'true'
            }
        }
    }
}
