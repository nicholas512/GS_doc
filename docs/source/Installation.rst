Installation
============

Requirements
------------

This is how you install globsim

``pip install globsim``

NetCDF
------

ECMWF Client libraries
----------------------
ECMWF is used to access ERA files. Python libraries (supporting python 2.7 and 3) to access the API are available from the `ECMWF website <https://confluence.ecmwf.int/display/WEBAPI/Accessing+ECMWF+data+servers+in+batch>`

ESMF
----
GLOBSIM uses ESMF libraries to do efficient regridding. These libraries must be built on your machine and have additional dependencies.  ESMP versions 7.0.1 and 7.1.0r are supported. To download ESMF, consult the `ESMF Users Guide <http://www.earthsystemmodeling.org/esmf_releases/public/ESMF_7_1_0r/ESMF_usrdoc/>`, particularly sections 5 and 8.

ESMPy
^^^^^^
ESMPy provide python bindings for the ESMF libraries.  If you have successfully installed the ESMF libraries, you can follow the instructions `here <http://www.earthsystemmodeling.org/esmf_releases/public/ESMF_7_1_0r/esmpy_doc/html/install.html#installing-esmpy>` to extract the python bindings. 
