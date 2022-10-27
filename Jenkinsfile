pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
        
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
