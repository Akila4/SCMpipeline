node{
   stage('SCM Checkout'){
       git branch: 'main', url: 'https://github.com/Akila4/SCMpipeline.git'
        
   }
   stage('Docker File Creation'){
       sh '''#!/bin/bash
              
               ls *.zip | echo  -e FROM registry.hub.docker.com/library/alpine:latest  \'\n\'COPY  $(cat -) ./home > Dockerfile
               cat Dockerfile
           '''
 
   }
}
