pipeline{
    agent any
    stages{
        stage('checkout code'){
            steps{
                sh '''
                    rm -rf *
                    git clone https://github.com/Shibil-Basith/website-sample.git
                '''
            }
        }
        stage('build'){
            steps{
                sh '''
                    pwd
                    ls -la
                    cd website-sample
                '''
                echo "Building completed"
            }
        }
        stage('test'){
            steps{
                sh '''
                    test -e website-sample/
                '''
                echo "testing completed"
            }
        }
        stage('deploy'){
            steps{
                sh '''
                    ls -la
                    cp -r website-sample/* /var/www/html/
                '''
                echo "deployment completed"
            }
        }
    }
}
