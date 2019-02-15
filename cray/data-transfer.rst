Data transfer to and from the Turing's Cray Urika-GX service
============================================================

This chapter explains how to transfer data to and from the Turing's Cray Urika-GX service ("Urika"). This requires a user account on BOTH Urika and hydra-vpn.epcc.ed.ac.uk. See :doc:`introduction` for instructions on how to get these user accounts.

The instructions are based upon using either the SCP secure copy command or SFTP secure file transfer command in bash shell-type environments (e.g. Linux command-line, Mac OS command-line or Git for Windows under Windows).

Lustre
------

Lustre is a high-performance parallel filesystem connected to Urika. Compute jobs can access data on Lustre in a highly-efficient way. 

You will have been given your own directory on Lustre::

    /mnt/lustre/<your-project-code>/<your-project-code>/<your-urika-username>

where ``<your-project-code>`` is the code of your project. By default all members of your project group can read this folder, but only you can write to it.

If you don't have such a directory, you can create one e.g.::

    mkdir /mnt/lustre/<your-project-code>/<your-project-code>/<your-urika-username>

You will also have access to a ``shared`` directory on Lustre::

    /mnt/lustre/<your-project-code>/<your-project-code>/shared

By default all members of your project group can both read and write to this folder (but no members of other projects can read or write to it).

There follows examples of data transfer to and from your home directory on Lustre. If you want to transfer data to and from your project's ``shared`` directory, replace ``/<your-project-code>/<your-project-code>/<your-urika-username>`` with ``<your-project-code>/<your-project-code>/shared`` in the following.

Using secure copy, SCP
----------------------

SCP supports a rich range of options so only examples of commonly file transfer actions are given. For further information consult a web search engine.

Pushing files from your local machine to Urika
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Copy a file ``file.dat`` from your home directory on your local machine to your home directory on Urika::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" file.dat <your-urika-username>@urika1:/home/users/<your-urika-username>/

Copy a file ``file.dat`` from your home directory on your local machine to a subdirectory ``sample_data`` of your home directory on Urika::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" file.dat <your-urika-username>@urika1:/home/users/<your-urika-username>/sample_data/

Copy a file ``file.dat`` from your home directory on your local machine to asubdirectory ``sample_data`` of your home directory on Urika, renaming the file to ``sample.dat``::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" file.dat <your-urika-username>@urika1:/home/users/<your-urika-username>/sample_data/sample.dat

Copy a directory ``data`` from your home directory on your local machine to your home directory on Urika::

    scp -r -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" data <your-urika-username>@urika1:/home/users/<your-urika-username>/

You will be prompted for your hydra-vpn.epcc.ed.ac.uk password and then your Urika password.

Copy a file ``file.dat`` from your home directory on your local machine to your Lustre directory on Urika::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" file.dat <your-urika-username>@urika1:/mnt/lustre/<your-project-code>/<your-project-code>/<your-urika-username>

**Note:** The ``-o "ProxyCommand ssh your-hydra-vpn-username@hydra-vpn.epcc.ed.ac.uk -W %h:%p"`` is needed because access to the Urika is through hydra-vpn.epcc.ed.ac.uk.

**Note:** The first time you execute one of these commands you may be asked to confirm the host fingerprints of hydra-vpn.epcc.ed.ac.uk and ``urika``.

Pulling files from your local machine to Urika
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

These will only work if your local machine supports SCP connections.

Copy a file ``file.dat`` from your home directory on your local machine to your home directory on Urika::

    scp <your-local-username>@<your-local-machine>:file.dat .

Copy a file ``file.dat`` from your home directory on your local machine to a subdirectory ``sample_data`` of your home directory on Urika::

    scp <your-local-username>@<your-local-machine>:file.dat sample_data/

Copy a file ``file.dat`` from your home directory on your local machine to asubdirectory ``sample_data`` of your home directory on Urika, renaming the file to ``sample.dat``::

    scp <your-local-username>@<your-local-machine>:file.dat sample_data/sample.dat

Copy a directory ``data`` from your home directory on your local machine to your home directory on Urika::

    scp -r <your-local-username>@<your-local-machine>:data .

You will be prompted for your local machine password.

**Note:** the first time you execute one of these commands you may be asked to confirm the host fingerprint of your local machine.

Pulling files from Urika to your local machine
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Copy a file ``file.dat`` from your home directory on Urika to your home directory on your local machine::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" <your-urika-username>@urika1:/home/users/<your-urika-username>/file.dat .

Copy a file ``file.dat`` from your home directory on Urika to a subdirectory ``sample_data`` of your home directory on your local machine::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" <your-urika-username>@urika1:/home/users/<your-urika-username>/file.dat sample_data/

