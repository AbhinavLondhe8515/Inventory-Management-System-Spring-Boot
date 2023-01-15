

node(){

 try {
        stage('Checkout Code'){
          checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'gitcreds', url: 'https://github.com/AbhinavLondhe8515/Inventory-Management-System-Spring-Boot.git']])
        }

 

 

        stage('Maven Build'){
            sh "mvn clean install"
        }

 

 

        stage('Test Cases Execution'){
            echo "The test is SUCCESSFUL"
        }


    }
    catch (Exception e){
        currentBuild.result = 'FAILURE'
        echo currentBuild.currentResult
    }
}
