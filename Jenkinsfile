pipeline {
    agent {
        docker {
            image 'node:20.9.0-alpine3.18' 
            args '-p 3000:3000' 
        }
    }
    stage('Checkout SCM') {
	steps {
		git url: 'https://github.com/kch-chaihong/simple-node-js-react-npm-app.git'
	}
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
