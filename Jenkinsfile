node {

  stage('Git-CheckOut') {
   git 'https://github.com/devops311/user-project-application.git'
  }
    stage('Trufflehog Inspection')
    {
    sh 'docker run gesellix/trufflehog --json https://github.com/devops311/user-project-application.git > trufflehogReport'
    sh 'cat trufflehogReport'
    }
    
 def project_path="application-code/code/userproject"
 
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
