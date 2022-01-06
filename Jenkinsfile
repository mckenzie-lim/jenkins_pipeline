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
        sh '''if test `ls | wc -l` -eq 2
then 
grep -A1 modification gestion_utilisateur 
grep -A1 modification gestion_groupes
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