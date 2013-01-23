Setting up Python, Apache, WSGI, etc.
=====================================

Apache and the WSGI module are required to run locally the applications developed to interact with the FME server.  The following steps will create a local environment similar to that on the server, to be used for testing and development.

1. Setup windows paths (note ArcGIS python is used, not FME python, currently at version 2.6):
	- ControlPanel -> System -> Advanced system settings -> Advanced tab -> Environment variables -> System variables -> path
	- Append: ;C:\Python26\ArcGIS10.0;C:\Python26\ArcGIS10.0\Scripts
	- Test by opening a new cmd window, and type 'python'.  You should be in a python shell.
1. Install Python Setuptools (required by pip):
	- Download from http://pypi.python.org/pypi/setuptools
	- Extract archive
	- Open a command shell in setuptools directory
	- Enter: python setup.py install
1. Install PIP:
	- Download from http://pypi.python.org/pypi/pip
	- Extract archive
	- Open a command shell in pip directory
	- Enter: python setup.py install
1. Install Flask (http://flask.pocoo.org/):
	- Open a command shell
	- Enter: python
	- Enter: pip install Flask
1. Install apache http server:	
	- Download from http://httpd.apache.org/download.cgi
	- Double click to install
	- Note without admin privileges run on port 8080
1. Install wsgi module (http://code.google.com/p/modwsgi):
	- Download from http://code.google.com/p/modwsgi/wiki/DownloadTheSoftware
	- Move & rename mod_wsgi-win32-ap22py26-3.3.so to C:\Program Files (x86)\Apache Software Foundation\Apache2.2\modules\mod_wsgi.so
	- Copy this http.conf to C:\Program Files (x86)\Apache Software Foundation\Apache2.2\conf\
	- Note futher configuration information here http://code.google.com/p/modwsgi/wiki/QuickConfigurationGuide

	
	