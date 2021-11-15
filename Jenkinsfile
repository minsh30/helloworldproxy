pipeline {
    agent any

    stages {
        stage('clean') {
            steps {
                echo 'CLEAN'
            }
        }
            stage('install') {
            steps {
                echo 'INSTALL'
            }
            }
            stage('build common parent') {
            steps {
                build 'api-common-parent'
            }
            }
              stage('build hellow world proxy') {
            steps {
                git 'https://github.com/minsh30/helloworldproxy.git'
               bat 'mvn clean install -P apigee-prep -D username=minshud@sidgs.com -D password=Minshu@123 -D env=test -D org=amer-mint-partner01'
            }
            }
    
        }
    }
}
