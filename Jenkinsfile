pipeline {
	//����job�����нڵ�
	agent {
	  label '192.168.2.16'
	}
	
	//���ô�����
	triggers {
	  pollSCM(H/5 * * * *)
	}
	
	//���ý׶λ�����ˮ�ߵĻ���������Ϊ������Ϊ��������ʹ��
	environments {
	  name = 'dinglin'
	}

	stages {
	  stage('first stage') {
	    steps {
	      sh 'xxx'
	    }
	  }
		
	  stage('second stage') {
	    tools {
	      maven 'mvn'   //tools�����Զ���װ�����ֶ���װ�Ĺ��ߵĻ�����������������Ҫ��global tool configuration��ָ��
	    }

	    steps {
              sh 'mvn --version'
            }
	  }
	}

	post {
	  success {
	    sh "mail subject to '2240930501@qq.com' "
	  }
	
	}


}