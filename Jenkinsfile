pipline{
    agent{
        docker{
            image 'stark77/obraz01'
        }
    }
        tools {
        maven "m3"
    }
    stages {
        stage('git'){
            git 'https://github.com/eug3n33/box.git'
        }
        stage ('build'){
            sh 'mvn package'
        }
        stage ('docker image'){

        }
        stage ('run docker'){

        }
    }
}