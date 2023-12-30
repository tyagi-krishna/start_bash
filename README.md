#!/bin/bash

read -s -p "Enter Password: " entered_password

if [ "$entered_password" -eq 1598 ]; then

	echo ""
	echo "UPDATING..."
	echo "1598" | sudo -S -v
	sudo apt update

	echo "UPGRADING..."
	sudo apt-get upgrade

	echo "AUTO-REMOVE.." 
	sudo apt-get autoremove
	sudo apt-get clean

	echo "Clearing the Window..."
	sleep 3
	clear

	echo "Welcome Krishna Tyagi..."

else
	echo "Wrong Password"
	./start.sh
fi

