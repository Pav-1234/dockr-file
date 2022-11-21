pipeline
agent any
stages {
stage ('checkout') {
steps {
echo 'scm checkout'
sh "pwd"
}
}
stage ('clean container') {
steps {
echo 'remove the container'
sh "pwd"
sh "chmod 700 (env ,workspacce)"
sh "docker ps-a"
sh "docker system prune --all --volumes"
}
}
stage ('Build') {
steps {
sh "pwd"
sh "cd python"
sh "cd /var/lib/jenkins/workspace/python
}
}
stage ('Run')" {
steps {
sh "docker run -itd python ".
sh "docker run -itd -p 1010:4000 image name 
}
}
stage ('complete') {
steps {
sh "echo container is running"
}
}
}
}
