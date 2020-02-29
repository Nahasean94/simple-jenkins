node('master'){
    stage("Fetch Source Code"){
        git 'https://github.com/Nahasean94/simple-jenkins.git'
    }
    
   
        printMessage('Running pipeline')
        
        stage("Testing"){
            sh 'python test_functions.py'
        }
        stage("Deployment"){
            if(env.BRANCH_NAME=='master'){
                printMessage('Deploying the master branch')
            }else{
                printMessage('No deployment configured for this branch')
            }
        }
        printMessage('Pipeline Complete')
 
}

def printMessage(message){
    echo "${message}"
}
