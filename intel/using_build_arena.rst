Using the build arena
=====================

This chapter explains how to use, and configure, a virtual machine for your project in the build arena of Atiras to both:

* Install and configure the computational and data analysis environment required by your project's researchers.
* Build a `Docker <https://www.docker.com/>`_ image containing a computational and data analysis environment which can be deployed upon nodes within the Intel cluster when your project's researchers submit jobs to the cluster.

The virtual machine allows outbound connections to hosts external to Atiras, to allow you to download software and install it on your virtual machine, and to build a Docker image.

The virtual machine runs CentOS Linux release 7.5.

See the chapter :doc:`connecting` for instructions on how to connect to a virtual machine in the build arena.

Run commands as administrator
-----------------------------

To run commands as administrator, run::

    sudo su -

You will be prompted for a password::

    [sudo] password for <your-virtual-machine-username>

Enter your virtual machine password. 

The prompt should change to the administrator prompt::

    #

Get software/data/documentation into the virtual machine
--------------------------------------------------------

The virtual machine supports a number of standard ways to get content - including software, data (for example sample data, test data, but *not secure or sensitive project data*), and documentation - into your virtual machine. This includes tools to:

* Access files from URLs, and interact with REST endpoints: ``curl``, ``wget``
* Securely transfer files: ``scp``, ``sftp``
* Securely log into remote hosts:, ``ssh``
* Interact with source code repositories: ``git``, ``svn``, ``cvs``

If using your virtual machine via RDP, then Mozilla Firefox web browser is also available:

* Either, run::

        firefox

* Or, select Applications => Firefox

Deploy a virtual machine, and Docker image, into the Secure Safe Haven
----------------------------------------------------------------------

Once you have configured the virtual machine, and, optionally, a Docker image, with the software needed by the researchers on your project, it can be deployed within the Secure Safe Haven. The process is as follows:

#. Request that the virtual machine, and Docker image (if applicable), be deployed into the Secure Safe Haven.
#. EPCC's Systems Development Team (SDT) audits your virtual machine in accordance with the required security standards of both your project and the Secure Safe Haven. If they have any concerns, suggestions, or requirements they will pass these back to you for you to act upon.
#. If you have built a Docker image, SDT will audit that also.
#. SDT shuts down your virtual machine in the build arena.
#. SDT copies your virtual machine into the Secure Safe Haven, connects it to your project's data area and starts it up. It is now available as a virtual machine for use by your project's researchers.
#. If you have built a Docker image, SDT deploys the image into the Secure Safe Haven, configuring the Secure Safe Haven so that the Docker image is deployed upon nodes within the Intel cluster when your researchers submit jobs.
#. SDT restarts the virtual machine in the build arena.

Default text editors
--------------------

By default, each build arena virtual machine provides two text editors:

* `ViM <https://www.vim.org/>`_: ``vi`` or ``vim``.
* GNU `nano <https://www.nano-editor.org/>`_: ``nano``.
