// https://github.com/jenkinsci/git-plugin/blob/master/src/main/java/hudson/plugins/git/GitSCM.java

pipeline {
    agent none
    stages {
        stage ('scm') {
            steps {
                echo "${scm}"   // hudson.plugins.git.GitSCM@49667ef7
                echo "${scm.gitTool}"   // null
                echo "${scm.GIT_BRANCH}"    // GIT_BRANCH
                echo "${scm.branches}"  // [${BRANCH}]
                echo "${scm.remoteRepositories}"    // 
                
            }
        }
    }
}
