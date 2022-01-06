pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh '''grep formation /etc/passwd

'''
      }
    }

    stage('stage2') {
      steps {
        sh '''if test `grep -c formation /etc/passwd` -ne 0
then 
find /tmp -user formation  > /tmp/formation
fi
'''
      }
    }

    stage('stage3') {
      steps {
        sh '''for i in `cat /tmp/formation`
do
ls -il $i
done
'''
      }
    }

  }
}