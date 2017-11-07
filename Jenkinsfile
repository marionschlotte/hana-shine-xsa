pipeline {
    agent any

    stages {
	stage("Clone"){

	    git "https://github.com/marionschlotte/hana-shine-xsa.git"

	}
        stage('Build') {
            steps {
                echo 'Building..'
//                sh 'export PATH=${WORKSPACE}/node_modules/grunt/bin:$PATH'
                sh 'java -jar /opt/sap/mta.jar --mtar -version'               
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
