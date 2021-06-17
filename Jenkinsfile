node{
    def name = "DUDE"
    echo "welcome ${name} to AJHUB"
    stage('SCM checkout'){

        git 'https://github.com/devopsmail26/jenkins-first-pipe.git'
    
    }
    stage('Compile Package'){

       sh 'mvn package'
    
    }
}
