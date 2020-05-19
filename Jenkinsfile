node {
   stage('SCM Checkout') {
       git 'https://github.com/bierbios/maven1.git'
       
   }
   
   stage('compile-package'){
       sh 'mvn package'
   }
}
