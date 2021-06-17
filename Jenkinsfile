node{
    def name = "DUDE"
    echo "welcome ${name} to AJHUB"
    stage('SCM checkout'){
        tool name: 'maven-1', type: 'maven'
        git 'https://github.com/devopsmail26/my-app.git'
    }
    stage('Compile Package'){
        sh 'mvn package'
    }
}
