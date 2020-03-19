pipeline {
	agent {
	  label '192.168.2.16'
	}

	stages {
	  stage('first stage') {
	    steps {
	      sh 'xxx'
	    }
	  }
		
	  stage('second stage') {
	    steps {
              sh 'xxx'
            }
	  }
	}

	post {
	  success {
	    sh "mail subject to '2240930501@qq.com' "
	  }
	
	}


}