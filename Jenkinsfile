pipeline {
    agent any

    environment {
        CONTAINER_NAME = "tilth-website-${env.BRANCH_NAME}"
        PORT = "${env.BRANCH_NAME == 'development' ? '8001' : '8000'}"
    }
    stages {
        stage('fetch') {
            steps {
                sh "docker build -t" ${CONTAINER_NAME}."
            }
        }
        stage('deploy') {
            steps {
                sh """
<<<<<<< HEAD
<<<<<<< HEAD
                docker stop ${CONTAINER_NAME} || true && docker run ${CONTAINER_NAME} || true
                docker run -dit --name ${CONTAINER_NAME} -p ${env.BRANCH_NAME == 'main' ? '8000': '8001'}:80 ${CONTAINER_NAME}
                """"
=======
                docker stop ${CONTAINER_NAME} || true && docker rm ${CONTAINER_NAME} || true
                docker run -dit --name ${CONTAINER_NAME} -p ${env.BRANCH_NAME == 'main' ? '8000': '8001'}:80 ${CONTAINER_NAME}""""
>>>>>>> ac99a07 (Added Jenkinsfile)
=======
                docker stop ${CONTAINER_NAME} || true && docker rm ${CONTAINER_NAME} || true
                docker run -dit --name ${CONTAINER_NAME} -p ${env.BRANCH_NAME == 'main' ? '8000': '8001'}:80 ${CONTAINER_NAME}""""
>>>>>>> 012c651 (Added Jenkinsfile)
            }
        }
        stage('cleanup') {
            steps {
                cleanWs()
            }
        }
    }
}
