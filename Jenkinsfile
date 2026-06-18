pipeline{
agent any
tools{
gradle'gradle'
jdk'jdk17'
}
stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/rheamanjunath/gradle177.git'
}
}
stage('Build'){
steps{
sh'gradle build'
}
}
stage('Test'){
steps{
sh'gradle test'
}
}
stage('Run Application'){
steps{
sh'gradle run'
}
}
}
post{
success{
echo'Build successfull!'
}
failure{
echo'Build failed!'
}
}
}
