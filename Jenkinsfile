pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "yarn install"
                sh "yarn build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/learning"
                sh "sudo mkdir /var/www/learning"
                sh "sudo cp -r '${WORKSPACE}/build/' /var/www/learning/"
            }
        }
    }
}
