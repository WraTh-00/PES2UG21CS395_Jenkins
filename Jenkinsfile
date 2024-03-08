pipeline {
  agent any  

  stages {
    stage('Build') {   // This stage builds the project
      steps {
        build 'PES2UG21CS395-1'  // This step builds the project using the build command
        sh 'g++ main.cpp -o output'  // This step compiles the source code using the g++ compiler
      }
    }
    stage('Test') {  // This stage tests the project
      steps {
        sh './output'  // This step runs the output binary
      }
    }
    stage('Deploy') {  // This stage deploys the project
      steps {
        echo 'deploy'  // This step prints a message to the console
      }
    }
  }
  post {  // This section defines a post-build block
    failure {  // This block will be executed if the pipeline fails
      error 'Pipeline failed'  // This step prints an error message to the console
    }
  }
}
