Installation
============

Requirements
------------

This is how you install globsim

``pip install globsim`` (eventually it will be a package)

NetCDF
------
NetCDF files are used to store data in a standard format. The NCO libraries must be installed and built on your computer for GLOBSIM to work.  Instructions can be found `Here <https://www.unidata.ucar.edu/software/netcdf/docs/getting_and_building_netcdf.html>`_. 

ECMWF Client libraries
----------------------
ECMWF is used to access ERA files. Python libraries (supporting python 2.7 and 3) to access the API are available from the `ECMWF website <https://confluence.ecmwf.int/display/WEBAPI/Accessing+ECMWF+data+servers+in+batch>`_


ESMF
----
GLOBSIM uses ESMF libraries to do efficient regridding. These libraries must be built on your machine and have additional dependencies.  ESMP versions 7.0.1 and 7.1.0r are supported. To download ESMF, consult the `ESMF Users Guide <http://www.earthsystemmodeling.org/esmf_releases/public/ESMF_7_1_0r/ESMF_usrdoc/>`_, particularly sections 5 and 8.

During installation, several environment variables are set::

ESMF_NETCDF
ESMF_NETCDF_LIBPATH
ESMF_NETCDF_LIBS
ESMF_NETCDF_INCLUDE
ESMF_COMPILER
ESMF_COMM

ESMPy
^^^^^^
ESMPy provide python bindings for the ESMF libraries.  If you have successfully installed the ESMF libraries, you can follow the instructions `here <http://www.earthsystemmodeling.org/esmf_releases/public/ESMF_7_1_0r/esmpy_doc/html/install.html#installing-esmpy>`_ to extract the python bindings.  More info is available at the `ESMPy main page <https://www.earthsystemcog.org/projects/esmpy/>`_.
