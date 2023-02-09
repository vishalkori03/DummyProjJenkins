pipeline {
    agent any

    stages {
        stage('Checkout GIT') {
            steps{
                git url:'https://github.com/vishalkori03/DummyProjJenkins.git', branch:'master'
				}

        }
		stage('Build') {
		steps{
		 sh "mvn -Dmaven.test.failure.ignore=true clean package"}}
		stage('Test') {
		steps{
		 sh "mvn test"}}
    }
	post {
                
                success {
                    echo 'Success-!!!'
                }
            }
}
 
