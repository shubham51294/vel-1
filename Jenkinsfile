pipeline {
    agent {
        label {
           label "built-in"
           customWorkspace "/mnt/vel-1"
        }
    }
  stages {
     stage ("1st-stage") {
         steps {
            sh "sudo yum install docker -y"
            sh "systemctl start docker -y"
            sh "docker run -itdp 80:80 --name shubham httpd"
            sh "docker cp index.html shubham:/usr/local/apache2/htdocs"
         }
     }
  }
}
