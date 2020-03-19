pipeline {
	//设置job的运行节点
	agent {
	  label '192.168.2.16'
	}
	
	//设置触发器
	triggers {
	  pollSCM(H/5 * * * *)
	}
	
	//设置阶段或者流水线的环境变量，为后面作为变量引用使用
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
	      maven 'mvn'   //tools设置自动安装或者手动安装的工具的环境变量，该名称需要在global tool configuration中指定
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