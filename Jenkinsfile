pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh '''
                pwd
                #git clone "https://github.com/Iam-7hills/katalon.git" katalongit
                cd /var/lib/jenkins/workspace/katalonpipeline/katalon
                
                xvfb-run -s ":99 -screen 0 1024x768x24" -e /tmp/xvfb.log /home/jenkins/.katalon/9.0.0/Katalon_Studio_Engine_Linux_64-9.0.0/katalonc -noSplash  -runMode=console  -projectPath="/var/lib/jenkins/workspace/katalonpipeline/katalon/KatalonDemo.prj" -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/testsuitekatalon" -apiKey="<api-key>" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true
                
                '''

            }

        }

    }

}

### -projectPath="/var/lib/jenkins/workspace/katalondemotest/KatalonDemUserAdd.prj" -retry=0 -testSuitePath="Test Suites/tesuite" -browserType="Chrome" -executionProfile="default" -apiKey="<API-KEY>" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true
