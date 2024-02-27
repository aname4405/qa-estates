pipeline {
    agent any    
    stages {
        stage('Build') {
            steps {                
                bat 'npm install'
                bat 'npm start'
            }
        }
        // stage('Deploy') {
        //     steps {
        //         a: {
        //             bat 'npm run preview'
        //         }
        //         b: {
        //             bat 'npx json-server db.json'
        //         }                
        //     }
        // }
    }
}
