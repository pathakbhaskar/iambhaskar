node {

stage 'Install apache'
	sh 'sudo apt install apache2 -y'
stage 'Start Apache'
	sh 'sudo service apache2 start'
stage 'Git checkout'
	git branch: 'main', url: 'https://github.com/pathakbhaskar/iambhaskar.git'
stage 'Deploy the application'
	sh 'sudo cp -R * /var/www/html/'
}