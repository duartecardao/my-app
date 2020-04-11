node {
    stage('SCM Checkout'){
        git 'https://github.com/duartecardao/my-app' 
    }
    stage('Compile Package'){
        //Get maven homepath
        def mvnHome = tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
}