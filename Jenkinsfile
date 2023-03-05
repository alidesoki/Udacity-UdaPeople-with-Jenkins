def gv
@Library('github.com/releaseworks/jenkinslib') _
pipeline {
    agent any
    stages {
            // stage("build frontend") {
            //     steps {
            //         sh '''
            //         cd frontend
            //         sudo npm i
            //         sudo npm run build
            //         '''
            //     }
            // }
            // stage("build backend") {
            //     steps {
            //         sh '''
            //         cd backend
            //         sudo npm i
            //         sudo npm run build
            //         '''
            //     }
            // }
            stage("test aws") {
                steps {
                    withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
                    AWS("--region=us-west-1 s3 ls")
                    }
                }
            }
    }
}
