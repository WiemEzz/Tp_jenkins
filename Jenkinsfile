pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh '''grep user /etc/passwd

'''
      }
    }

    stage('stage2') {
      steps {
        sh '''if test `grep -c user /etc/passwd` -ne 0
then 
find / -user user  > /tmp/orsys
fi
'''
      }
    }

    stage('stage3') {
      steps {
        sh '''for i in `cat /tmp/user`
do
ls -il $i
done
'''
      }
    }

  }
}