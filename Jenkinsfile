#!/usr/bin/groovy
/* -*- mode: groovy; -*-
 * CI-RT default Jenkinsfile
 */

pipeline {
	agent any;

	options {
		timestamps()
	}

	stages {
		stage('trigger ci-rt scheduler') {
			steps {
				build job: 'cirt-scheduler', parameters: [
				      string(name: 'TESTDESCRIPTION_REPO', value: 'https://github.com/ci-rt/test-description.git'),
				      string(name: 'GUI_TESTDESCR_BRANCH', value: 'master'),
				      string(name: 'GUI_DB_HOSTNAME', value: 'localhost:5432'),
				      string(name: 'GUI_CIRT_LIB_VERSION', value: 'master')]
			}
		}
	}
}
