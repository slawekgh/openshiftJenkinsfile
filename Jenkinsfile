try {
   timeout(time: 20, unit: 'MINUTES') {
      node(slave) {
          stage('build') {
            openshiftBuild(buildConfig: 'openshift-bc-simple', showBuildLogs: 'true')
          }
         
          stage('ship') {
            openshiftBuild(buildConfig: 'openshift-bc-simple', showBuildLogs: 'true')
          }
         
          stage('run') {
            openshiftBuild(buildConfig: 'openshift-bc-simple', showBuildLogs: 'true')
          }
          stage('deploy') {
            //openshiftDeploy(deploymentConfig: 'slawekdeploj')
            //openshiftScale(deploymentConfig: 'slawekdeploj',replicaCount: '5')
             
          }
        }
   }
} catch (err) {
   echo "in catch block"
   echo "Caught: ${err}"
   currentBuild.result = 'FAILURE'
   throw err
}          
