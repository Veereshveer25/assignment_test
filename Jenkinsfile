pipeline {
	agent { label 'node2' }
        stages {
		stage ('javaprojects') {
			steps {
				sh '''#!/bin/bash
				            git pull https://github.com/riyaz-ahamadm92/java-projects.git
				            if [ $? -ne 0 ] ; then
				            git clone https://github.com/riyaz-ahamadm92/java-projects.git
				            fi
				            cd java-projects
				            mvn clean install
				            if [ $? -eq 0 ] ; then
				            echo " Build is success "
					    else
				            echo " Build is failed "
				            fi '''
				            }
				       }
	}
}
	
