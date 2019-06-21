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
        }
    }
}
