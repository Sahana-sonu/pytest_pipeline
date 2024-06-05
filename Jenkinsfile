pipeline {
    agent {
       node {
         label 'agent_dev1'
      }
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Sahana-sonu/pytest_pipeline.git', credentialsId: 'test_pipeline'
            }
        }
        
        stage('Run') {
            steps {
                bat 'python test_ops.py'
            }
        }
    }
}
