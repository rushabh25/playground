pipeline {
  
  agent any 
    
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
  
  stages {
    
    stage('Example') {
            steps {
              script {
                try {
                  for(String item in params.PERSON.split(',')) {
                    String trimmedItem = item.trim()
                    echo "hello ${trimmedItem}"
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
      
