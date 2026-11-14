@Library("Shared") _
pipeline{
    agent { label "wsl"}
    stages{
        
        stage("Code"){
            steps{
                script{
                    code("https://github.com/Elite05-Ur/django-notes-app.git","main")
                }
            }
        }
        stage("Build"){
            steps{
                script{
                   build("notes-app","latest","omaan490")
                }
            }
        }
        stage("Push to DockerHub"){
            steps{
                script{
                    push("notes-app","latest","omaan490")
                }
            }
        }
        stage("Deploy"){
            steps{
                script{
                    deploy()
                }
            }
        }
    }
}
