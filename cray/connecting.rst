Connecting to the Turing's Cray Urika-GX service
================================================

This chapter explains how to connect to the Turing's Cray Urika-GX service ("Urika"). This requires a user account on BOTH Urika and hydra-vpn.epcc.ed.ac.uk. See the chapter :doc:`introduction` for instructions on how to get these user accounts.

Access to Urika is via SSH. The applications software on Urika itself can be accessed via a web browser. This chapter explains how to setup an SSH tunnel from hydra-vpn.epcc.ed.ac.uk to Urika so that a web browser can be used to access the applications software. It also explains how to access Urika's command line directly.

An overview of how to connect is as follows. Instructions are provided for:

* Windows: using `MobaXterm <https://mobaxterm.mobatek.net/>`_ (recommended), `PuTTY <https://putty.org>`_ or the ssh client in `Git for Windows <https://git-for-windows.github.io/>`_ SSH clients and Mozilla Firefox, Internet Explorer and Google Chrome web browsers.
* MacOS and Linux: using ssh client and Mozilla Firefox web browser.

Other SSH client software and web browsers can also be used if they are suitably configured.

Connecting involves the following steps:

1. :ref:`setup-ssh-tunnel`.
2. :ref:`modify-hosts`.
3. :ref:`configure-browser`.
4. :ref:`use-browser`.

Alternatively you can:

* :ref:`connect-cli`.

In the following:

* Replace ``your-hydra-vpn-username`` with your hydra-vpn.epcc.ed.ac.uk username.
* Replace ``your-urika-username`` with your Urika username.

.. _setup-ssh-tunnel:

Set up an SSH tunnel to Urika
-----------------------------

If you are a Windows user, you can do one of:

* :ref:`ssh-tunnel-moba`.
* :ref:`ssh-tunnel-putty`.
* :ref:`ssh-tunnel-putty-prompt`.
* :ref:`ssh-tunnel-git`.

If you are a MacOS or Linux user, you can:

* :ref:`ssh-tunnel-ssh`.

.. _ssh-tunnel-moba:

Set up an SSH tunnel using MobaXterm
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start MobaXterm.
#. Click the 'Tunnelling' icon:

   .. image:: MobaTunnelingIcon.PNG

#. The MobaSSHTunnel window will appear.

   .. image:: MobaNewSshTunnel.PNG

#. Click the 'New SSH Tunnel' button.
#. The SSH tunnel window will appear.

   .. image:: MobaNewSshTunnelConfig.PNG

#. Select 'Dynamic port forwarding (SOCKS proxy)'.
#. Enter the following configuration:

   * 'Forwarded port': ``2222``
   * 'SSH server': ``hydra-vpn.epcc.ed.ac.uk``
   * 'SSH login': ``your-hydra-vpn-username``
   * 'SSH port': ``22``

#. Click the 'Save' button.
#. Back in the MobaSSHTunnel window, in the 'Name' field, enter ``hydra-vpn``

#. Click the Start icon by the tunnel you want to start:

   .. image:: MobaStartSshTunnel.PNG

#. When prompted for your password, enter your hydra-vpn.epcc.ed.ac.uk password.
#. Click the 'OK' button.
#. Click the 'Exit' button.

In future, you can start the tunnel as follows:

#. Click the 'Tunnelling' icon.
#. The MobaSSHTunnel window will appear.
#. Click the Stop icon by the tunnel you want to stop.

In future, you can stop the tunnel as follows:

#. Click the 'Tunnelling' icon.
#. The MobaSSHTunnel window will appear.
#. Click the Stop icon by the tunnel you want to stop.

.. _ssh-tunnel-putty:

Set up an SSH tunnel using PuTTY
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start PuTTY.
#. PuTTY's Configuration should appear, showing the Session configuration.
#. In the 'HostName (or IP address)' field, enter ``hydra-vpn.epcc.ed.ac.uk``. See below.

   .. image:: PuTTY-Session-hydra-vpn.PNG

#. Click 'Connection', then 'SSH', then 'Tunnels' on the left-hand menu.
#. In the 'Source port' field, enter ``2222``
#. Click the radio button beside 'Dynamic'. See below.

   .. image:: PuTTY-Connection-SSH-tunnels-hydra-vpnCapture.PNG

