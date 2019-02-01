node { 
  
    stage ('Save Branch'){
      def BRANCH_TEST = [];
      git branch > allbranches;
      allbranches.split(' ').each{BRANCH_TEST.add}
                          }
  
     stage('Clone repo') {
        //bat "git config core.longpaths true"
        git branch: "BRANCH_TEST.each" , url: "https://github.com/claudia-pimentel/dotnetcore-testproj"
    }
    stage('Build') { 
        echo "Running build"
        sh 'dotnet test'
                    }
}
