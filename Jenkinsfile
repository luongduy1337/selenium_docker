pipeline {
    agent any
    stages {
        stage("Build Jar"){
            steps{
                sh "mvn clean package -DskipTests"
            }

        }

        stage("Build Image"){
            steps {
                echo "docker build -t=luongtranduy/selenium ."
            }
        }

        stage("Pushing Image"){
            steps {
                echo "docker push luongtranduy/selenium"
            }
        }
    }

    post{

        always{
            echo 'doing clean up'
        }

    }
}