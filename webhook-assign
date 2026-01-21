

pipeline{
    agent any

    triggers {
        githubpush()
    }
    tools {
  jdk 'openjdk'
  maven 'maven'
}
stages{
    stage('clone'){
        steps{
            git 'https://github.com/abhitengsal3-hash/java11-examples.git'
        }
    }
    stage('build'){
        steps{
            sh 'mvn clean package'
        }
    }
    stage('archieve'){
        steps{
            archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
        }
    }
}
}
