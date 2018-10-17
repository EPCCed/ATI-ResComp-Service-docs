SAFE for Individual Users
=========================

The Turing's `SAFE <https://safe.epcc.ed.ac.uk/ati>`_ is an online user
service management system. Through SAFE, individual users can request
machine accounts, reset passwords, see available resources and track
their usage. All users must be registered on SAFE before they can apply
for accounts on the machines in the Turing's Research Computing Service.

Registering, logging in, passwords
----------------------------------

.. _register:

Register on SAFE
~~~~~~~~~~~~~~~~

#. Go to SAFE `New User Signup
   Form <https://safe.epcc.ed.ac.uk/ati/signup.jsp>`__
#. Fill in your personal details. You can come back later and change
   them if you wish
#. Click "Register"
#. You are now registered. Your SAFE password will be emailed to the
   email address you provided. You can then login with that email
   address and password

At this point your account is registered on SAFE but you do not
have a machine account on the Turing's Research Computing Service.

To obtain a machine account on the Turing's Research
Computing Service you require a 
*Project Code*. Your project's PI or Project Manager should be able to
supply you with these details. Once you have them you should:

#. :ref:`login`.
#. :ref:`request-machine-account`.

.. _login:

Login to SAFE
~~~~~~~~~~~~~

#. Go to `SAFE <https://safe.epcc.ed.ac.uk/ati>`_ 
#. Type in the email address you have registered with.
#. Type in your SAFE password.
#. Click "Login".
#. You are now on the Main Page and here you can see menus along the top
   which give access to SAFE functionality.

.. _change-details:

Change your personal details on SAFE
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Go to the menu *Your details* and select *Update personal details*
#. Make the changes you wish
#. Click *Commit Update* to save the changes
#. Go back to *Your details* and you will see the revised information

Do not forget the last step, or nothing will happen.

**Note:** your postal address does not automatically include the name
of your department and institution; if you want these in your postal
address, you must type them again.

.. _change_email:

Change your email address on SAFE
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Go to the menu *Your details* and select *Update email*
#. Enter the new email address and click *Request*

A verification email will then be sent to the new email address. This
email contains a link which you must use to verify your new address. On
acknowledging your new address the change will be committed and you must
use the new email address when logging into SAFE.

.. _change-passwd:

Change your SAFE password
~~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Go to the menu *Your details* and select *Change SAFE password*
#. Fill in the boxes and click *Change*

.. _reset-passwd:

Reset your SAFE password
~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Enter your email address
#. Click *Email*
#. The SAFE will mail your password to your email address.

SAFE will only mail to email addresses it already knows. But email is
not a secure medium, so if you change your password this way, you should
immediately change it again from inside SAFE. 

**Note:** anyone could go to SAFE, type your email address and request
a new password by clicking "Email". If that happens you will receive
an email message out of the blue saying that your password has been
changed. In this case you should change your password again as soon as
possible.

.. _request-machine-account:

Request an account for a Research Computing Service machine 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Go to the menu *Login accounts* and select *Request login account*
#. Choose the project code for the machine you want from the *Project*
   pull-down list.
#. Then press *Select Project*. A new screen will appear.
#. Press the radio button next to the machine you want the account 
   for then press  *Select Machine*.
#. In the field next to *Request username*, enter the username you
   would prefer to use on this machine.

   Every username must be unique, and you must create a new machine
   account with a unique username for each project you work on.
   Usernames cannot be used on multiple projects, even if the previous
   project has finished.

#. Accept the Terms and Conditions of Access by clicking the
   appropriate button.

When you do this, you will be sent an acknowledgment by email, which
will include your SAFE password — you should change this as soon as
possible. 

You will have to wait for your PI or project manager to accept your
request to register. When this has happened, the systems team are
prompted to create your account on the machine. Once this has been
done, you will be sent an email. You can then
:ref:`get-machine-passwd` from your SAFE account.

.. _get-machine-passwd:

Get your password for the service machine
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Wait till you receive the email with your details. Then:

#. :ref:`login`.
#. Go to the menu *Login accounts* and you will see your account on the
   machine listed. Click *username*
#. This will display details of your account. Click *View Login Account
   Password* You will need to enter in your SAFE password and then click
   *view*, and you will see your password to the machine

This password is generated randomly by SAFE. It's best to
copy-and-paste it across when you login to the machine.

.. _reset-machine-passwd:

Reset the password on your machine account
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you have forgotten your current password, or it has expired, then
you can ask for it to be reset:

#. :ref:`login`.
#. Go to the menu *Login accounts* and select the account you need the
   new password for
#. Click *username* which displays details of this machine
   account.
#. Click *New Login Account Passwd*

The systems team will change your password. When this has been done,
you will be informed by email; this means that you can come back to
SAFE and :ref:`get-machine-passwd`.

.. _change-machine-passwd:

Change a password on your machine account
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This is machine-specific.

**Note:** When you change your password on machines in this way, the
changes are **not** reflected on SAFE, so please remember your new
password.

**hydra-vpn.epcc.ed.ac.uk gateway**:

#. At the command-line, run::

    passwd

#. You will be prompted to enter your old password.
#. You will be prompted to enter your new password twice.

**Alan Turing Institute Cray Urika-GX Service**:

#. At the command-line, run::

    change_ldap_passwd

#. You will be prompted to enter your new password twice.
#. You will be prompted to enter your old password.

