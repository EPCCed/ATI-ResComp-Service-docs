Data transfer to and from the ATI Cray Urika
============================================

This chapter explains how to transfer data to and from the ATI Cray Urika service. This requires
a user account on BOTH the Urika and hydra-vpn.epcc.ed.ac.uk. See the chapter 
:doc:`introduction` for instructions on how to get these user accounts.

The instructions are based upon using the scp secure copy command on a Linux command line.

Copying a file from your local machine onto the ATI Urika
---------------------------------------------------------

The following command ::

	scp -o "ProxyCommand ssh your-hydra-vpn-username@hydra-vpn.epcc.ed.ac.uk -W %h:%p" dummy-file your-urika-username@urika1:/home/users/your-urika-username/

copies the file called ``dummy-file`` from the local directory on the local machine to 
the directory ``/home/users/your-urika-username/`` on the ATI Urika. 

The ``-o "ProxyCommand ssh your-hydra-vpn-username@hydra-vpn.epcc.ed.ac.uk -W %h:%p"`` is needed because access to the ATI Urika is through hydra-vpn.epcc.ed.ac.uk.

Note that the first time you execute this command or a similar one that you may be asked to confirm machine fingerprints.
	

Retrieving a file from the ATI Urika to your local machine
----------------------------------------------------------

The following command ::

	scp -o "ProxyCommand ssh your-hydra-vpn-username@hydra-vpn.epcc.ed.ac.uk -W %h:%p" your-urika-username@urika1:/home/users/your-urika-username/urika-dummy-file copy-of-urika-dummy-file

copies the called ``urika-dummy-file`` from the directory ``/home/users/your-urika-username/`` on the ATI Urika to the 
user's local directory on their local machine.



	
