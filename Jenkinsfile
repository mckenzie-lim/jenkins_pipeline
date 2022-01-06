pipeline {
  agent any
  stages {
    stage('Stage1') {
      steps {
        sh '''git clone https://github.com/abesrour1111/git_devops.git 
'''
      }
    }

    stage('Stage2') {
      steps {
        sh '''cd git_devops 
ls | wc -l'''
      }
    }

    stage('Stage3') {
      steps {
        sh '''if test `ls | wc -l` -e 2
then 
grep modification gestion_utilisateurs tail -1
grep modification gestion_groupes tail -1
fi 
'''
      }
    }

    stage('Stage4') {
      steps {
        sh '''if test `ls | wc -l` -ne 2
then 
echo "echec"
fi '''
      }
    }

  }
}