pipeline {
    stages {
        stage("build") {
            steps {
                script {
                    try {
                        sh './gradlew build --no-daemon'
                    }
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
