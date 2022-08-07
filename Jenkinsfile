
pipeline {
  agent any

  tools {nodejs "node"}

  stages {

    stage('Git') {
      steps {
        git  'https://github.com/wsjung0516/jenkins-test.git'
      }
    }

    stage('Build') {
      steps {
        sh 'npm install'
         sh '<<Build Command>>'
      }
    }


    // stage('Test') {
    //   steps {
    //     sh 'node test'
    //   }
    // }
  }
}
//     stage('Checkout SCM') {
//         git branch: 'jenkins_test', url: 'https://github.com/wsjung0516/jenkins-test.git'
//     }

//     stage('Install node modules') {
//         sh "npm install"
//     }

//     stage("Test") {
//         sh "npm run test-headless"
//     }

//     stage("Build") {
//         sh "npm run build --prod"
//     }

//     stage("Copy") {
//         sh "cp -a /var/lib/jenkins/workspace/angular-pipeline/dist/jenkins-test/. /var/www/jenkins_test/html/"
//     }
// }
