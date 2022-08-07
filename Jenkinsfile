node {
    stage('Checkout SCM') {
        git branch: 'jenkins_test', url: 'https://github.com/wsjung0516/jenkins-test.git'
    }

    stage('Install node modules') {
        sh "/usr/bin/npm install"
        sh "npm install"
    }

    stage("Test") {
        sh "npm run test-headless"
    }

    stage("Build") {
        sh "npm run build --prod"
    }

    stage("Copy") {
        sh "cp -a /var/lib/jenkins/workspace/angular-pipeline/dist/jenkins-test/. /var/www/jenkins_test/html/"
    }
}
