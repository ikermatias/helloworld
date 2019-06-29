#!groovy

node {
   stage 'Checkout'
	checkout scm
   
   stage 'Set registry'
	sh 'npm config set registry http://registry.npmjs.org/' 

   stage 'Setup'
	sh 'npm install'

   stage 'Mocha test'
	sh './node_modules/mocha/bin/mocha'

   stage 'Cleanup'
	echo 'prune and cleanup'
	sh 'npm prune'
	sh 'rm node_modules -rf'
 }
