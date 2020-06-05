pipeline{
agent any
stages{
 
 stage('checkout'){
steps{
script{
env.PATH="C:/Users/Leena_Desu/Downloads/apache-maven-3.6.3-bin/apache-maven-3.6.3/bin;c:\\Windows\\System32"
}
checkout([$class: 'GitSCM', branches: [[name: '*/Project/unitTest']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '929915bb-9ad6-4f1f-b466-41c055b0f1df', url: 'https://git.epam.com/Leena_Desu/allcdpprojects.git']]])
}
}
stage('build'){
steps{
    dir('junithometask') {
  bat label: '', script: 'mvn package'
}
}
}
stage('post build')
{
steps{
    junit 'junithometask/target/surefire-reports/*.xml'}
}
stage('notify')
{
steps{
    emailext body: 'build success', subject: 'jenkins', to: 'desuleenarteddy547@gmail.com'
}
}
}

}