node('UBUNTU_NODE1'){
    stage('install apache') {
        sh 'sudo apt update && sudo apt install apache2 -y'
    }
    stage('install php') {
        sh 'sudo apt install php -y'
    }
    stage('create file') {
        sh 'sudo touch /var/www/html/info.php'
        sh 'sudo chown ubuntu /var/www/html/info.php'
        sh 'sudo chgrp ubuntu /var/www/html/info.php'
    }
    stage('writefile'){
        writeFile file: '/var/www/html/info.php', 
                  text: '''<?php
                            phpinfo();
                                ?>'''
   }
}

