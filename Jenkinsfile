pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    stages {
        stage('dev') {
            steps {
                sh 'python --version'
            }
        }
        stage('test') {
            steps {
                 //This sh step runs the Python command to compile your application and
                //its calc library into byte code files, which are placed into the sources workspace directory
                sh 'python -m py_compile sources/app.py'
            }
        }
        stage('result') {
            steps {
                 //This stash step saves the Python source code and compiled byte code files from the sources
                //workspace directory for use in later stages.
                stash(name: 'compiled-results', includes: 'sources/*.py*')
            }
        }
    }
  }
