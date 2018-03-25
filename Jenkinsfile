pipeline{
    agent any
    stages {
        stage ('Initialize') {
            steps {
                sh 'mvn clean package'
            }
            post{
                success{
                    echo 'Now Archieving'
                    archieveArtifacts artifacts:'**/target/*.war'
                }
            }
        }
    }
}