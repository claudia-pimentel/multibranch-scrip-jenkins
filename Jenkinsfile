node { 
  
    stage ('Save Branches'){
    sh '$BRANCH='Git branch''    
    }
    
    stage('Clone repo') {
        //bat "git config core.longpaths true"
        git branch: "${BRANCH}" , url: "https://github.com/claudia-pimentel/dotnetcore-testproj"
    }
    stage('Build') { 
        echo "Running build"
        sh 'dotnet test'
                    }
}
