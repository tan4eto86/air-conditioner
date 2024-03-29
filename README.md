# air-conditioner

Project for the 2019 TUES internship in Astea Solutions. The goal is to automate controll over an AC with Home Assistant, running on a Docker image, communicating with the device via Mosquitto broker. 

# Commands
## STEP 1: Install docker

Use the comands bellow:

	
	sudo apt update

	sudo apt install apt-transport-https ca-certificates curl software-properties-common

	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add 

	sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"

	sudo apt update

	apt-cache policy docker-ce
	
	sudo apt install docker-ce
	




## STEP 2 (optional): Use docker without sudo
	
Use the comands bellow:

	sudo usermod -aG docker {USER}

	su - {USER}

## STEP 3: Run docker image with Home Assistant
	
Use the command bellow:

	docker run --init -d --name="home-assistant" --restar on-failure -v /{PATH_TO_DIRECTORY}/air-conditioner/docker:/config -p 8123:8123 homeassistant/home-assistant

If you have already used the name "home-assistant" for docker container, you could set it to anything unused.

# Sources

## Decoding the AC remote commands

https://github.com/ToniA/Raw-IR-decoder-for-Arduino/blob/master/Fujitsu.cpp

We used this repository to understand how the AC is decoding the hexadecimal numbers it recieves as commands from the remote.
