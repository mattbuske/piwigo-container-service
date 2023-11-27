# Piwigo Container Service for Podman

Pull the install script from your AlmaLinux Host via:
```SHELL
curl https://github.com/mattbuske/piwigo-container-service/blob/main/setup/install.sh > ./install.sh
./install.sh
```

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
