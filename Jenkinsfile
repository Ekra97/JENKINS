pipeline {
  agent any
  stages {
    stage('') {
      steps {
        sh '''
pipeline {
  agent any
  stages { 
    stage(\'stage 1\') {
      steps {
        sudo apt-get -y update && sudo apt-get -y upgrade
      }
    }

    stage(\'stage 2\') { 
      steps {
        dpkg -1 > /tmp/paquets
      }
    }

    stage (\'stage 3\') {
      steps {
         if [\'grep -c git /tmp/paquets\' - ne 0 ]
then
dpkg -s git
else
sudo apt-get install -y git
fi
      }
    }

  }
}
  '''
      }
    }

  }
}