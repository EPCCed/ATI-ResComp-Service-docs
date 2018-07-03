Cray Urika GX
=============

This chapter contains information about the ATI service on the Cray Urika GX system. It explains:

- the `Hardware`_
- `Requesting access to the ATI Cray Urika GX system`_ 
- the `Early Access Service`_
- `Usage Restrictions`_
- `Training Materials`_
- `Software troubleshooting`_


Where appropriate it contains links to Cray's documentation for the system.

The chapter :doc:`connecting` explains how to connect to the ATI service on the Cray Urika GX system.

Hardware
--------

The Cray Urika GX system consists of 12 compute nodes (each 2x18 core Broadwell CPU)
with 256GB of memory and 60TB of storage. For more details of the Urika system,
see the `Cray website <http://www.cray.com/products/analytics/urika-gx>`_.

Requesting access to the ATI Cray Urika GX system 
-------------------------------------------------

This section explains how you request access to the ATI service on the Cray Urika GX system. 

Access to the Cray Urika GX system is by SSH via hydra-vpn.epcc.ed.ac.uk. You therefore 
need user accounts on BOTH the Cray Urika and hydra-vpn.epcc.ed.ac.uk. You can request user accounts for both of these using your account on the `ATI SAFE <https://safe.epcc.ed.ac.uk/ati>`_.

Instructions on getting an account for the ATI SAFE and using a *Project Code* to request 
access to ATI research computing resources such as the Urika are in the 
:doc:`../safe-guide/safe-guide-users` section of this User Guide.

For the Urika Early Access service, this *Project Code* entry can be obtained 
by contacting the ATI Research Computing Service Manager via an email to 
research-computing-support@turing.ac.uk.  

If your request for access to the Urika is successful, you will receive emails from the 
`ATI SAFE <https://safe.epcc.ed.ac.uk/ati>`_ with the information for your user account on
the Urika and, if you do not already have one, information for your user account on the hydra-vpn.epcc.ed.ac.uk machine.

Early Access Service 
--------------------

When the Cray Urika GX system is initially made available to ATI researchers it will be run as an Early Access service. This purpose of this Early Access service will be to establish how best to later configure the service to meet ATI researcher needs. The Early Access Service will therefore be replaced at a later to be specified date.

This section explains how the Early Access service on the Cray Urika GX system operates.

#. There will be one ATI SAFE *Project Code* for the Early Access Service.
#. This *Project Code* can be obtained by contacting the ATI Research Computing Service Manager via an email to research-computing-support@turing.ac.uk.
#. During the Early Access Service there are no limitations on user disk quotas.
#. There is no batch queuing software on the system. A job will only execute if there are resources available. If sufficient resources are not available then the user will have to try and submit later. 
#. During the Early Access Service there is no procedure in place for resolving disagreements on resource usage and allocations.
#. There is NO backup on any of the 3 filesystems users have access to.
#. There is NO disaster recovery.


Usage Restrictions 
------------------

#. ATI Cray GX system users may not make any public presentation or publish any paper or report on the Equipment or its performance without receiving prior express written consent from Cray. ATI users must provide any results from work on the system and methodology as to how the Results were obtained to Cray. Cray is allowed to use such results used in marketing collateral; press releases, white papers, etc. Cray may share Results with Intel.  
#. ATI users may therefore not make any public presentation or publish any paper or report on the Urika GX hardware or software or its performance without receiving prior express written consent from the ATI Research Computing Service Manager

Training Materials 
------------------

#. The slides from the Urika training course given by Cray in December 2017 are `available <https://cray.app.box.com/v/ati-training-dec-2017>`_.
#. These slides provide an overview of the hardware, the software stack, use of applications (Hadoop, Spark, Cray Graph Engine, Jupyter Notebooks), resource management and case studies. 
#. Cray have also provided slides explaining the various job submission mechanisms available on the Urika.  These are available on the Urika itself via a web browser configured to access Cray's application (see :doc:`connecting`).  In such a browser these slide are available at http://urika1.turing.ac.uk/static/documentation/notebooks/ATI-Job-Submission.pdf 

Software troubleshooting
------------------------

#. Using Jupyter through the Urika web interface: when you first get your Urika account, you must first log in directly to the command line (see :doc:`connecting`).  This ensures that a home directory is created for you. If you do NOT do this then if you attempt to use Jupyter through the Urika web interface then after you enter your Urika username and password you will get the error  "500 : Internal Server Error".
