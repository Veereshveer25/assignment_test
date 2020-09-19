pipeline {
	agent { label 'node2' }
        stages {
		stage ('STAGE 1') {
			steps {
				sh '''#!/bin/bash
				git pull https://github.com/Veereshveer25/javaproject.git
				if [ $? -ne 0 ] ; then
				git clone https://github.com/Veereshveer25/javaproject.git
				fi
				cd javaproject 
				mvn clean install
				if [ $? -eq 0 ] ; then
				echo " Build is success "
				else
				echo " Build is failed "
				fi
				'''
			}	
		}
		
	}
}
