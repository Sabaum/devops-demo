@Library("projetas-library") _

PROJECT_NAME = "devops-demo"
PROJECT_VERSION = "${env.BRANCH_NAME}:${BUILD_ID}"

def config = [
        activeBranches: ['dev', 'qa', 'master'],
        name          : PROJECT_NAME,
        image         : PROJECT_NAME,
        stack         : PROJECT_NAME,
        nodeLabel     : 'jenkins-slave.amazon-linux.projetas.com.br',
        key           : "${PROJECT_NAME}:${PROJECT_VERSION}",
        version       : PROJECT_VERSION,
        branch        : env.BRANCH_NAME,
        language      : 'java',
        swarms        : [
                dev   : 'node01.docker.projetas.com.br',
                qa    : 'node01.docker.projetas.com.br',
                master: 'node01.docker.projetas.com.br',
        ]
]

javaPipeline(config)