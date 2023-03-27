#!groovy
node('master') {

    stage('Git checkout main branch') {
        sh "cd jenkins-stress-test && git pull origin main"
    }

    stage('copy and delete old versions') {
        // sh "rm -rf ${WORKSPACE}@script/*/migrations"
        echo "copy and delete old versions"
    }

    stage('copy to target host'){
        // sh "scp -r ${WORKSPACE}/backend/* root@172.26.129.143:/opt/test-platform/test-platform/backend/"
        echo "copy to target host"
    }

    //stage('Deploy:makemigrations') {
    //    sh "ansible-playbook ${WORKSPACE}/backend/test_platform.yml --tags='makemigrations' -e \"host=172.26.129.143\""
    //}
    //stage('Deploy:migrate') {
    //    sh "ansible-playbook ${WORKSPACE}/backend/test_platform.yml  --tags='migrate' -e \"host=172.26.129.143\""
    //}
    stage('Deploy:restart') {
        // sh "ansible-playbook ${WORKSPACE}/backend/test_platform.yml  --tags='restart' -e \"host=172.26.129.143\""
        echo  "deploy restart test"
    }
    //stage('Deploy:curl_test') {
    //    sh "ansible-playbook ${WORKSPACE}/backend/test_platform.yml  --tags='curl_test' -e \"host=172.26.129.143\""
    //}
}

