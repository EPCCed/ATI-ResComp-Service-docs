Alan Turing Institute Cray Urika-GX Service
===========================================

This chapter contains information about the Turing's Cray Urika-GX service ("Urika"). It explains:

- Cray Urika-GX :ref:`hardware`.
- :ref:`access`.
- :ref:`early_access`.
- :ref:`restrictions`.
- :ref:`training`.

Where appropriate it contains links to Cray's documentation for the Cray Urika-GX system.

:doc:`connecting` explains how to connect to the Turing's Cray Urika-GX service.

.. _hardware:

Hardware
--------

The Turing's Cray Urika-GX service consists of 12 compute nodes where each node comprises 256GB of memory, 800 GB SSD and 2x18 core Broadwell CPU. In addition there is 60TB of Lustre storage.

For a detailed description of the Cray Urika-GX platform, see the `Cray website <http://www.cray.com/products/analytics/urika-gx>`_.

.. _access:

Requesting access to Urika
--------------------------

This section explains how you request access to Urika.

Access to Urika is by SSH via hydra-vpn.epcc.ed.ac.uk. You therefore need user accounts on BOTH Urika and hydra-vpn.epcc.ed.ac.uk. You can request user accounts for both of these using your account on the Turing's `SAFE <https://safe.epcc.ed.ac.uk/ati>`_.

Instructions on getting an account for the Turing's SAFE and using a *Project Code* to request access to Turing's research computing resources, including Urika, are in the :doc:`../safe-guide/safe-guide-users` section of this User Guide.

For Urika's Early Access Service, this *Project Code* entry can be obtained by contacting the Turing's Research Computing Service Manager via an email to research-computing-support@turing.ac.uk.  

If your request for access to Urika is successful, you will receive emails from the Turing's `SAFE <https://safe.epcc.ed.ac.uk/ati>`_ with the information for your user account on Urika and, if you do not already have one, information for your user account on hydra-vpn.epcc.ed.ac.uk.

.. _early_access:

Early Access Service 
--------------------

Urika is currently being run for the Turing's researchers as an Early Access Service. This purpose of this Early Access Service is to establish how best to later configure the service to meet the needs of the Turing's researchers. The Early Access Service will be replaced at a future date.

This section explains how Urika's Early Access Service operates:

- There is one SAFE *Project Code* for the Early Access Service.
- This *Project Code* can be obtained by contacting the Turing's Research Computing Service Manager via an email to research-computing-support@turing.ac.uk.
- There are no limitations on user disk quotas.
- There is no batch queuing software provided. A job will only execute if there are resources available. If sufficient resources are not available then the user will have to try and submit later.
- There is no procedure in place for resolving disagreements on resource usage and allocations.
- There is **no** backup on any of the 3 filesystems users have access to.
- There is **no** disaster recovery.

.. _restrictions:

Usage Restrictions 
------------------

- Urika users must not make any public presentation or publish any paper or report on the Cray Urika-GX service, its hardware, software, or its performance without receiving prior express written consent from Cray. Users must provide any results from work on the Cray Urika-GX service, and the methodology as to how the results were obtained, to Cray. Cray is allowed to use such results used in marketing collateral; press releases, white papers, etc. Cray may share these results with Intel.  
- Urika users must therefore not make any public presentation or publish any paper or report on the Cray Urika-GX service, its hardware or software or its performance without receiving prior express written consent from the Turing's Research Computing Service Manager

.. _training:

Training Materials 
------------------

- `Cray Urika-GX training course slides <https://cray.app.box.com/v/ati-training-dec-2017>`_, Cray, December 2017. An overview of the hardware, the software stack, use of applications (including Hadoop, Spark, Cray Graph Engine, Jupyter Notebooks), resource management and case studies. 
