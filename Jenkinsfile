node {
    stage('SCM Checkout'){
        git 'https://github.com/duartecardao/my-app' 
    }
    state('Compile Package'){
        sh 'mvn package'
    }
}