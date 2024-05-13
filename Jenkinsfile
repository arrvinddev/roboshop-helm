pipeline{

   agent any 

   stages {

    stage('Clone App Repo'){
        steps{
        dir('APP'){
            git branch: 'main', url: 'https://github.com/arrvinddev/cart'
        }
        }
    }

     stage('Helm Deploy') {
        steps{
        sh 'helm upgrade -i ${component} . APP/values.yaml'
     }
     }

   }
}