node() {
    try {
        stage('checkout public repo') {
            folder = new File("$WORKSPACE/.git")
            if (folder.exists())
            {
               println "Found .git folder. Clearing it.."
               sh'git clean -fxd'
            }
            checkout scm
        }
        stage('deploy') {
           sh "echo Deploy Successful"
        }
     }
    catch (err) {
        currentBuild.result = "FAILURE"
        throw err
    }
}
