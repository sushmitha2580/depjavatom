pipeline {
    agent {
     label 'agent1'
   }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', curl: 'https://github.com/sushmitha2580/java-example-artisan.git'
            }
        }
        stage('Test') {
            steps {
                echo "testing"
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
		
        stage('Deploy') {
            steps {
		          sh 'sudo cp /home/ubuntu/jenkins/workspace/depjavatom/target/*.war /home/ubuntu/tomcat/webapps/'
				  echo "deployed to tomcat successfully"            }
        }
    }

}

