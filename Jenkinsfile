pipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/prakashk0301/product-app.git'
        }
    }
    {
		stage('trigger the docker-compose') {
			steps {
				sh label: '', script: 'docker-compose -f docker-compose.yml up -d --build'
				
			}
		}
	}
}
