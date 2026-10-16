pipeline
{
	agent any
	stages
	{
		stage("download git code")
		{
			steps
			{
				checkout scm
			}
		}
		stage("install apache2")
		{
			steps
			{
				sh "sudo apt update -y"
				sh "sudo apt install -y apache2"
			}
		}
		stage("Deploy the website")
		{
			steps
			{
				sh "sudo cp /project1/index.html /var/www/html/index.html"
			}
		}
		stage("start the apache2")
		{
			steps
			{
				sh "sudo systemctl start apache2"
			}
		}
	}
}