#. Press the 'Add' button. ``D2222`` will be added to the list of 'Forwarded ports'. See below.

   .. image:: PuTTY-Add-dynamic.PNG

#. Press the 'Open' button.
#. A PuTTY terminal window will appear. This contains a login prompt. See below.

   .. image:: PuTTY-hydra-terminal.PNG

#. Enter your hydra-vpn.epcc.ed.ac.uk username and password.

Now, skip down to :ref:`modify-hosts`.

.. _ssh-tunnel-putty-prompt:

Set up an SSH tunnel using PuTTY and the Command Prompt
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start a Command Prompt.
#. Enter the command::

    putty.exe -ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk -D 2222

#. Enter your hydra-vpn.epcc.ed.ac.uk username and password.

Now, skip down to :ref:`modify-hosts`.

.. _ssh-tunnel-git:

Set up an SSH tunnel using Git for Windows
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start a Git Bash command prompt:

   - Either, select Start => 'Git' => 'Git Bash'.
   - Or, enter ``Git Bash`` into the toolbar search box.

#. Enter the command::

    ssh -D 2222 <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk

Now, skip down to :ref:`modify-hosts`.

.. _ssh-tunnel-ssh:

Set up an SSH tunnel using ssh
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Open a Terminal.
#. Enter the command::

    ssh -D 2222 <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk

.. _modify-hosts:

Modify the hosts file
----------------------

The ``hosts`` file helps to resolves domain names without going via a DNS server. If IP address is found for a domain name then that domain name is used. Here, it is used to map Urika's IP addresses to domain names.

#. Edit the ``hosts`` file. This can be found in the following location:

   - Windows: ``C:\Windows\System32\drivers\etc\hosts``
   - MacOS: ``/etc/hosts``
   - Linux: ``/etc/hosts``

#. Add the following lines::

    172.24.40.11 urika1.turing.ac.uk
    172.24.40.12 urika2.turing.ac.uk

If you cannot find the ``hosts`` file, or do not have the privileges to modify this file, then please contact your local systems administrator for help.

Here is an example file with these lines added ::

    # Copyright (c) 1993-2009 Microsoft Corp.
    #
    # This is a sample HOSTS file used by Microsoft TCP/IP for Windows.
    #
    # This file contains the mappings of IP addresses to host names. Each
    # entry should be kept on an individual line. The IP address should
    # be placed in the first column followed by the corresponding host name.
    # The IP address and the host name should be separated by at least one
    # space.
    #
    # Additionally, comments (such as these) may be inserted on individual
    # lines or following the machine name denoted by a '#' symbol.
    #
    # For example:
    #
    #      102.54.94.97     rhino.acme.com          # source server
    #       38.25.63.10     x.acme.com              # x client host
    
    # localhost name resolution is handled within DNS itself.
    #	127.0.0.1       localhost
    #	::1             localhost
    172.24.40.11 urika1.turing.ac.uk
    172.24.40.12 urika2.turing.ac.uk

.. _configure-browser:

Configure web browser to access Urika's applications software
-------------------------------------------------------------

Once you have set up an SSH tunnel and modified the ``hosts`` file, you now need to configure your web browser to access Urika's applications software.

If you are a Windows, MacOS or Linux user, you can:

* :ref:`configure-firefox`.

If you are a Windows user, you can alternatively:

* :ref:`configure-ie-chrome-windows`.

.. _configure-firefox:

Configure Mozilla Firefox
^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start Firefox.
#. Open the advanced network settings:

   * If using Firefox Quantum 60.0:

     #. Select Menu => 'Options'
     #. Scroll down to Network Proxy
     #. Click 'Settings...

   * If using Firefox ESR 52.2.0:

     #. Select Menu => 'Preferences'
     #. Click 'Advanced'
     #. Click 'Network'
     #. Click 'Settings...', next to 'Configure how Firefox connects to the Internet'. See below.

        .. image:: Firefox-options-advanced-network.PNG

