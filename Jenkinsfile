node{
    def name = "DUDE"
    echo "welcome ${name} to AJHUB"
    stage('SCM checkout'){

    git 'git@github.com:devopsmail26/my-app.git'
    
    }
    stage('Compile Package'){

    sh 'mvn package'
    
    }
}
