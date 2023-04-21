pipeline{
    agent any
    stages{
        stage("git checkout")
        {
            steps{
                    git url: 'https://github.com/tinkusaini13/Docker-Compose-for-CI-CD-Pipeline.git', branch: 'main'
                    sh  "cd /var/lib/jenkins/workspace/demo"
                    sh "git clone https://github.com/tinkusaini13/Docker-Compose-for-CI-CD-Pipeline.git "
                    
                 }
          }
        stage("List files")
        {
            steps{
                sh "ls -ltr"
            }
        }
       
        stage("create docker container sonar")
        {
            steps{
                sh " docker-compose up -d"
            }   
            }
         stage("verify web server running or not ")
        {
            steps{
                sh "docker-compose ps"
                
            }   
            }
    }
}
