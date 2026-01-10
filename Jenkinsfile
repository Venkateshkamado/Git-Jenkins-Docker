pipeline{
agent any
stages{
stage(Build)
{
	echo "Building application"
}
stage(test)
{
	echo "testing the application"
}
stage(run)
{
	echo "Running the application"
	bat 'javac Helloworld.java'
	bat 'java Helloworld.java'
	echo "lets see o/p and check right or wrong"
}
}
}
}