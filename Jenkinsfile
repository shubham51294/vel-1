pipeline {
    agent {
        label {
           label "dev"
           customWorkspace "/mnt/vel-2"
        }
    }
  stages {
     stage ("1st-stage") {
         steps {
            sh "sudo yum install docker -y"
            sh "systemctl start docker -y"
            sh "docker run -itdp 80:90 --name shubham httpd"
            sh "docker cp index.html shubham:/usr/local/apache2/htdocs"
         }
     }
  }
}
