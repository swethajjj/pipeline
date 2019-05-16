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
                                        stage('unittest') {
                                                            steps {
                                                                   echo "runing unittest"
                                                            }
                                        }
                                        stage('integrationtest') {
                                                           agent {
                                                                  docker {
                                                                         reuseNode false
                                                                         image 'ubuntu'
                                                            }
                                                           steps {
                                                                 echo "runnig integraion test"
                                                           }
                                        }
                                    }
                    }
   }
   }
   }
   
        
    
      
     
        
 
    
