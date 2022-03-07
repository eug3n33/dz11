pipeline{
    agent{
        docker {
            image 'stark77/obraz01'
        }
    }
        tools {
        maven "m3"
    }
    stages {
        stage('git'){
            steps{
               git 'https://github.com/eug3n33/box.git'
            }
        }
        stage ('build'){
            steps{
               sh 'mvn package'
            }
        }
        stage ('docker image'){
            steps{
               sh 'sodo apt install docker.io'
               sh 'docker build -t obraz02 .'
               sh '''docker image tag obraz02 stark77/obraz02 && docker push stark77/obraz02'''
            }
        }
        stage ('run docker'){
            steps{
               sh 'ssh root@130.193.39.33'
               sh 'docker push stark77/obraz02'
               sh 'docker-compose up -d'
            }

        }
    }
}