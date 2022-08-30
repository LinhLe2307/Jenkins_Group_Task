pipeline {
  agent any

  tools {nodejs "node"}
 
  stages {
  
    stage ("build") {
      steps{
        echo "building my app..."
      }
    
    }
    stage ("test") {
      steps {
        echo "testing my app..."
        sh 'npm test'
      }
    }
    stage ("deploy") {
     steps {
        echo "deploying my app..."
      }
    }
  }
}