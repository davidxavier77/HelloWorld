pipeline {
   agent any

   stages {
      stage('Clean') {
         steps {
            //sh label: 'Change PWD to /tmp/ILServices/',script: 'rm -rf /tmp/ILServices/' 
            cleanWs()
            //sh label: 'Change PWD to /tmp/ILServices/',script: 'mkdir /tmp/ILServices/' 
            //Hi There
            pwd()
            sh label: 'Clone the latest from master Branch' ,script:'git clone https://github.com/davidxavier77/HelloWorld.git' 
            sh label: '', script: 'dotnet publish ./HelloWorld/HelloWorld.csproj'
         }
         post{
             success{
                 echo "Hello World is a success"
             }
             failure{
                 echo "Hello world has failed"
             }
         }
      }

   }
}
