pipeline {
    agent any
    stages {
        stage ("Clean"){
            steps {
                deleteDir()
            }
        }
        stage ("Clone repo") {
            steps {
                sh "git clone https://github.com/jenkins-docs/simple-java-maven-app.git"
            }
        }
        stage ("Build") {
            steps {
                dir("simple-java-maven-app") {
                    sh "mvn clean install"
                }
            }
        }
        stage ("Test") {
            steps {
                dir("simple-java-maven-app") {
                    sh "mvn test"
                }
            }    
        }
    }
}
