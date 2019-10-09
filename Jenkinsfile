node {

    stage('SCM checkout'){
      git credentialsId: 'git-cred', url: 'https://github.com/senaint/practgit', branch: 'master'
    }

    stage('Environment') {
      sh 'git --version'
      echo "Branch: ${env.BRANCH_NAME}"
      sh 'docker -v'
      sh 'printenv'
    }

    stage('Deploy'){

      sh 'docker-compose up -d'
 
      }

}
