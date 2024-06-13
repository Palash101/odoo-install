<h3>Installation procedure</h3>

1. **Download the script:**
```text
git clone https://github.com/ventor-tech/odoo-install-script
```
2. **Modify the parameters as you wish.**
There are a few things you can configure, this is the most used list:

- OE_USER - will be the username for the system user.
- OE_HOME - will be the home directory of the system user.
- OE_VERSION - is the Odoo version to install, for example _10.0_ for Odoo V10.
- OE_INSTALL_DIR - is the path where all environment will be installed to.
- OE_REPO - is the path where odoo will be clonned to.
- INSTALL_WKHTMLTOPDF - set to _False_ if you do not want to install it, if you want to install it you should set it to _True_.
- OE_PORT - is the port where Odoo should run on, for example 8069.
- OE_NETRPC_PORT - is the port where Odoo net-rpc should run on, for example 8070.
- OE_LONGPOOL_PORT - is the port where Odoo long pool should run on, for example 8070.
- IS_ENTERPRISE - will install the Enterprise version on top of community version if you set it to _True_, set it to _False_ if you want the community version of Odoo.
- OE_SUPERADMIN - is the master password for this Odoo installation.
- OE_DB_PASSWORD - is the password of postgres user.
- OE_WORKERS - is the number of Odoo workers
- PG_VERSION - is a version of postgresql installed

3. **Become root**
```text
su
```
4. **Make the script executable**
```text
sudo chmod +x run.sh
```
5. **Execute the script:**
```text
sudo ./run.sh
```
To run on ubuntu 22 where python 3.12 is intalled


1. **Install python3.10:**
```text
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.10

```
2. **Set Python3.10 as defualt:**
```text
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.12 1
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.10 2
```

3. **Install Latest postgress:**
```text
sudo apt install postgresql postgresql-contrib
```
4. **Install python dependencies: make sure to use 3.10 for dev dependency**
```text
sudo apt install libsasl2-dev python3.10-dev libldap2-dev libssl-dev
```
5. **Install python dependencies: make sure to use 3.10 for dev dependency**
```text
python3 -m pip install --upgrade pip setuptools wheel
```


