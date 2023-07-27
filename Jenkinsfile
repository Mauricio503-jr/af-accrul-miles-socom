#!groovy
properties([disableConcurrentBuilds(), gitLabConnection(''), pipelineTriggers([])])

env.DEFAULT_CONFIG_REPO='https://git.lifemiles.net/LM-DevOps/pl-product-pipeline.git'
env.DEFAULT_CONFIG_BRANCH='master'
env.DEFAULT_CONFIG_PATH_BACK_END='Jenkinsfile-iac'

def giturl = // "https://git.lifemiles.net/lm-accounting-financial/af-redeemed-miles-on-flights-report.git"

def Jenkinsfile = fileLoader.fromGit(env.DEFAULT_CONFIG_PATH_BACK_END,env.DEFAULT_CONFIG_REPO, env.DEFAULT_CONFIG_BRANCH, 'Jenkins-Gitlab', '')

Jenkinsfile.start_pipeline(giturl)