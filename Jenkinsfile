node { 
  
    stage ('Save Branch'){
      sh 'git branch > BRANCH_TEST'    
    }
    
  for ((cont=0; cont<${#BRANCH_TEST[@]}; cont++));
    do
    stage('Clone repo') {
        //bat "git config core.longpaths true"
        git branch: "${BRANCH_TEST}" , url: "https://github.com/claudia-pimentel/dotnetcore-testproj"
    }
    stage('Build') { 
        echo "Running build"
        sh 'dotnet test'
                    }
}
