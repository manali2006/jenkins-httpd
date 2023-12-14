pipeline {
agent {
label {
label "built-in"
customWorkspace "/mnt/wsp-1/"
}
}
stages {
stage ("delete") {
steps {
sh "rm -rf /mnt/wsp-1/jenkins-httpd"
}
}
stage ("httpd") {
steps {
sh "yum install httpd -y"
sh "service httpd start"
}
}
stage (deploy") {
steps {
sh "cp -r /mnt/wsp-1/jenkins-httpd/index.html /var/www/html"
sh "chmod -R 777 /var/www/html/index.html"
}
}
}
}
