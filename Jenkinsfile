pipeline {
  
  agent any 
    
    stages {
      
      stage ("setup parameters") {
        steps {
          parameters { string(name: 'DEPLOY_ENV', defaultValue: 'staging', description: '') }
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
      
