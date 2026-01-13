pipeline{
agent any
environment{
APP_NAME="Helloworld"
VERSION="1.0-${BUILD_NUMBER}"
}
stages{
stage("Build"){
steps
{
	echo "Here Compiling the Java file"
	bat 'javac Helloworld.java'
}
}
stage("test"){
when {
    expression { fileExists('Helloworld.class') }
}
steps{
	script{
	echo "testing the application and running it"
	try{
		bat 'java Helloworld'
	}catch(err)
	{
	currentBuild.result='FAILURE'
	error("TEST FAILED")
	}
}
}
}
stage("Packaging"){
steps{
	echo "lets see o/p and check right or wrong"
	echo "changed let's see what happens and package it"
	bat 'jar cf %APP_NAME%-%VERSION%.jar Helloworld.class'
	bat 'dir'
}
}
stage("Archive"){
steps{
archiveArtifacts artifacts: '*.jar', fingerprint: true
}
}
}
post {
        success {
            echo "Build succeeded"
        }
        failure {
            echo "Build failed"
        }
        always {
            echo "Cleaning up workspace"
            cleanWs()
        }
}
}