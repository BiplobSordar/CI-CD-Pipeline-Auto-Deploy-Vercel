// pipeline {
//     agent any

//     environment {
//         VERCEL_TOKEN = credentials('vercel_token')
//     }

//     stages {
//         stage('Install') {
//             steps {
//                 bat 'npm install'
//             }
//         }
//         stage('Test') {
//             steps {
//                 echo 'Skipping tests - no test script found'
//             }
//         }
//         stage('Build') {
//             steps {
//                 bat 'npm run build'
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 bat 'npx vercel --prod --yes --token=%VERCEL_TOKEN%'
//             }
//         }
//     }
// }

pipeline {
    agent any

    environment {
        VERCEL_TOKEN = credentials('vercel_token')
    }

    stages{
        stage('Install'){
            bat 'npm install'
        }
    }
    stages{
        stage('Test'){ 
           echo 'Skipping tests -no test script found'
        }
    }
    stages{
        stage('Build'){
            bat 'npm run build'
        }
    }
    stages{
        stage('Deploy'){
            bat 'npx vercel --prod --yes --token=%VERCEL_TOKEN'
        }
    }
}