pipeline{
agent any
stages{
stage("Build"){
steps
{
	echo "Here Compiling the Java file"
	bat 'javac Helloworld.java'
}
}
stage("test"){
steps{
	echo "testing the application and running it"
	bat 'java Helloworld.java'
}
}
stage("Packaging"){
steps{
	echo "lets see o/p and check right or wrong"
	echo "changed let's see what happens and package it"
	bat 'jar cf Helloworld.jar Helloworld.class'
}
}
}
}