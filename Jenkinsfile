node('sonar'){
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