#. Click the radio button for 'Manual proxy configuration:'. 
#. In the 'SOCKS Host' field, enter ``localhost``
#. In the adjoining 'Port:' field, enter ``2222``. 
#. Click the radio button for 'SOCKS v5'. 
#. In the 'No proxy for:' field, enter ``localhost, 127.0.0.1, .com, .io, .net, .org``. See below.

   .. image:: Firefox-settings.PNG

#. Press 'OK'.

Now, skip down to :ref:`use-browser`.

.. _configure-ie-chrome-windows:

Configure Internet Explorer or Google Chrome on Windows
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Both Internet Explorer and Google Chrome use Windows Internet Options.

**Note:** Changing the Internet Options affects Windows as a whole. You may want to :ref:`configure-firefox` and use it instead if you do not want a system-wide change.

#. Open Internet Options:

   * Via Toolbar Search box:

     - Enter 'Internet Options'

   * Via Windows Control Panel:

     #. Click 'Network and Internet'
     #. Click 'Internet Options'

   * Via Internet Explorer:

     * Select Cog icon => 'Internet options'

   * Via Google Chrome:

     #. Click 'Settings'
     #. Click 'Advanced'
     #. Click 'System'
     #. Click 'Open proxy settings'

#. Click 'Connections'. See below.

   .. image:: Windows-InternetOptions-Connections.PNG

#. Click 'LAN settings'.
#. Click the radio button for 'Use a proxy server for your LAN...'. See below.

   .. image:: Windows-InternetOptions-Connections-Advanced.PNG

#. Click 'Advanced'.
#. In the SOCKS field, enter: ``localhost``
#. In the adjoining field, enter: ``2222``
#. In the 'Exceptions:' field, enter: ``*.local; localhost; 127.0.0.1;*.com;*.io;*.net;*.org``. See below.

   .. image:: Windows-InternetOptions-Connections-Advanced-Proxy.PNG

#. Click the 'OK' button
#. Click the 'OK' button

Now, skip down to :ref:`use-browser`.

.. _use-browser:

Use web browser to access Urika's applications software
-------------------------------------------------------

Once you have set up an SSH tunnel, modified the ``hosts`` file and configured your web browser, you can now use your web browser to connect to Urika's applications software user interface.

Enter::

    http://urika1.turing.ac.uk/home

into your browser and the following view of Urika's user interface will appear.

.. image:: urika.PNG

If you are using Internet Explorer or Google Chrome and you get a warning that ``This site is not secure`` appears:

#. Click 'More information'
#. Click 'Go on to the webpage (not recommended)'

.. _connect-cli:

Connect to Urika via the command-line
-------------------------------------

The commands above to :ref:`setup-ssh-tunnel` also connect to hydra-vpn.epcc.ed.ac.uk via the command-line.

If you do not care about tunnelling or using a web browser then the commands are simpler.

If you are a Windows user, you can do one of:

* :ref:`connect-urika-moba`.
* :ref:`connect-urika-putty`.
* :ref:`connect-urika-putty-prompt`.
* :ref:`connect-urika-git`.

If you are a MacOS or Linux user, you can:

* :ref:`connect-urika-ssh`.

.. _connect-urika-moba:

Connect to Urika using MobaXterm
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start MobaXterm.
#. Click the 'Session' icon:

   .. image:: MobaSessionIcon.PNG

#. The Session Settings window will appear. 
#. Click the 'SSH' icon:

   .. image:: MobaSshIcon.PNG

#. The Basic SSH settings will appear.

   .. image:: MobaSshSessionConfig.PNG

#. Click the 'Specify username' checkbox so it is checked.
#. Enter the following configuration:

   - 'Remote host': ``urika1``
   - 'Specify username': ``your-urika-username``
   - 'Port': ``22``

#. Click the 'Network settings' tab.
#. Click the 'Connect through SSH gateway (jump host)' checkbox so it is checked.
#. Enter the following configuration:

   - 'Gateway SSH server': ``hydra-vpn.epcc.ed.ac.uk``
   - 'Specify username': ``your-hydra-vpn-username``
   - 'Port': ``22``

#. Click the 'OK' button.
#. When prompted for your password, enter your hydra-vpn.epcc.ed.ac.uk password.
#. A terminal window will appear.
#. When prompted for your password, enter your Urika password.

To connect in future:

