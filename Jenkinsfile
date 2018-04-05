pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
                cleanWs()
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], browser: [$class: 'GithubWeb', repoUrl: 'https://github.com/alikbm/building-java-libraries'], 
                doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/alikbm/building-java-libraries.git']]]) 
                sh './gradlew clean build'
                    
                    
                }
    
        }
        stage('Test'){
            steps {
                sh 'echo '
                //junit 'reports/**/*.xml' 
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo '
            }
        }
    }
}
