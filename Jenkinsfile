node {
    stage ('Checkout from GitHub And Running Ansible Playbook'){
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/ggnanasekaran77/jenkins-ansibleplugin.git']]])
        ansiColor('xterm'){
            ansiblePlaybook(colorized: true, disableHostKeyChecking: true, playbook: 'master.yml')
        }
    }
}