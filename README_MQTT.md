Project for the 2019 TUES internship in Astea Solutions. The goal is to automate controll over an AC with Home Assistant, running on a Docker image, communicating with the device via Mosquitto broker.

#Commands STEP 1: Install Mosquitto

Use the comands bellow:

sudo apt update

sudo apt install mosquitto

sudo apt install mosquitto-clients

sudo apt update

STEP 2 (optional): Use Mosquitto without sudo

Use the comands bellow:

sudo usermod -aG mosquitto {USER}

su - {USER}

STEP 3: Configure your broker

Open configuration.yaml in your docker folder directory

Enter your mqtt(mosquitto) config:
________________________________________________________
mqtt:
  broker: <your IP address>
  username: username
  password: password
________________________________________________________

STEP 4: Subscribe broker(mosquitto) to docker

Use the command bellow:

mosquitto_sub -h <host> -p <port> -t <topic> -u <user> -P <password>

If you have already used the name "home-assistant" for docker container, you could set it to anything unused.