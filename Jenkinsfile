node {
 checkout scm

 stage("Build"){
  docker.image('shippingdocker/php-composer:2.9').inside('-u root') {
   sh 'rm composer.lock'
   sh 'composer install'
  }
 }

 docker.image('ubuntu').inside('-u root') {
  sh 'echo "Ini adalah test"'
 }
}