Copy a file ``file.dat`` from your home directory on Urika to a subdirectory ``sample_data`` of your home directory on your local machine, renaming the file to ``sample.dat``::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" <your-urika-username>@urika1:/home/users/<your-urika-username>/file.dat sample_data/sample.dat

Copy a directory ``data`` from your home directory on Urika to your home directory on your local machine::

    scp -r -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" <your-urika-username>@urika1:/home/users/<your-urika-username>/data .

Copy a file ``file.dat`` from your Lustre directory on Urika to your home directory on your local machine::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" <your-urika-username>@urika1:/mnt/lustre/<your-project-code>/<your-project-code>/<your-urika-username>/file.dat .

You will be prompted for your hydra-vpn.epcc.ed.ac.uk password and then your Urika password.

**Note:** The ``-o "ProxyCommand ssh your-hydra-vpn-username@hydra-vpn.epcc.ed.ac.uk -W %h:%p"`` is needed because access to the Urika is through hydra-vpn.epcc.ed.ac.uk.

**Note:** The first time you execute one of these commands you may be asked to confirm the host fingerprints of hydra-vpn.epcc.ed.ac.uk and ``urika``.

Pushing files from Urika to your local machine
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This will only work if your local machine supports SCP connections.

Copy a file ``file.dat`` from your home directory on Urika to your home directory on your local machine::

    scp file.dat <your-local-username>@<your-local-machine>:

Copy a file ``file.dat`` from your home directory on Urika to a subdirectory ``sample_data`` of your home directory on your local machine::

    scp file.dat <your-local-username>@<your-local-machine>:sample_data

Copy a file ``file.dat`` from your home directory on Urika to a subdirectory ``sample_data`` of your home directory on your local machine, renaming the file to ``sample.dat``::

    scp file.dat <your-local-username>@<your-local-machine>:sample_data/sample.dat

Copy a directory ``data`` from your home directory on Urika to your home directory on your local machine::

    scp -r data <your-local-username>@<your-local-machine>:

You will be prompted for your local machine password.

**Note:** the first time you execute one of these commands you may be asked to confirm the host fingerprint of your local machine.

Using secure file transfer, SFTP
--------------------------------

These commands only work if your local machine supports SFTP connections.

SFTP supports a rich range of options so only examples of commonly file transfer actions are given. For further information consult a web search engine.

SFTP by default attempts to connect to port 22 on the local machine. If your local machine uses a non-default port then this can be specified using the ``oPort`` argument. For example, if the local port was 22222, you would provide an argument ``-oPort=22222``.

Pulling files from your local machine to Urika
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Copy a file ``file.dat`` from your home directory on your local machine to your home directory on Urika::

    sftp <your-local-username>@<your-local-machine>:<path-to-your-home-directory>/file.dat .

Copy a directory ``data`` from your home directory on your local machine to your home directory on Urika::

    sftp -r <your-local-username>@<your-local-machine>:<path-to-your-home-directory>/data .

You will be prompted for your local machine password.

Copying files between your local machine and Urika
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Log in to your local machine's SFTP server::

    sftp <your-local-username>@<your-local-machine>

You will be prompted for your local machine password. The following commands are all run within an SFTP session shell.

Change to your home directory on your local machine::

    cd <path-to-your-home-directory>

List the files in the current directory on your local machine::

    ls

Copy a file ``file.dat`` from the current directory on your local machine to your current directory on Urika::

    get file.dat

Copy a directory ``data`` from the current directory on your local machine to your current directory on Urika::

    get -r data

List the files in the current directory on Urika::

    lls

Copy a file ``file.dat`` from the current directory on Urika into the current directory on your local machine::

    put file.dat

Copy a directory ``data`` from the current directory on Urika into the current directory on your local machine::

    put -r data

Exit the SFTP session::

    exit

Using SSHFS to mount a remote directory
---------------------------------------

You can also mount a remove directory into your home directory on Urika using `SSHFS <https://github.com/libfuse/sshfs/>`_. Once mounted, you can use your directory as if it was a local directory.

This command only works if your local machine supports SFTP connections.

As SSHFS uses SFTP, it, by default, attempts to connect to port 22 on the local machine. If your local machine uses a non-default port then this can be specified using the ``oPort`` argument. For example, if the local port was 22222, you would provide an argument ``-oPort=22222``.

For example, to mount a directory ``data`` from your home directory on your local machine to your home directory on Urika::

    mkdir data
    sshfs -o intr,large_read,auto_cache,workaround=all <your-local-username>@<your-local-machine>:data data

You will be prompted for your local machine password.

To remove the mount you can run, for example::

    fusermount -u data
    rmdir data

**Note:** Do **not** mount directories directly onto Lustre. Urika compute nodes have no network access and so cannot access directories via a mount.
