node {



stage('Clone Repository')


{

checkout scm

}

stage('Show me the files'){


sh "ls -l"


}

stage('Build docker image'){

sh "docker build -t exams:latest ."

}

stage('Docker login to hub and push the image'){
sh "docker login -u 'maoromo' -p 'Learn@Jenkins1' "
sh "docker tag exams:latest maoromo/exams:latest"
sh "docker push maoromo/exams:latest"

}

stage('docker run the image'){
sh "docker run -d -p 4546:80/tcp devops-exams:latest"
stage('Apply changes to the environment') {
sh "ls -l"

}

}
