Atiras, Secure Safe Haven and Intel cluster
===========================================

This chapter contains information about the Alan Turing Institute Remote Access Service (Atiras), a Secure Safe Haven with an Intel cluster. It explains:

- `Key components`_
- `Requesting access to Atiras`_ 
- `Early Access Service`_
- `Usage Restrictions`_

Key components
--------------

The **Alan Turing Institute Remote Access Service (Atiras)** provides a service for running computational and data analysis tasks upon project data held within a secure environment. Atiras consists of the following components.

**Atiras portal**

The Atiras portal is a web browser-based remote desktop gateway by which researchers can access the Secure Safe Haven and build arena. It allows the use of virtual machines within Atiras via either a command-line terminal or a graphical desktop.

**Secure Safe Haven**

The Secure Safe Haven provides a project with virtual machines customised with software required by that project and connected to the project's data held within the Secure Safe Haven. These virtual machines allow the project's researchers to run computational and data analysis tasks, access the project's data held within the Secure Safe Haven, and submit jobs to the Intel cluster (these virtual machines also serve as login nodes for the Intel cluster).

Virtual machines do not allow outbound or inbound connections to hosts external to the Secure Safe Haven.

Each virtual machine runs CentOS Linux release 7.5.

**Intel cluster**

The Intel cluster, within the Secure Safe Haven, is a cluster of 32 Intel Xeon compute nodes. Each node has 2 CPUs, a 1 x Skylake Gold 6148F (Omnipath-enabled) CPU and 1 x Skylake Gold 6148 CPU. Each CPU has 20 physical cores, with hyperthreading this provides 40 virtual cores per CPU. The cluster, in total, has 1280 physical cores. Each node has 192GB of memory and 8TB of local storage. 300TB of storage is shared across the cluster via NGS. 33TB is shared via BeeGFS.

Nodes do not allow outbound or inbound connections to hosts external to the Secure Safe Haven.

Each node runs CentOS Linux release 7.5.

**Project data areas**

Each project has a data area in the Secure Safe Haven. These are available in fixed sizes, for example 10GB, 50GB, or 100GB. The size available to a project depends upon both the data a project wants to hold within the Secure Safe Haven and the data they expect to produce from their analyses.

**Build arena**

Complementing the Secure Safe Haven, but sitting outside of it, is the **build arena**. The build arena provides a project with project-specific virtual machines. A project's researcher administrators and researcher developers have administrator rights sufficient to install and configure the computational and data analysis environment required by their project's researchers.

Virtual machines allow outbound connections to hosts external to Atiras, to allow for software to be downloaded and installed in the virtual machines.

Once a virtual machine has been configured, it is deployed, by EPCC's Systems Development Team, into the Secure Safe Haven, where it becomes available as a virtual machine for a project's researchers. Depending on the project, a researcher developer may retain administrator rights on the deployed virtual machine to be able to make configuration changes and fixes for the project's researchers.

Each virtual machine runs CentOS Linux release 7.5. They are configured with 4 CPUs, 16GB memory and ~60GB disk space to allow for software assembly and testing. Once deployed into the Secure Safe Haven the number of cores, available RAM and disk space are extended.

Requesting access to Atiras
---------------------------

This section explains how you request access to Atiras.

If you are a researcher wanting to access a virtual machine for your project within the Secure Safe Haven, you will need:

#. An account for the Atiras portal to access the Secure Safe Haven.
#. An account for a virtual machine in the Secure Safe Haven.

If you are one of your project's researcher administrators or researcher developers wanting to access a virtual machine for your project within the build arena, you will need:

#. An account for the Atiras portal to access the build arena.
#. An account for a virtual machine in the build arena.

Note: if you are a research administrator or researcher developer wanting to access virtual machines both in the build arena and Secure Safe Haven then you will need all 4 accounts.

You can request user accounts for each of these using your account on the `ATI SAFE <https://safe.epcc.ed.ac.uk/ati>`_.

Instructions on getting an account for the ATI SAFE and using a *Project Code* to request access to the ATI's research computing resources are in the :doc:`../safe-guide/safe-guide-users` section of this User Guide.

This *Project Code* entry can be obtained by contacting the ATI's Research Computing Service Manager via an email to research-computing-support@turing.ac.uk.

If your request for access is successful, you will receive emails from the `ATI SAFE <https://safe.epcc.ed.ac.uk/ati>`_ with the information for your user accounts for the Atiras portal, the Secure Safe Haven and the build arena.

Access is via the `Atiras portal <https://secure.epcc.ed.ac.uk/ati/>`_

Early Access Service 
--------------------

When Atiras is initially made available to the ATI's researchers it will be run as an Early Access service. This purpose of this Early Access service will be to establish how best to later configure the service to meet the ATI's researchers' needs. The Early Access service will therefore be replaced at a later to be specified date.

This section explains how the Early Access service on Atiras operates.

#. There will be one ATI SAFE *Project Code* for the Early Access Service.
#. This *Project Code* can be obtained by contacting the ATI Research Computing Service Manager via an email to research-computing-support@turing.ac.uk.
#. During the Early Access Service there are no limitations on user disk quotas.
#. There is no batch queuing software on the system. A job will only execute if there are resources available. If sufficient resources are not available then the user will have to try and submit later. 
#. During the Early Access Service there is no procedure in place for resolving disagreements on resource usage and allocations.
#. There is NO backup on any of the filesystems users have access to.
#. There is NO disaster recovery.
