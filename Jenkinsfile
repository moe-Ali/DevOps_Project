pipeline {
    
	agent any

	tools {
        maven "maven_3.9.1"
        jdk "JDK_8"
    }

    environment {
        NEXUS_USER = 'admin'
        NEXUS_PASS ='123'
        RELEASE_REPO = 'devops_project-release'
        CENTRAL_REPO ='devops_project-central'
        SNAP_REPO ='devops_project-snapshot'
        NEXUSIP = '192.168.52.132'
        NEXUSPORT= '8081'
        NEXUS_GRP_REPO = 'devops_project-group'
        NEXUS_LOGIN = 'nexuslogin' // nexus login credential name on jenkins
        // NEXUS_VERSION = "nexus3"
        // NEXUS_PROTOCOL = "http"
        // NEXUS_URL = "172.31.40.209:8081"
        // NEXUS_REPOSITORY = "vprofile-release"
	    // NEXUS_REPOGRP_ID    = "vprofile-grp-repo"
        // NEXUS_CREDENTIAL_ID = "nexuslogin"
        // ARTVERSION = "${env.BUILD_ID}"
    }
	
    stages{
        
        stage("BUILD"){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