**Atiras portal:**

#. Go to the Atiras portal home page.
#. Click the menu labelled by your username at the top-right of the page. 
#. Select 'Settings'.   
#. Fill in the following fields: 
    - 'Current Password' 
    - 'New Password' 
    - 'Confirm New Password' 
#. Click 'Update Password'.   

**Atiras Secure Safe Haven and build arena virtual machines**:

If running a SSH (secure shell) session, or from terminal window in an
RDP (remote desktop) session:

#. Run:: 
 
    passwd 
 
#. You will be prompted to enter your old password. 
#. You will be prompted to enter your new password twice. 

Alternatively, if running an RDP (remote desktop) session:

#. Click the button icon on the top right hand side of the desktop.
#. You will be presented with a dialog box. Click your user name then
   select 'Account Settings'. 
#. Click '<your-virtual-machine-username>' on the row of user names.
#. Click the button (with five blobs) next to the 'Password' field.
#. Fill in the following fields:
    - 'Current Password'
    - 'New Password'
    - 'Verify New Password'
#. Click 'Change'. 

User Mailing Options
--------------------

.. _view-mailings:

View user mailings
~~~~~~~~~~~~~~~~~~

All mailings are archived and can be viewed in `SAFE <https://safe.epcc.ed.ac.uk/ati>`_. 

#. :ref:`login`. 
#. Go to the section *View user mailings*.
#. Press the *View* button to access the mailings.

.. _subscribe-mail:

Join, or leave, a mailing list
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There are three mailing lists available.

- *Major Announcements* mailings contain information on major service
  upgrades and future plans. All users are subscribed to this list by
  default.
- *Service News* mailings contain information on training courses,
  newsletters, events, and other general announcements. All users are
  subscribed to this list by default.
- *System Status Notifications* inform users when the service goes up
  or down, including the reminders of the next planned maintenance
  shutdowns. Users are not subscribed to this list by default. You
  will need to explicitly subscribe to this list if you wish to
  receive these emails.

You can subscribe to any combination of these email lists via SAFE:

#. :ref:`login`.
#. Go to the menu *Your details* click *Email list settings*
#. In the panel headed *Mailing list preferences* click on the mailing
   lists you would like to subscribe to.
#. Click *Update List Preferences*

If you wish to unsubscribe from user mailings completely:

#. Click on the menu *Your details* click *Update personal details* find
   *Opt out of user emails* field and click it.
#. Click *Commit Update*. Do not forget this step, or nothing will
   happen.

**Note:** This overrides any option enabled in *Mailing list
preferences* panel.

**Note:** Regardless of whether you are subscribed to a particular
mailing list, you can still view **all** user mailings which have been
sent, from within SAFE. See :ref:`view-mailings` for details.

Tracking and Managing Available Resources
-----------------------------------------

.. _check-resources:

Check how much time and space are available to you
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Go to the menu *Login accounts*.
#. Select the *username* which you wish to see details for.

You will then see the information for this account. You will see the
quotas for disk space (if your project group is using these) and how
much is in use.

You can also see which file systems your project is using. Under the
heading *Volume* you will see entries for RDF (if used by your
project), *home* and *work* and in brackets after each, the name of
the file system they are hosted on, followed by the current usage by
your project, and total quota.

The budget values displayed are updated every morning, and the values
shown for disk use are updated four times a day. For this reason, all
these values may not be completely up-to-date. If there is a lot of
activity in your project, the numbers shown could be significantly
different from from the current ones.

.. _request-resources:

Request more kAUs/disk space
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In the first instance, please contact the principal investigator, or
the project manager of your project. The PI will then take the
necessary steps to either allocate you more resources out of the
project reserve, or to request an increase from the helpdesk/research
councils.

The helpdesk does not own project resources and has no authority to
allocate them to individual users. This responsibility lies with the
project PI/project manager.

.. _review-usage:

Review the use you have made of the service, or the activity of the service as a whole
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Go to the menu *Service information* and select *Report Generator*.
#. Select the report you wish to run and the format you want the output
   in (web, PDF, CSV, XML) by clicking the appropriate icon in the list.
#. Complete the required information in the form: this will usually
   consist of at least a date range to analyse and may have other
   options depending on the report you are running.
#. Click *Generate Report*.

If you are a PI or Project Manager, you will have access to additional
reports to generate information on whole projects or groups as well as
your own usage and the usage of the service as a whole.

Miscellaneous
-------------

.. check_queries:

Check the queries you have submitted to the helpdesk
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Go to the menu *Help and Support* and select *Your support
   requests*. 
#. Click the number of a query to check the contents of the query
   log. 

This will show you the queries of yours that haven't yet been resolved.

**Note:** some of the internal correspondence about a query will not
be shown.

You can also use SAFE to submit a query — use *New support request*.

.. _feedback:

Register your approval — or your annoyance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. :ref:`login`.
#. Go to the menu *Help and Support* and select *Service feedback*.
#. Click on the scale somewhere between 5 penalty points and 5 gold
   stars indicating your level of anger or delight.
#. Optionally: enter a comment in the comment box.
#. Click *Set Token*.

The tokens may appear in the public service reports, although your
name will not be published with them. Although an entry in the comment
field is optional, it necessarily gives greater weight to your
feelings - without it we cannot tell why you have set a token. 
