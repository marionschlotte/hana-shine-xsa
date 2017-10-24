pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'export PATH=${WORKSPACE}/node_modules/grunt/bin:$PATH'
                sh 'java -jar /opt/sap/mta.jar --mtar northwind.mtar --build-target=NEO build'               
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
