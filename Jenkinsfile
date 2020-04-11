node {
    stage('SCM Checkout'){
        git 'https://github.com/duartecardao/my-app' 
    }
    stage('Compile Package'){
        sh 'mvn package'
    }
}