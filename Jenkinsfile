pipeline {
    agent any

    stages {   
        stage('Production') {
            steps {
                script{
                    sh "cd /var/lib/jenkins/jenkins_parameterized_pipeline"
                    sh "python3 hello.py"
                    for(int i=0;i<5;i++){
                        echo "Level ${i+1}"
                        sleep 1
                    }
                    echo "Test Completed"
                }
            }
        }
        stage("Docker Build"){
            steps {
                echo "Dockerizeing the image..."
                echo "Docker Build is taking place"
                echo "Docker Push"
            }
      }
      stage("Kubernetes Build"){
            steps{
                echo "Kubernetes Build is taking place"
                echo "Kubernetes Push"
            }
      }
      stage("Deployment to Production Server"){
            steps{
                script{
                    echo "Deploying in the Server..."
                    for(int i=0;i<5;i++){
                    echo "Level ${i+1}"
                    sleep 1
                }
                echo "Deployed to Server"
                echo "Build Successful"
                }
            }
        }
        }
    }
