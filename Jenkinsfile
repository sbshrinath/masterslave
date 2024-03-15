pipeline {
       agent {
            label 'slave1'
             }

     stages {
         stage('Checkout') {
             steps {
                     checkout scm
                   }
                           }
         stage('Build') {
             steps {
                     sh '/home/harry/workdir/apache-maven-3.9.6/bin/mvn install'
                   }
                        }
         stage('Deploy') {
             steps {
                     sh 'cp target/masterslave.war /home/harry/workdir/apache-tomcat-9.0.86/webapps'
                   }
                         }

            }
         }
