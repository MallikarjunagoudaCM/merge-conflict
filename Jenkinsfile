job('PipelineJ3'){
  
  description('This 3rd Pipeline project using Groovy')
  label('Linux_VM')
  
  scm{
    
   github(ownerAndProject='MallikarjunagoudaCM/simple-java-maven-app' , branch='master')
  
  }
  
  steps{
    
    maven{
      
     mavenInstallation('mymave2')
      
      goals('package')
      
    }
    
    shell('java -jar target/*.jar')
    
   
  }
  
  publishers {
        archiveArtifacts('target/*.jar')
        archiveJunit('target/surefire-reports/*.xml')
  }
}
