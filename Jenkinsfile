pipeline{
agent any
stages{
stage('scm'){
steps{
checkout([$class: 'GitSCM', branches: [[name: '*/feat01']], extensions: [], userRemoteConfigs: [[credentialsId: 'c291bbd5-bd02-4f7d-a544-68e6d1bcb5fd', url: 'https://github.com/vidufirstorg/mavenrepo.git']]])
}
}
stage('build'){
steps{
sh 'mvn package'
}
}
}
}
