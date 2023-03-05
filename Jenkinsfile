def gv
pipeline {
    agent any
    tools {
        maven 'maven-3.9'
    }
    stages {
            stage("init") {
                steps {
                    script {
                        gv = load "script.groovy"
                    }
                }
            }
    }
}
