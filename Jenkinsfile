pipeline {
    agent any
	parameters {
	choice(name: 'BRANCHES', choices: ['main', 'jar', 'war'], description: 'Pick Brannch to Build')}
	

    stages {
        stage('SCM') {
            steps {
                git branch: "${params.BRANCHES}", url: 'https://github.com/awskaizen02/maven_sample_repo.git'
            }
        }
	stage('Build'){
		steps{
			bat 'mvn clean'
			bat 'mvn install'
}		
	}
    }
}
