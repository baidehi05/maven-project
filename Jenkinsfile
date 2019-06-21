pipeline {
    agent any

    tools {
	maven 'localMaven'
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
