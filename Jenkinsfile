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
		stage("install nginx")
		{
			steps
			{
				sh "sudo apt update -y"
				sh "sudo apt install -y nginx"
			}
		}
		stage("Deploy the website")
		{
			steps
			{
				sh "sudo cp /project1/index.html /usr/share/nginx/html/index.html"
			}
		}
		stage("start the nginx")
		{
			steps
			{
				sh "sudo systemctl start nginx"
			}
		}
		stage("Git information")
		{
			steps
			{
				sh "git branch"
				sh "git log"
				sh "git log --oneline"
			}
		}
	}
}
