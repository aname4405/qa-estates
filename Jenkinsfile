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
                    'npm run server': {
                        bat 'npx json-server --watch db.json'
                    },
                                        'npm start': {
                        bat 'npm start'
                    }
                )                    
            }             
                   
        }
    }
}
