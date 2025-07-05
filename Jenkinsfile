pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                    test -f build/index.html
                '''
            }
        }
    }
}


// pipeline {
//     agent any

//     stages {
//         stage('w/o docker') {
//             steps {
//                 sh '''
//                     echo "Without docker"
//                     ls -la
//                     touch container-no.txt
//                 '''
//             }
//         }

//         stage('w/ docker') {
//             agent {
//                 docker {
//                     image 'node:18-alpine'
//                     reuseNode true
//                 }
//             }
//             steps {
//                 sh '''
//                     ls -la
//                     echo "With docker"
//                     touch container-yes.txt
//                 '''
//             }
//         }
//     }
// }
