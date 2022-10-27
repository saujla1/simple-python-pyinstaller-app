pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'python3 -m py_compile sources/add2vals.py sources/calc.py'
                sh 'python3 - m pip install pytest'
        
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
