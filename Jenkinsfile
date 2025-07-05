pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
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
