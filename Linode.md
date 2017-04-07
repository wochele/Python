# Linode

- [Start a new ubuntu server](#server)
- [Running Django](#django)

<a name="server"></a>
## Start a new ubuntu server


```
# Install updates
> apt-get update && apt-get upgrade

# Set hostname
> echo "<hostname>" > /etc/hostname
> hostname -F /etc/hostname
> vi /etc/hosts
  Add the line: 
  <ip address>    <hostname>

# Set timezone
> dpkg-reconfigure tzdata

# Check Python Versions
> python -V
> python3 -V

# Install pip
> apt-get install -y python3-pip

# Install dev tools
> apt-get install build-essential libssl-dev libffi-dev python3-dev

# Install virtual environment
> apt-get install -y python3-venv

# Use virtual environment
> pyvenv my_env    # Create a virtual env
> source my_env/bin/activate   # Activate the env
```

Note: Within the virtual environment, you can use the command python instead of python3, and pipinstead of pip3 if you would prefer. If you use Python 3 on your machine outside of an environment, you will need to use the python3 and pip3 commands exclusively. 

https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-programming-environment-on-an-ubuntu-16-04-server

<a name="django"></a>
## Running Django

- Make sure the ip address of the server is added to ALLOWED_HOSTS in settings.py

`ALLOWED_HOSTS = ['50.116.19.8']`

`> ./manage.py runserver 0.0.0.0:8000`
