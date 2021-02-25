// https://github.com/jenkinsci/git-plugin/blob/master/src/main/java/hudson/plugins/git/GitSCM.java

pipeline {
    agent none
    stages {
        stage ('scm') {
            steps {
                echo "${scm}"
                echo "${scm.gitTool}"
                echo "${scm.GIT_BRANCH}"
            }
        }
    }
}
