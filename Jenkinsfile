pipeline {
	agent { label 'node2' }
        stages {
		stage ('C-Project') {
			steps {
				sh '''#!/bin/bash
				git pull https://github.com/Veereshveer25/C-Project.git
				if [ $? -ne 0 ] ; then
				git clone https://github.com/Veereshveer25/C-Project.git
				fi
				cd C-Project
				make ABC.exe
				if [ $? -eq 0 ] ; then
				echo " Build is success "
				else
				echo " Build is failed "
				fi
				'''
			}	
		}
		stage ('javaprojects') {
			steps {
				sh '''#!/bin/bash
				            git pull https://github.com/Veereshveer25/java-projects.git
				            if [ $? -ne 0 ] ; then
				            git clone https://github.com/Veereshveer25/java-projects.git
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
	
