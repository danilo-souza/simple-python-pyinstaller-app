pipeline {
    agent none 
    stages {
        stage('Build') { 
            agent {
                sudo docker {
                    image 'python:2-alpine' 
                }
            }
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
            }
        }
    }
}
