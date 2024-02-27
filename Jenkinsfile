pipeline {
    agent any    
    stages {
        stage('Build') {
            steps {                
                bat 'npm install'
                }
        }
        stage('Deploy') {
            steps {
                parallel (
                    'npm start': {
                        bat 'npm start'
                    },
                    'npm run server': {
                        bat 'npx json-server --watch db.json'
                    }
                )                    
            }             
                   
        }
    }
}
