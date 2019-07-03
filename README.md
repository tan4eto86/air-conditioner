# air-conditioner

STEP 1: Install docker<br\>
	use the comands bellow:<br\>
	```
	sudo apt update
	```<br\>
	```
	sudo apt install apt-transport-https ca-certificates curl software-properties-common
	```<br\>
	```
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
	```<br\>
	```
	sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
	```<br\>
	```
	sudo apt update
	```<br\>
	```
	apt-cache policy docker-ce
	```<br\>
	```
	sudo apt install docker-ce
	```
<br\><br\>



STEP 2 (optional): Use docker without sudo<br\>
	use the comands bellow:<br\>
	```
	sudo usermod -aG docker {USER}
	```<br\>
	```
	su - {USER}
	```
<br\><br\>

STEP 3: