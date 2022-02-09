node{
   stage('SCM Checkout'){
      dir("/var/lib/jenkins/workspace/docker-test/$BUILD_NUMBER"){
       git branch: 'main', url: 'https://github.com/Akila4/SCMpipeline.git'
        }
   }
   stage('Docker File Creation'){
       sh '''#!/bin/bash
              dir("/var/lib/jenkins/workspace/docker-test/$BUILD_NUMBER"){
               ls *.zip | echo  -e FROM registry.hub.docker.com/library/alpine:latest  \'\n\'COPY  $(cat -) ./home > Dockerfile
               cat Dockerfile
           '''
             }
 
   }
}
