# Jupyter-Notebook-on-Raspberry-Pi

Follow these instructions to setup Jupyter on Raspberry Pi Zero

Open the terminal of Raspberry Pi and run these commands:

    sudo su -
    apt-get update
    apt-get install python3-matplotlib
    apt-get install python3-scipy
    pip3 install --upgrade pip
    reboot
    sudo pip3 install jupyter
    
To save space and clean up the software packages downloaded for updating Raspberry Pi, follow this command:

    sudo apt-get clean
    
It is always recommended to setup a password for a secure access:

    jupyter notebook password

Now run Jupyter using this command:

    jupyter notebook --no-browser

Open another terminal window on your laptop and follow this command:

    ssh -N -f -L localhost:8888:localhost:8888 pi@raspberrypi.local

Now open any browser and go to this address  http://localhost:8888. You would be asked to enter the Jupyter password that will take you to the folder view. Now you can create a new notebook and start testing the sensors.
