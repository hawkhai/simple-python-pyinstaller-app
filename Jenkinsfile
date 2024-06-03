pipeline {
    agent any
    stages {
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
        stage('Deliver') {
            steps {
                sh 'pyinstaller --onefile sources/add2vals.py'
            }
            post {
                success {
                    archiveArtifacts 'dist/add2vals'
                }
            }
        }
    }
}