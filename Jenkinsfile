pipeline {
    agent any

    stages {
        stage('continuous download') {
            steps {
                git 'https://github.com/kliakos/sparkjava-war-example.git'
           
        }
        stage('continuous build') {
            steps {
             sh 'mvn install'   
            }
        }
         stage('continuous deployment') {
            steps {
             sh 'sshpass -p "nikhila" scp target/maven-compiler-plugin-3.1.war root@172.17.0.3:/var/lib/apache-tomcat-9.0.56/webapps'   
            }
        }
       
    }
}

