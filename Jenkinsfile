pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               
                sh '''
                python3 -m venv mlip
                . mlip/bin/activate
                pip install pytest numpy pandas scikit-learn

                '''


            }
        }
        stage('Test') {
            steps {

                sh '''
                . mlip/bin/activate
                pytest
                
                '''

            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
