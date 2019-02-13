.. _docker:

Running GlobSim with Docker
============================

As an alternative to building GlobSim from scratch, you can run it in a Docker container and save yourself hours of compiling ESMF.

Install Docker
--------------
Install Docker from the `Docker website <https://www.docker.com/get-started>`_


Open GlobSim Docker container
-----------------------------
Next, open a docker command-line window.
If you don't have the docker container image but only the docker build file, enter the following to create an image::

    docker build <dir> --tag=GlobSim
    
where <dir> is replaced by the directory containing the following files::

    Dockerfile
    esmf-python.tar.gz
    
Then, start the docker container! You'll want to attach it to a folder on your computer using the `-v` flag, replacing <directory> with a directory on your computer::

    docker run --rm -v <directory>:/data: -t -i GlobSim
    
.. note:: Windows users: Docker is only able to attach directories that are listed in VirtualBox as shared directories. This defaults to 'C:/Users' (entered as '/c/users' in the docker command line). For any directories outside of this path, you must `manually add shared folders <http://support.divio.com/local-development/docker/how-to-use-a-directory-outside-cusers-with-docker-toolboxdocker-for-windows>`_ through the VirtualBox GUI.  

Download GlobSim
----------------
Download GlobSim into the /opt folder

From github::
  
    cd /opt
    git clone https://geocryology/globsim
    git checkout working
    
With pip (not yet)::
 
    pip3 install globsim
    
From a tar.gz file in your attached volume::

    cp /data/globsim.tar.gz /opt/
    cd /opt
    tar -xvf globsim.tar.gz
    
Copy credentials files
----------------------
Obtain the necessary credentials files and copy them into the /root folder of the docker image using the attached volume (if you were running this elsewhere you would copy them into your home folder)

Run GlobSim using the example directories
-----------------------------------------
You're now ready to run GlobSim! Try the :ref:`example`

