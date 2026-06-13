pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package -DskipTests'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t rakeshs53350/petclinic:v1 .'
            }
        }

        stage('Docker Push') {
            steps {
                bat 'docker push rakeshs53350/petclinic:v1'
            }
        }
    }
}