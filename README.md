# air-conditioner

STEP 1: Install docker

	use the comands bellow:

	```
	sudo apt update
	```

	```
	sudo apt install apt-transport-https ca-certificates curl software-properties-common
	```

	```
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add 
	```

	```
	sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
	```

	```
	sudo apt update
	```

	```
	apt-cache policy docker-ce
	```

	```
	sudo apt install docker-ce
	```




STEP 2 (optional): Use docker without sudo
	
	use the comands bellow:

	```
	sudo usermod -aG docker {USER}
	```

	```
	su - {USER}
	```

STEP 3: