node('sonar'){
stage('clone') {
sh 'git clone git@github.com:vinodopsdev/Pipeline-1.git'
}
stage('source code') {
sh 'cd Pipeline-1'
}
stage('stage1') {
sh 'mvn clean package'
}
stage('stage2') {
sh 'mvn sonar:sonar'
}
stage('stage3') {
sh 'mvn deploy'
}
}
