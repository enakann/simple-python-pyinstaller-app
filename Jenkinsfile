pipeline{
    agent none
 stages {
    stage ('Checkout'){
        git branch: 'master', url: 'https://github.com/enakann/simple-python-pyinstaller-app.git'
    }
   
        stage('Build'){
            agent {
            docker {
                image 'python:2-alpine'
            }
        }
        steps{
            sh 'python -m py_compile sources/add2vals.py sources/calc.py'
        }
    }
 }
}
