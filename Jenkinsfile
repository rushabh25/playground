pipeline {
  
  agent any 
    
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
  
  stages {
    
    stage('Example') {
            steps {
              params.PERSON.split(',').each {
                item -> echo "hello ${item}.trim()"
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
      
