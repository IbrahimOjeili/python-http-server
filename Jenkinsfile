node {

    stage ("clone repository") {

        git branch: 'master', credentialsId: 'github', url: 'https://github.com/IbrahimOjeili/python-http-server'

    }

    stage ("copy python script and folder") {

        sh "sudo cp -r app.py public/ /home/python"

        sh "sudo chown -R python:python /home/python"

    }

    stage ("restart service") {

        sh "sudo systemctl restart python"

    }

}
