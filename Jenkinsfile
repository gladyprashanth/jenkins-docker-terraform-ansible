pipeline {
  agent any
  stages {
    stage('VINAYAK') {
      steps {
        script{
                def mvnHome = tool name: 'maven', type: 'maven'
                sh "${mvnHome}/bin/mvn package"
        }
      }
    }
    stage('BUILD PRASATH') {
      steps{
        script {
          sh "docker build -t prashanth/cicd-poc-jenkins-ansible:$BUILD_NUMBER ."
        }
      }
    }
    stage('Push PRASHANTH') {
      steps{
        script {
          sh "echo $USER"
          sh "docker login -u gladyprashanth -p Prash@911"
          sh "docker push prashanth/cicd-poc-jenkins-ansible:$BUILD_NUMBER"
          }
        }
      }
    }
}

