pipeline{
  agent any
  stages{
    stage('checkout'){
      steps{
        deleteDir()
        sh '''
          git clone https://github.com/Shibil-Basith/website-sample.git
          ls -l
          pwd
        '''
      }
    }
    stage('deploy'){
      steps{
        rm -rf /var/www/html/*
        cp -r website-sample/* /var/www/html
        ls -l
      }
    }
  }
}
