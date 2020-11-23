node
{
    
    stage('CheckoutCOde')
    {
      git credentialsId: 'ea0f21ea-4c9a-411f-8f31-49f825993d6c', url: 'https://github.com/bhaskar0504/node-js-application.git'  
        
    }
    
    stage('Build')
    {
        
     nodejs(nodeJSInstallationName: 'nodejs15.2.1'){
         sh "npm install"  
     } 
    }
    
    stage('ExecuteSonarQubeReport')
    {
        
     nodejs(nodeJSInstallationName: 'nodejs15.2.1'){
         sh "npm run sonar"  
     } 
    }
    
    stage('RunNodeJsApp')
    {
        
     nodejs(nodeJSInstallationName: 'nodejs15.2.1'){
         sh "npm start &"  
     } 
    }
}
