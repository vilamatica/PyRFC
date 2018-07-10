# PyRFC - Instalación

## Creación Virtualenv

```bash
$ mkvirtualenv -p python2.7 pyrfc
(pyrfc): $ pip install -r requirements.txt
Collecting cython==0.28.4 (from -r requirements.txt (line 1))
  Using cached https://files.pythonhosted.org/packages/ae/02/4f218b527aee1a1ea5592ec2f75052f6dbc616f6107a1c7658f92ae19962/Cython-0.28.4-cp27-cp27mu-manylinux1_x86_64.whl
Installing collected packages: cython
Successfully installed cython-0.28.4
(ppyrfc): $ vim setup.py
CYTHON_VERSION = '0.28.4' # Verify it's same version!!!
```

## Compilación

Teniendo instalada la [SAP NW RFC Library](http://sap.github.io/PyRFC/install.html#sap-nw-rfc-library-installation), por ejemplo, en /opt/sap/nwrfcsdk

```bash
(pyrfc): $ SAPNWRFC_HOME=/opt/sap/nwrfcsdk python setup.py sdist bdist_wheel

....

running install
running install_lib
creating build/bdist.linux-x86_64
creating build/bdist.linux-x86_64/wheel
creating build/bdist.linux-x86_64/wheel/pyrfc
copying build/lib.linux-x86_64-2.7/pyrfc/_exception.py -> build/bdist.linux-x86_64/wheel/pyrfc
copying build/lib.linux-x86_64-2.7/pyrfc/__init__.py -> build/bdist.linux-x86_64/wheel/pyrfc
copying build/lib.linux-x86_64-2.7/pyrfc/_pyrfc.so -> build/bdist.linux-x86_64/wheel/pyrfc
running install_egg_info
Copying src/pyrfc.egg-info to build/bdist.linux-x86_64/wheel/pyrfc-1.9.91-py2.7.egg-info
running install_scripts
creating build/bdist.linux-x86_64/wheel/pyrfc-1.9.91.dist-info/WHEEL
creating 'dist/pyrfc-1.9.91-cp27-cp27mu-linux_x86_64.whl' and adding '.' to it
adding 'pyrfc/__init__.py'
adding 'pyrfc/_exception.py'
adding 'pyrfc/_pyrfc.so'
adding 'pyrfc-1.9.91.dist-info/top_level.txt'
adding 'pyrfc-1.9.91.dist-info/WHEEL'
adding 'pyrfc-1.9.91.dist-info/METADATA'
adding 'pyrfc-1.9.91.dist-info/RECORD'
removing build/bdist.linux-x86_64/wheel
```
