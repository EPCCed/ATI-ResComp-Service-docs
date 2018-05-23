Data transfer to and from the ATI Cray Urika
============================================

This chapter explains how to transfer data to and from the ATI Cray Urika service. This requires a user account on BOTH the Urika and hydra-vpn.epcc.ed.ac.uk. See the chapter :doc:`introduction` for instructions on how to get these user accounts.

The instructions are based upon using either the ``scp`` secure copy command or ``sftp`` secure file transfer command in bash shell-type environments (e.g. Linux command-line, Mac OS command-line or Git for Windows under Windows).

``scp`` and ``sftp`` support a rich range of options so only examples of commonly file transfer actions are given. For further information consult a web search engine.

Copy files from your local machine to Urika
-------------------------------------------

Use scp on your local machine to push a file to Urika
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Copy a file ``file.dat`` from your home directory on your local machine to your home directory on Urika::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" file.dat <your-urika-username>@urika1:/home/users/<your-urika-username>/

Copy a file ``file.dat`` from your home directory on your local machine to a subdirectory ``sample_data`` of your home directory on Urika::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" file.dat <your-urika-username>@urika1:/home/users/<your-urika-username>/sample_data/

Copy a file ``file.dat`` from your home directory on your local machine to asubdirectory ``sample_data`` of your home directory on Urika, renaming the file to ``sample.dat``::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" file.dat <your-urika-username>@urika1:/home/users/<your-urika-username>/sample_data/sample.dat

You will be prompted for your hydra-vpn.epcc.ed.ac.uk password and then your Urika password.

**Note:** The ``-o "ProxyCommand ssh your-hydra-vpn-username@hydra-vpn.epcc.ed.ac.uk -W %h:%p"`` is needed because access to the Urika is through hydra-vpn.epcc.ed.ac.uk.

**Note:** The first time you execute one of these commands you may be asked to confirm the host fingerprints of hydra-vpn.epcc.ed.ac.uk and ``urika``.

Use scp on Urika to pull a file from your local machine
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

These will only work if your local machine supports `scp` connections.

Copy a file ``file.dat`` from your home directory on your local machine to your home directory on Urika::

    scp <your-local-username>@<your-local-machine>:file.dat .

Copy a file ``file.dat`` from your home directory on your local machine to a subdirectory ``sample_data`` of your home directory on Urika::

    scp <your-local-username>@<your-local-machine>:file.dat sample_data/

Copy a file ``file.dat`` from your home directory on your local machine to asubdirectory ``sample_data`` of your home directory on Urika, renaming the file to ``sample.dat``::

    scp <your-local-username>@<your-local-machine>:file.dat sample_data/sample.dat

You will be prompted for your local machine password.

**Note:** the first time you execute one of these commands you may be asked to confirm the host fingerprint of your local machine.

Copy files from Urika to your local machine
-------------------------------------------

Use scp on your local machine to pull a file from Urika
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Copy a file ``file.dat`` from your home directory on Urika to your home directory on your local machine::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" <your-urika-username>@urika1:/home/users/<your-urika-username>/file.dat .

Copy a file ``file.dat`` from your home directory on Urika to a subdirectory ``sample_data`` of your home directory on your local machine::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" <your-urika-username>@urika1:/home/users/<your-urika-username>/file.dat sample_data/

Copy a file ``file.dat`` from your home directory on Urika to a subdirectory ``sample_data`` of your home directory on your local machine, renaming the file to ``sample.dat``::

    scp -o "ProxyCommand ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -W %h:%p" <your-urika-username>@urika1:/home/users/<your-urika-username>/file.dat sample_data/sample.dat

You will be prompted for your hydra-vpn.epcc.ed.ac.uk password and then your Urika password.

**Note:** The ``-o "ProxyCommand ssh your-hydra-vpn-username@hydra-vpn.epcc.ed.ac.uk -W %h:%p"`` is needed because access to the Urika is through hydra-vpn.epcc.ed.ac.uk.

**Note:** The first time you execute one of these commands you may be asked to confirm the host fingerprints of hydra-vpn.epcc.ed.ac.uk and ``urika``.

Use scp on Urika to push a file from your local machine
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This will only work if your local machine supports `scp` connections.

Copy a file ``file.dat`` from your home directory on Urika to your home directory on your local machine::

    scp file.dat <your-local-username>@<your-local-machine>:

Copy a file ``file.dat`` from your home directory on Urika to a subdirectory ``sample_data`` of your home directory on your local machine::

    scp file.dat <your-local-username>@<your-local-machine>:sample_data

Copy a file ``file.dat`` from your home directory on Urika to a subdirectory ``sample_data`` of your home directory on your local machine, renaming the file to ``sample.dat``::

    scp file.dat <your-local-username>@<your-local-machine>:sample_data/sample.dat

You will be prompted for your local machine password.

**Note:** the first time you execute one of these commands you may be asked to confirm the host fingerprint of your local machine.
