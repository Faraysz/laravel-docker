node {

    def PROD_HOST = "127.0.0.1"

    checkout scm

    stage("Build") {
        docker.image('composer:2').inside('-u root') {
            sh '''
            cd src
            rm -f composer.lock
            composer install --ignore-platform-req=ext-intl
            '''
        }
    }

    stage("Testing") {
        docker.image('ubuntu').inside('-u root') {
            sh 'echo "Pipeline Jenkins berhasil dijalankan"'
        }
    }

    stage("Deploy") {
    docker.image('ubuntu').inside('-u root') {
        sh '''
        apt update
        apt install -y openssh-client rsync
        '''
        
        sshagent (credentials: ['ssh-prod']) {
            sh '''
            mkdir -p ~/.ssh
            ssh-keyscan -H 127.0.0.1 >> ~/.ssh/known_hosts

            rsync -avz ./ faraysz@127.0.0.1:/home/faraysz/laravel-deploy
            '''
        }
    }
}

}
