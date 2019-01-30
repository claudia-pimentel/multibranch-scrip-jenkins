properties([
    parameters([
        gitParameter(branch: '',
                     branchFilter: 'origin/(.*)',
                     defaultValue: 'master',
                     description: '',
                     name: 'BRANCH',
                     quickFilterEnabled: false,
                     selectedValue: 'NONE',
                     sortMode: 'NONE',
                     tagFilter: '*',
                     type: 'PT_BRANCH')
    ])
])
node { 
    
     git branch: "${params.BRANCH}", url: 'https://github.com/jenkinsci/git-parameter-plugin.git'
  
    stage('Clone repo') {
        //bat "git config core.longpaths true"
        git branch: "${params.BRANCH}" , url: "https://github.com/claudia-pimentel/dotnetcore-testproj"
    }
    stage('Build') { 
        echo "Running build"
        sh 'dotnet test'
                    }
}
