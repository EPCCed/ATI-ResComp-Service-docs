Data transfer to and from the ATI Cray Urika
============================================

This chapter explains how to transfer data to and from the ATI Cray Urika service. This requires
a user account on BOTH the Urika and hydra-vpn.epcc.ed.ac.uk. See the chapter 
:doc:`introduction` for instructions on how to get these user accounts.

The instructions are based upon using the scp secure copy command on a Linux command line.

Copying a file from your local machine onto the ATI Urika
---------------------------------------------------------

The following command ::

	scp -o "ProxyCommand ssh tsloan@hydra-vpn.epcc.ed.ac.uk -W %h:%p" dummy-file tsloan@urika1:/home/users/tsloan/

copies the file called ``dummy-file`` from the local directory on the local machine to 
the directory ``/home/users/tsloan/`` on the ATI Urika. 

The ``-o "ProxyCommand ssh tsloan@hydra-vpn.epcc.ed.ac.uk -W %h:%p"`` is needed because access to the ATI Urika is through hydra-vpn.epcc.ed.ac.uk.

Note that the first time you execute this command or a similar one that you may be asked to confirm machine fingerprints.
	

Retrieving a file from the ATI Urika to your local machine
----------------------------------------------------------

The following command ::

	scp -o "ProxyCommand ssh tsloan@hydra-vpn.epcc.ed.ac.uk -W %h:%p" tsloan@urika1:/home/users/tsloan/urika-dummy-file copy-of-urika-dummy-file

copies the called ``urika-dummy-file`` from the directory ``/home/users/tsloan/`` on the ATI Urika to the 
user's local directory on their local machine.


Using wget on the ATI Urika 
---------------------------

Some of the user documentation for the software available on the ATI Urika 
refers to the use of ``wget`` in Urika command line examples.  For example in the 
`Urika GX Analytic Applications Guide <http://docs.cray.com/PDF/Urika-GX_Analytics_Applications_Guide_12UP00_S-3015.pdf>`_, 
section 4.3, bullet 2 has the command ::

	$ wget -U firefox http://www.gutenberg.org/cache/epub/76/pg76.txt

Given that access to the Urika is via ssh through hydra-vpn.epcc.ed.ac.uk then 
this command must be executed as follows on the ATI Urika ::

	ssh 172.24.40.13 'wget -U firefox http://www.gutenberg.org/cache/epub/76/pg76.txt' >> pg76.txt
	
where 172.24.40.13 is the IP address of hydra-vpn.epcc.ed.ac.uk. 

Note this means that a copy of the file being transferred will also reside in the user's account on hydra-vpn.epcc.ed.ac.uk.

	
