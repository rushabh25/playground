def approvalMap

pipeline {
  
  agent any 
    
  stages {
    
    stage('Setup Env') {
      steps {
        script {
          approvalMap = input id: 'targetEnv', message: 'What files do you want to delete in a comma separated format', ok: 'Proceed?', parameters: [string(defaultValue: 'MY_FILE_NAME', description: 'File to be deleted, example: file1.txt,file2.txt', name:'targetEnv')]
          env.TARGET = approvalMap
        }
      }
    }
    
    stage('Example') {
            steps {
              script {
                try {
                  for(String item in env.TARGET.split(',')) {
                    String trimmedItem = item.trim()
                    sh 'echo \"hello ${trimmedItem}\"'
                  }
                } catch (err) {
                  echo "caught exception: ${err.getMessage()}"
                }
            }
        }
    }
 
      stage ("build") {
        steps {
          echo "building the application"
        }
      }
    
    stage ("proceed with the remaining steps") {
      steps {
        input message: "Proceed with remaining steps?"
      }
    }
      
      stage ("test") {
        steps {
          echo "testing the application"
        }
      }
      
      stage ("deploy") {
        steps {
          echo "deploying the application"
        }
      }
    }
}
      
