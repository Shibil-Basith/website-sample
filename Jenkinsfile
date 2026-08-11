pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                sh '''
                    rm -rf *
                    git clone https://github.com/Shibil-Basith/website-sample.git
                '''
            }
        }
        stage('deploy'){
            steps{
                sh '''
                    ls -la
                    rm -rf /var/www/html/*
                    cp -r website-sample/* /var/www/html/
                '''
                echo "deployment completed"
            }
        }
    }
}
