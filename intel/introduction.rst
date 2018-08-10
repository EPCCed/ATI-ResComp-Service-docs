Atiras, Intel cluster and Secure Safe Haven
===========================================

This chapter contains information about the Alan Turing Institute Remote Access Service (Atiras), Intel cluster and Secure Safe Haven. It explains:

- `Hardware`_
- `Requesting access to Atiras and the Intel cluster`_ 
- `Early Access Service`_
- `Usage Restrictions`_
..
  - `Training Materials`_
  - `Software troubleshooting`_
..

The chapter :doc:`connecting` explains how to connect to Atiras.

Hardware
--------

The Intel cluster within the Secure Safe Haven is a cluster of 32 Intel Xeon compute nodes. Each node has 2 CPUs, a 1 x Skylake Gold 6148F (Omnipath-enabled) CPU and 1 x Skylake Gold 6148 CPU. Each CPU has 20 physical cores, with hyperthreading this provides 40 virtual cores per CPU. The cluster, in total, has 1280 physical cores. Each node has 192GB of memory, 160GB of home storage, 1.5TB scratch storage and 5.5TB extra storage. 300TB of storage is shared across the cluster.

Each node runs CentOS Linux release 7.5.

Requesting access to Atiras and the Intel cluster
-------------------------------------------------

This section explains how you request access to both Atiras and the Intel cluster within the Secure Safe Haven.

Access is via the `Atiras portal <https://secure.epcc.ed.ac.uk/ati/>`_

You need user accounts on BOTH Atiras and the Intel cluster within the Secure Safe Haven. You can request user accounts for both of these using your account on the `ATI SAFE <https://safe.epcc.ed.ac.uk/ati>`_.

Instructions on getting an account for the ATI SAFE and using a *Project Code* to request access to ATI research computing resources are in the :doc:`../safe-guide/safe-guide-users` section of this User Guide.

For Atiras and the Intel cluster, this *Project Code* entry can be obtained by contacting the ATI Research Computing Service Manager via an email to research-computing-support@turing.ac.uk.

If your request for access is successful, you will receive emails from the `ATI SAFE <https://safe.epcc.ed.ac.uk/ati>`_ with the information for your user account on both Atiras and the Intel cluster.

Early Access Service 
--------------------

When Atiras and the Intel cluster within the Secure Safe Haven is initially made available to ATI researchers it will be run as an Early Access service. This purpose of this Early Access service will be to establish how best to later configure the service to meet ATI researcher needs. The Early Access Service will therefore be replaced at a later to be specified date.

This section explains how the Early Access service on Atiras and within the Secure Safe Haven operates.

#. There will be one ATI SAFE *Project Code* for the Early Access Service.
#. This *Project Code* can be obtained by contacting the ATI Research Computing Service Manager via an email to research-computing-support@turing.ac.uk.
#. During the Early Access Service there are no limitations on user disk quotas.
#. There is no batch queuing software on the system. A job will only execute if there are resources available. If sufficient resources are not available then the user will have to try and submit later. 
#. During the Early Access Service there is no procedure in place for resolving disagreements on resource usage and allocations.
#. There is NO backup on any of the filesystems users have access to.
#. There is NO disaster recovery.

Usage Restrictions 
------------------

#. ATI users may not make any public presentation or publish any paper or report on the hardware or software or its performance without receiving prior express written consent from the ATI Research Computing Service Manager.

..
  Training Materials 
  ------------------
..

..
    Software troubleshooting
    ------------------------
..
