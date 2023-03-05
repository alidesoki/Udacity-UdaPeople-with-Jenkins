def gv
pipeline {
    agent any
    stages {
            stage("deploy frontend") {
                steps {
                    sh '''
                    cd frontend
                    npm i
                    '''
                }
            }
    }
}
