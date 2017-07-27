# Using JupyterHub and SpiNNaker
The Jupyter Notebook is a tool where code can be executed / demonstrated in cells in a browser interface. The code is executed by the Kernel which receives instructions from the Jupyter Notebook frontend.

JupyterHub is a tool allowing multiple users to spawn instances of a Jupyter Notebook server installed on a local machine, so that other people can run Jupyter notebooks as if they were on the local machine.

This means that in demonstrations, users can access a SpiNNaker installation and use PyNN from any computer on a network, connected to the server.

## Installing JupyterHub
- Make sure all services are installed into the system as **root** instead of into a user directory so that all users can access it.
- Install [Jupyter](http://jupyter.org/install.html) using `pip3` to ensure that Jupyter runs from a Python3 installation. Do not use Anaconda as it creates a Python installation in a local user directory.
- Install [JupyterHub](https://jupyterhub.readthedocs.io/en/latest/) - requires Python3.4 or greater.
- [Create](https://jupyterhub.readthedocs.io/en/latest/config-basics.html) a `jupyter_config.py` file and [add your user as admin](https://jupyterhub.readthedocs.io/en/latest/authenticators-users-basics.html)
- Run JupyterHub by running `sudo jupyterhub` from the folder which contains the config file.

## Using SPyNNaker8
- Make sure the SpiNNaker files are in a system directory (e.g. `/usr/share/`) and that the correct system environmental variables are setup in `/etc/profile.d` or `/etc/profile/`
- Place the `.spynnaker.cfg` file in `/etc/xdg` instead of a user directory so that all users read that instead of creating their own.

