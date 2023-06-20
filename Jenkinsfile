pipeline {
    agent {
        label "ubuntu-agent"
    }
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
    stages {
        
        stage("clean workspace") {
            steps {
                cleanWs()
            }
        }
    
        stage("checkout from SCM") {
            steps {
                git branch: 'main', credentialsId: 'github', url: "https://github.com/sadobin/complete-prodcution-e2e-pipeline"
            }
        }
    }
}
