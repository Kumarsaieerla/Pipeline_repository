node('node_1')
{
    def mavenHome = tool name: "maven3.9.6"
    stage('CodeCheckout')
    {
    git branch: 'development', credentialsId: '174d702a-0690-4895-9aa7-e612464046b8', url: 'https://github.com/Kumarsaieerla/maven_appns.git'

    }
    stage('Build')
    {
    sh "${mavenHome}/bin/mvn clean package"
    }
    stage('ExecuteSonar')
    {
    sh "${mavenHome}/bin/mvn sonar:sonar"
    }
    
}
