pipeline { 
    agent { 
        docker { 
            image 'python:3.10.1-alpine' 
            }
        } 
    stages { 
        stage ('Build') { 
                steps { 
                    echo 'Running build phase. ' 
                }
        }
        stage ('Test') { 
          steps { 
                    echo 
                    'Running test phase. ' 
                }
            
        }
    }           
 }
