pipeline{
agent any
stages{
stage("Build"){
steps
{
	echo "Building application"
}
}
stage("test"){
steps{
	echo "testing the application"
}
}
stage("run"){
steps{
	echo "Running the application"
	bat 'javac Helloworld.java'
	bat 'java Helloworld.java'
	echo "lets see o/p and check right or wrong"
}
}
}
}