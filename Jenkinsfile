// https://github.com/jenkinsci/git-plugin/blob/master/src/main/java/hudson/plugins/git/GitSCM.java

pipeline {
    agent none
    stages {
        stage ('scm') {
            steps {
                script {
                    echo "scm: ${scm}"   // hudson.plugins.git.GitSCM@49667ef7
                    echo "scm.dump(): ${scm.dump()}"
                    echo "scm.gitTool: ${scm.gitTool}"   // null
                    echo "scm.GIT_BRANCH: ${scm.GIT_BRANCH}"    // GIT_BRANCH
                    echo "scm.branches: ${scm.branches}"  // [${BRANCH}]
                    echo "scm.remoteRepositories: ${scm.remoteRepositories}"    // [org.eclipse.jgit.transport.RemoteConfig@54e2228a]
                    echo "scm.getRepositories: ${scm.getRepositories()}"     //
                    echo "scm.branches.dump(): ${scm.branches.dump()}"     //
                    scmBranch = scm.branches[0].name
                    remote_repos = scm.remoteRepositories
                    echo "remote_repos = scm.remoteRepositories"
                    first_repo = remote_repos[0]
                    echo "first_repo = remote_repos[0]"
                    echo "${branch}"
                    echo "first_repo.getName(): ${first_repo.getName()}"
                    echo "first_repo.getURIs(): ${first_repo.getURIs()}"
                    def engine = new groovy.text.SimpleTemplateEngine() //template engine
                    def template = engine.createTemplate(scmBranch).make([:]<<params) //convert source string to template - making a copy of params because its immutability is freaking out the template engine
                    String branch = template // convert template to string
                    echo "Branch is: ${branch}"
                }
            }
        }
    }
}
