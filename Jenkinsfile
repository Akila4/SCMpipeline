node{
   stage('SCM Checkout'){
      dir("/var/lib/jenkins/workspace/docker-test/$BUILD_NUMBER"){
       git branch: 'main', url: 'https://github.com/Akila4/SCMpipeline.git'
        }
   }
   stage('Docker File Creation'){
           dir("/var/lib/jenkins/workspace/docker-test/$BUILD_NUMBER"){
		sh '''#!/bin/bash
               ls *.zip | echo  -e FROM registry.hub.docker.com/library/alpine:latest  \'\n\'COPY  $(cat -) ./home > Dockerfile
               cat Dockerfile
           '''
             }
 
   }
}
