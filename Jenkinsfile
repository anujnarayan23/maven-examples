pipeline {
    agent any
    tools {
    maven '3.6.3'
        }
stages {
	stage('Build') {
	steps {
    sh ' cd maven-code-coverage'
	sh 'mvn -B -DskipTests clean package'
	}
}// End of Build
stage('Test') {
	steps {
    sh ' cd maven-code-coverage'
		sh 'mvn test'
		junit 'target/surefire-reports/*.xml'
	}
}//end of test

}//End of Stages
}//end pipeline
