pipeline {
    agent any

    stages {
        stage('scm') {
            steps {
               git changelog: false, poll: false, url: 'https://github.com/arunsinghrawat123/ModSecurity.git'
            }
        }
    
    stage('OWASP Depedency') {
            steps {
               dependencyCheck additionalArguments: '--format HTML', odcInstallation: 'OWASP Dependency Check'
            }
        }
    }
}
        
