pipeline {
    agent {
        docker { image "ubuntu:18.04"
                  args '-u root:root -v $HOME/workspace/myproject:/myproject'
        }
    }
    stages {
       stage('Checkout SCM') {
          steps {
            checkout([
              $class: 'GitSCM',
              branches: [[name: "**" ]],
              userRemoteConfigs: [[
                url: 'https://github.com/hwchiu/jenkins-test.git',
                credentialsId: '',
              ]]
             ])
           }
        }
        stage('Test') {
            steps {
                sh '''
                echo "haha"
                '''
            }
        }
    }
}
