pipeline {
    agent any
    stages {
        stage('test'){
            steps {
                sh 'echo "test"'
            }
        }
        stage('build'){
            steps {
                sh 'echo "build"'
                sh 'python -m py_compile sources/add2vals.py sources/calc.py'
            }
        }
        stage('push'){
            steps {
                sh 'echo "push"'
            }
        }
        stage('deploy'){
            steps {
                sh 'echo "deploy"'
            }
        }
    }
}