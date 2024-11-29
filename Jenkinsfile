pipeline {
	agent { 
    label 'master' 
	}

    stages {
        stage('Build') {
            steps {
                echo 'This is Build stage!'
            sh 'pwd'    
		    sh 'rm -rf *'
		    sh 'git clone -b devops_branch1 https://github.com/duggandlar/devops.git'
            }
        }
        stage('Test') {
            steps {
                echo 'This is Test stage!'
            sh 'pwd'
            sh 'ls -ltr'
		    sh 'cd devops/maven/my-app/ && mvn clean && mvn package && java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App'
		    echo 'Project build is complete'
            }
        }
    }
}
