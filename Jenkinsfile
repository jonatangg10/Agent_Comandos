pipeline {
    agent none
    environment {
        LANG = 'es_CO.UTF-8'
        LANGUAGE = 'es_CO:es'
    }
    stages {
        stage('Build') { 
            agent { label 'any' }
            steps {
                echo "${WORKSPACE}"
            }
        }
    }
}
