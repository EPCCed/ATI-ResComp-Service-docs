Troubleshooting
===============

Jupyter through the Urika web interface gives "500 : Internal Server Error"
---------------------------------------------------------------------------

You might find that if you use Jupyter through the Urika web interface that after you enter your Urika username and password you get the error "500 : Internal Server Error".

This can be caused by you not having a home directory. This, in turn, can occur if you try to use Jupyter without having at least one time logged into Urika using the command-line. Your home directory is created the first time you log into Urika using the command-line.

To fix the problem, log in to Urika using the command-line (see :doc:`connecting`) then try accessing Jupyter again.

"mrun" raises "ERROR:Not enough nodes"
--------------------------------------

If you run ``mrun`` and ask for more nodes than there are nodes free you will ghet this error. For example, if you were to check the available nodes::

    mrun --info

This might show::

    Available Resources:
                         : Nodes[ 1] CPUs[ 36] idle nid000[09]
                         : Nodes[ 8] CPUs[288] busy nid000[03-05,08,10-13]
                         : Nodes[ 5] CPUs[???] down nid000[00-02,06-07]

Asking for 4 nodes in this case::

    mrun -n 4 -N 4 hello_world

will raise this errror::

    Thu Aug 09 2018 16:05:13.174259 BST[][mrun]:ERROR:Not enough nodes.
    Available: 1 Needed: 4

Urika has no specific job management tool like PBS, Slurm etc. As a result, job scheduling tools, such as ``mrun`` will wait according to its own rules until resources become available. Its default behaviour is to exit if the requested resources (in this case, nodes) are not available.

You can use ``mrun``'s command-line options to change this behaviour::

    --immediate=<number>
           Exit if resources are not  available  within
           the time period specified.

     --wait
           If enough idle resources are not immediately
           available to run this job, this option  will
           ask Mesos to allocate as many as it can, and
           continue to block as busy resources free  up
           and  ask  Mesos  to  allocate those as well,
            until enough are allocated for this  job  to
           begin.

For more information, see the the ``mrun`` manual page::

    man mrun
