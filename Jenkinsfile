// pipeline laravel boiler plate

pipeline {
	agent any
	environment {
			TARGET_DIR = "C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\JmeterDimas"
	}
	stages {
		stage('Scan with JMeter'){
		steps {
				echo "scan with JMETER"

				dir ("${TARGET_DIR}") {
//					bat 'scancentral -url http://192.168.1.186:8080/scancentral-ctrl start -bt mvn -upload -versionid 10002 -uptoken f2a08e91-3e45-4d1f-963a-0efde16f1a31'
					bat 'jmeter -n -t "1. Load BlazeDemo 10.jmx"'
				}
			}
		}
		stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }
	}	
}