def gv
pipeline {
    agent any
    stages {
            stage("build frontend") {
                steps {
                    sh '''
                    cd frontend
                    sudo npm i
                    sudo npm run build
                    '''
                }
            }
            stage("build backend") {
                steps {
                    sh '''
                    cd backend
                    sudo npm i
                    sudo npm run build
                    '''
                }
            }
    }
}
