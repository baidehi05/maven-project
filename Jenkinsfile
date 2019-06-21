pipeline {
    agent any

    tools {
	maven 'local-maven'
    }

    stages {
        stage('Building') {
            steps {
                echo 'Bilding the project...'
		bat label: '', script: 'mvn clean package'
            }
	    post {
		success {
			echo 'Archiving Artificts...'
			archiveArtifacts artifacts: '**/*.war'
		}
	    }
		
        }
	stage('CheckStyle') {
            steps {
                echo 'CheckStyle...'
		checkstyle canComputeNew: false, defaultEncoding: '', healthy: '', pattern: 'clean package checkstyle:checkstyle', unHealthy: ''
            }
        }
    }
}
