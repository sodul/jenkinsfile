// https://github.com/jenkinsci/git-plugin/blob/master/src/main/java/hudson/plugins/git/GitSCM.java

pipeline {
    agent none
    stages {
        stage ('scm') {
            steps {
                script {
                    echo "${scm}"   // hudson.plugins.git.GitSCM@49667ef7
                    echo "${scm.dump()}"
                    echo "${scm.gitTool}"   // null
                    echo "${scm.GIT_BRANCH}"    // GIT_BRANCH
                    echo "${scm.branches}"  // [${BRANCH}]
                    echo "${scm.remoteRepositories}"    // [org.eclipse.jgit.transport.RemoteConfig@54e2228a]
                    echo "${scm.getRepositories()}"     //
                
                    remote_repos = scm.remoteRepositories
                    first_repo = remote_repos[0]
                    echo "${first_repo.getName()}"
                    echo "${first_repo.getURIs()}"
                }
            }
        }
    }
}
