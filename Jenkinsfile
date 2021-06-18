node{
    def name = "DUDE"
    echo "welcome ${name} to AJHUB"
    stage('SCM checkout'){
        
        git 'https://github.com/devopsmail26/my-app.git'
    }
    stage('Compile Package'){
        
        def mvnHome = tool name: 'maven-1', type: 'maven'
        
        sh "${mvnHome}/bin/mvn package"
    }
}
