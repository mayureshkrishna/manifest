pipeline {
  agent {
    docker {
      image 'mayureshkrishna/venue:latest'
    }

  }
  stages {
    stage('deploy') {
      steps {
        pushToCloudFoundry(target: 'api.sys.pcf25.az.deployfast.io', organization: 'mk', cloudSpace: 'dev', credentialsId: 'mk-pcf', selfSigned: 'true', pluginTimeout: '120')
      }
    }
  }
}