pipeline {
    agent any
    tools {
        maven "MAVEN3.9"
        jdk "JDK17"
    }
    
    environment {
        SNAP_REPO = 'company-snapshot'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'Maveric@123'
		RELEASE_REPO = 'company-release'
		CENTRAL_REPO = 'com-maven-central'
		NEXUSIP = '192.168.56.15'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'com-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
        SONARSERVER = 'sonarserver'
        SONARSCANNER = 'sonarscanner'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}