# Invoice_Management_System

Setup  

Using Python virtualenv

Prerequisites

You have a working installation of Python 2.7.*

You can install software on your system.

You can create and activate Python virtual environments. Create a Python virtual environment somewhere on your system and activate it your shell prompt should look something like this:
(env)[username@computer pwd]$

Clone this repository into the directory of your choice like so:

$ git clone https://github.com/Filipo-Dev/Invoice_Management_System.git

cd into the project root directory and install the needed requirements.

NB: Ensure that your virtual environment is activated.

$ cd Invoice-Management-System/

$ pip install -r requirements.txt

You will need to set the following environment variables. Open your .bashrc file

$ vim ~/.bashrc
and add the following:

export SECRET_KEY='{secure secret key}'

export NAME='{database name}'

export USER='{user}'

export PASSWORD='{user password}'

export HOST='{database host ip}'

export PORT='{database port}'

Setup the database by running the following.


$ python manage.py migrate

Running

When all is okay, you can start the local development server.


$ python manage.py runserver

Visit localhost:8000 in your browser.


Using Docker

You can build and run the app using Docker containers. This requires minimal setup.


Prerequisites

Make sure you have Docker a Docker-compose installed. Follow the URLs below to install for the appropriate system.


Installing docker-compose

Installing docker


After installation you can verify that it is installed by running


$ sudo docker version

It should display something like this if successful:


Client:

 Version:           18.06.1-ce
	
 API version:       1.38
	
 Go version:        go1.10.3
	
 Git commit:        e68fc7a
	
 Built:             Tue Aug 21 17:25:13 2018
	
 OS/Arch:           linux/amd64
	
 Experimental:      false
	

Server:

 Engine:
	
  Version:          18.06.1-ce
		
  API version:      1.38 (minimum version 1.12)
		
  Go version:       go1.10.3
		
  Git commit:       e68fc7a
		
  Built:            Tue Aug 21 17:27:37 2018
		
  OS/Arch:          linux/amd64
		
  Experimental:     false
		
Now clone the repository and cd into deploy directory inside the root of the project.


$ cd Invoice-Management-System

Now run to build and start running the containers.


$ docker-compose build --no-cache

$ docker-compose up --no-start --force-recreate

$ docker-compose start

Then visit 127.0.0.1 in your browser.

Supervisor will be running on 127.0.0.1:9001. If prompted for username and password, use the following:


username: lipo

password: lipo

Features

Testing

Run the commands below to test the project and view the coverage.


$ coverage run --source='.' manage.py test

$ coverage report -m

To exclude the virtualenv folder do the following:


$ coverage run --omit ve  --source="." manage.py  test

In the above example "ve" is the name of the virtualenv.


Contributing

Fork it (https://github.com/Filipo-Dev/Invoice_Management_System.git)

Create your feature branch (git checkout -b feature/fooBar)

Commit your changes (git commit -am 'Add some fooBar')

Push to the branch (git push origin feature/fooBar)

Create a new Pull Request

