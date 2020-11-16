 pipeline {
        agent any
                stages {
                       stage('one') {
                               steps {
                                    echo "hi this is swetha"
                               }
                       }
                       stage('two') {
                               steps {
                                      input('do u want to proceed?')
                               }
                      }
                      stage('three') {
                              when {
                                      not {
                                             branch "master"
                                     }
                             } 
                             steps {
                                    echo "hello"
                             }
                      }
                      stage('four') {
                                      parallel {
                                           stage('unit test') {
                                                              steps {
                                                                   echo "runing unit tests"
                                                              }
                                           } 
                                           stage('integration test') {
                                                              agent {
                                                                     docker {
                                                                             reuseNode false
                                                                             image 'ubuntu'
                                                                      }
                                                              }
                                                              steps {
                                                                    echo "runnig integraion test"
                                                              }
                                           }
                                    }
                      }
                }
   }
        
    
      
     
        
 
    
