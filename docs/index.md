# Piwigo Container Service for Podman

## Pre-Requisites 
**NOTE:** This is tested and verified to work if the same versions listed below are used, otherwise, things may not be exactly the same!
1. AlmaLinux OS == 9.3 
2. Latest version of Podman installed
3. The latest version of podman-compose installed (docker-compose)
4. The latest podman-plugins installed
5. SELinux is *Enabled* (We do not disable it just because its tricky, its an important security feature!)

## Requirements
1. A user to the AlmaLinux server with sudo permissions to run the install script

## Process
Pull the install script from your AlmaLinux Host (the script must be run in sudo mode!) in your current working directory:
```SHELL
curl https://github.com/mattbuske/piwigo-container-service/blob/main/setup/install.sh > ./install.sh
# Do we need to update the script to be executable? - Test this
sudo ./install.sh
```

The Script will:

1. Check for necessary pre-requisites
    1. If not installed/configured to minimum, exit.
2. Look for the expected file structure
    3. If it does not exist, create it
4. Look for the expected users, and if they do not exist, create them
5. Checks for the installation of git (required) and installs if it does not exist
6. Look for the expected git repository
    1. If it does not exist, clone it
7. Pull updates from the git repository
8. 

## Development

### Documentation

To run and build the documentation for this project, Python and Pip are required. Then setup a virtual python environment and serve the docs from inside the project directory like so:
```SHELL
# Windows Powershell
## Create the python virtual environment
py -m venv .venv
## Activate the python virtual environment
.venv/Scripts/Activate.ps1
## Install documentation requirements
py -m pip install -r requirements.txt
## Serve the documentation
py -m mkdocs serve
```

Then visit http://127.0.0.8:8000 to view your documentation in real time. Updating the documents in the `docs/` folder or the `mkdocs.yml` file will automatically rebuild and display the documentation in the browser for you.
