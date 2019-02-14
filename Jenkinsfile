pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo "Building the Job with MAVEN"
            }
            steps{
                sh 'mvn clean package'
            }
            post{
                always{
                    echo "Verifying the status"
                }
                success{
                    echo "========Build executed successfully======="
                }
                failure{
                    echo "========Build execution failed========"
                }
            }
        }

        stage('SonarQube Testing'){
            steps{
                echo "===Static Code Analysis started=="
                sh 'mvn clean verify sonar:sonar -Dsonar.projectName=PRADHAN -Dsonar.projectKey=PRADHAN -Dsonar.projectVersion=$BUILD_NUMBER'
            }

        }

    }
    
    }
