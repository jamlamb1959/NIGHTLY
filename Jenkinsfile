#!/usr/bin/env groovy

pipeline {
  agent any
  stages {
	stage('Install Scripts') {
		parallel {
			stage('on Khadas') {
				agent { label 'khadas' }
				steps {
					sh '''
cd sh
sudo -S install * /usr/local/bin <<DONE
cutekids
DONE
./bld.setup
'''
				}
			}
			stage('on oci') {
				agent { label 'oci' }
				steps {
					sh '''
cd sh
sudo -S install * /usr/local/bin <<DONE
cutekids
DONE
./bld.setup
'''
				}
			}
			stage('on tailgate') {
			agent { label 'tailgate' }
			steps {
				sh '''
cd sh
sudo -S install * /usr/local/bin <<DONE
cutekids
DONE
./bld.setup
'''
			}
			}
			stage('on 3d') {
			agent { label '3d' }
			steps {
				sh '''
cd sh
sudo -S install * /usr/local/bin <<DONE
cutekids
DONE
./bld.setup
'''
			}
			}
			stage('on geek') {
			agent { label 'geek' }
			steps {
				sh '''
cd sh
which sudo
sudo which install
sudo -S install * /usr/local/bin <<DONE
cutekids
DONE
./bld.setup
'''
			}
			}
			stage('on ubu-23-10-bld') {
			agent { label 'ubu-23-10-bld' }
			steps {
				sh '''
cd sh
which sudo
sudo which install
sudo -S install * /usr/local/bin <<DONE
cutekids
DONE
./bld.setup
'''
			}
			}
		}
	}
    }
}
