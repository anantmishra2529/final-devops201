node {

  stage('Git-CheckOut') {
   git 'https://github.com/anantmishra2529/final-devops201.git'
  }

    
 def project_path="pom.xml"
 
 dir(project_path) {
    
  stage('Maven-Clean') {
   sh label: '', script: 'mvn clean'
  }
    
 stage('Maven-Compile') {
   sh label: '', script: 'mvn compile'
  }
  
   stage('Maven-Install') {
   sh label: '', script: 'mvn install'
  }
  
	
 
  }
}
