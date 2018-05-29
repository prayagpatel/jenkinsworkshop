pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${params.Name}!"
        sh 'java -version'
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
    stage('Wait for ') {
      steps {
        echo 'Continuing Deployment'
        input 'Should we continue'
      }
    }
  }
  environment {
    MY_NAME = 'Prayag'
    TEST_USER = credentials('test-user')
  }
  post {
    aborted {
      echo 'Why didn\'t you push my button?'
      
    }
    
  }
  parameters {
    string(name: 'Name', defaultValue: 'Prayag Patel', description: 'Who should I say hi to?')
  }
}
