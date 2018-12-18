node{
    stage('SCM Checkout'){
        git 'https://github.com/ramudevops123/mvnproj.git'
    }
    stage('Clean-Stage'){
        //Get maven homepath
        def M2_HOME = tool name: 'M2_HOME', type: 'maven'
        sh "${M2_HOME}/bin/mvn clean"
    }
    stage('Package-Stage'){
        
        sh "${M2_HOME}/bin/mvn package"
    }
    stage('Install-Stage'){
        
        sh "${M2_HOME}/bin/mvn install"
    }
    stage('Deploy-Stage'){
        
        sh "${M2_HOME}/bin/mvn deploy"
    }
}
