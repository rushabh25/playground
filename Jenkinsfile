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
                  params.PERSON.split(',').each { item -> echo "hello ${item}" }
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
      
