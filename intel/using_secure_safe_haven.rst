Using the Secure Safe Haven
===========================

This chapter explains how to use a virtual machine for your project in the Secure Safe Haven of Atiras.

The virtual machine is customised with software required by your project and is connected to your project's data held within the Secure Safe Haven. The virtual machine allows you to run computational and data analysis tasks, access your data held within the Secure Safe Haven, and submit jobs to the Intel cluster (these virtual machines also serve as login nodes for the Intel cluster).

See the chapter :doc:`connecting` for instructions on how to connect to a virtual machine in the Secure Safe Haven.

Access project data
-------------------

Your project data will be available as NFS mounts on your virtual machine. These will be in the ``/mnt/`` directory.

Submit a job to the Intel cluster
---------------------------------

The Secure Safe Haven uses the `Slurm workload manager <https://slurm.schedmd.com/>`_ to run jobs on the Intel cluster.

You can submit jobs to the Intel cluster using the ``qsub`` command.

Data security within the Intel cluster
--------------------------------------

**These are planned**

Local disks on compute nodes are purged at the end of each run.

File permissions on ``/tmp`` directories are such that other projects won't be able to access any temporary data that has been deposited there by you. Furthermore, the contents of ``/tmp`` are deleted on a regular basis to avoid project-specific data inadvertently being left there.

The job scheduler is configured so that two projects never share the same compute node at the same time.

Troubleshooting: no internet connections
----------------------------------------

Virtual machines in the Secure Safe Haven do not allow outbound or inbound connections to hosts external to the Secure Safe Haven.
