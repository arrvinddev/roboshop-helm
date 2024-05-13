pipeline{

   agent any 

   parameters{
    string(name: 'component', defaultValue: '', description: 'App Component Name')
   }

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
        sh 'helm upgrade -f ${component} . APP/values.yaml'
     }
     }

   }
}