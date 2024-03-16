# CICDPipeline-html

<h3>Jenkins configurations</h3>
<img width="661" alt="image" src="https://github.com/garimas007/CICDPipeline-html/assets/146625788/e424f102-7f59-4c57-a5d2-d9272e4512d1">
<img width="653" alt="image" src="https://github.com/garimas007/CICDPipeline-html/assets/146625788/1880ec32-7969-4674-8ac8-00bf21a49942">
<h3>Code</h3>
-----------------------------------------------------------------------------------------------------------------------------------------------
pipeline {
    agent any
    environment {
        GIT_URL = 'https://github.com/garimas007/CICDPipeline-html.git'
        GIT_BRANCH = 'main'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('git_repo_cloning') {
            steps {
                git branch: env.GIT_BRANCH , url: env.GIT_URL
            }
        }
        stage('general_cmds') {
            steps {
                echo "This is just to test if its working"
                sh 'pwd'
                sh 'ls -a'
                sh 'whoami'
            }
        }
    }
}
---------------------------------------------------------------------------------------------------------------------------------------------
<h3>Success Deployment on Jenkins</h3>
<img width="780" alt="image" src="https://github.com/garimas007/CICDPipeline-html/assets/146625788/113d79de-f997-44d9-99fd-9f3b0bd196c0">