#. Double-click on ``urika1 (your-urika-username)`` in the 'User sessions' area on the left-hand side of the MobaXterm window.
#. When prompted for your password, enter your hydra-vpn.epcc.ed.ac.uk password.
#. A terminal window will appear.
#. When prompted for your password, enter your Urika password.

.. _connect-urika-putty:

Connect to Urika using PuTTY
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start PuTTY.
#. PuTTY's Configuration should appear, showing the Session configuration.
#. In the 'HostName (or IP address)' field, enter ``hydra-vpn.epcc.ed.ac.uk``. See below.

   .. image:: PuTTY-Session-hydra-vpn.PNG

#. Press the 'Open' button.
#. A PuTTY terminal window will appear. This contains a login prompt. See below.

   .. image:: PuTTY-hydra-terminal.PNG

#. Enter your hydra-vpn.epcc.ed.ac.uk username and password.

Now, skip down to :ref:`connect-urika-hydra`.

.. _connect-urika-putty-prompt:

Connect to Urika using PuTTY and the Command Prompt
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start a Command Prompt.
#. Enter the command::

    putty.exe -ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk

#. Enter your hydra-vpn.epcc.ed.ac.uk username and password.

Now, skip down to :ref:`connect-urika-hydra`.

.. _connect-urika-git:

Connect to Urika using Git for Windows
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Start a Git Bash command prompt:

   - Either, select Start => 'Git' => 'Git Bash'.
   - Or, enter ``Git Bash`` into the toolbar search box.

#. Enter the command::

    ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk

Now, skip down to :ref:`connect-urika-hydra`.

.. _connect-urika-ssh:

Connect to Urika using ssh
^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Open a Terminal.
#. Enter the command::

    ssh <your-hydra-vpn-username>@hydra-vpn.epcc.ed.ac.uk

.. _connect-urika-hydra:

Connect to Urika from hydra-vpn.epcc.ed.ac.uk
---------------------------------------------

Once you have logged in to hydra-vpn.epcc.ed.ac.uk, you can log into Urika, by connecting to one of its login nodes, via the command-line, as follows.

Either, enter::

    ssh <your-urika-username>@u1

Or, enter::

    ssh <your-urika-username>@u2

When prompted, enter the password for your **Urika** account.

You will be presented with the Urika command line.

**Note: Urika's login nodes**

Urika has 2 login nodes:

* ``urika1``: Alias: ``u1`` (as used above). IP address: 172.24.40.11.
* ``urika2``: Alias: ``u2`` (as used above). IP address: 172.24.40.12.

.. tested-platforms:

Tested platforms and tools
--------------------------

These instructions have been tested on the following platforms and tools.

* Operating systems:

  - Windows 10 Enterprise.
  - `CentOS <https://www.centos.org>`_ Linux release 7.4.1708 (Core) virtual machine running under VMWare Workstation 14 on Windows 10 Enterprise.

* SSH clients:

  - `MobaXterm <https://mobaxterm.mobatek.net/>`_ Personal Edition v10.9 Build 3656.
  - `Putty <https://putty.org>`_ 0.70 64-bit Windows.
  - `Git for Windows <https://git-for-windows.github.io/>`_ 2.15.1 on Windows 10 Enterprise.
  - OpenSSH_7.6p1, OpenSSL 1.0.2m  2 Nov 2017, provided in Git fot Windows 2.15.1.
  - OpenSSH_7.6p1, OpenSSL 1.0.2m  2 Nov 2017, provided in CentOS 7.

* Web browsers:

  - `Mozilla Firefox <https://www.mozilla.org/en-US/firefox/>`_:

    * Quantum 60.0 (64-bit) under Windows 10 Enterprise.
    * ESR 52.2.0 (64-bit) under CentOS 7.

  - Internet Explorer 11 under Windows 10 Enterprise.
  - `Google Chrome <https://www.google.co.uk/chrome/>`_ 66 under Windows 10 Enterprise.

Use of SSH keys
---------------

Using SSH keys with an SSH Agent can be used to make access to resources such as Urika more convenient.  Further information on how to do this is available in the `Cirrus HPC service documentation <https://cirrus.readthedocs.io/en/latest/user-guide/connecting.html#making-access-more-convenient-using-a-ssh-agent>`_.
