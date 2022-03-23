pipeline {
  agent {
    docker {
      image 'python:2-alpine'
    }

  }
  stages {
    stage('Basic Info') {
      steps {
        sh '''echo PATH = ${PATH}
echo M2_HOME = ${M2_HOME}'''
      }
    }

    stage('Build Python') {
      steps {
        sh 'python -m py_compile sources/add2vals.py sources/calc.py'
      }
    }

  }
}