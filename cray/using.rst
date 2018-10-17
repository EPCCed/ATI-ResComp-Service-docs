Using the Turing's Cray Urika-GX service
========================================

This chapter provides miscellaneous hints and tips on using the Turing's Cray Urika-GX service ("Urika").

See the chapter :doc:`connecting` for instructions on how to connect to Urika.

.. _view-doc:

View documentation
------------------

Detailed documentation on Urika and its software and services is available on the Urika home page:

#. Within a web browser, visit http://urika1.turing.ac.uk/home (see `Use web browser to access Urika's applications software <connecting.html#use-browser>`__).
#. Click on Learning Resources on the home page, or visit http://urika1.turing.ac.uk/documentation.

Submit jobs
-----------

To access notes on submitting jobs using the various job submission mechanisms available on Urika:

#. :ref:`view-doc` as described above.
#. Scroll down the page and click on "Job Submission Notes".

Alternatively, within a web browser, visit http://urika1.turing.ac.uk/static/documentation/notebooks/ATI-Job-Submission.pdf.

Open Jupyter notebook
---------------------

#. Within a web browser, visit http://urika1.turing.ac.uk/home (see `Use web browser to access Urika's applications software <connecting.html#use-browser>`__).
#. Click on the "jupyter" icon on the home page.
#. A Jupyter sign-in page will open in a new browser tab, prompting you for a Username and Password. Enter your Urika username and password.
#. Click Sign In.
#. A Jupyter notebook page will appear in a new browser tab, displaying the contents of your home directory on Urika.

Open Apache Mesos resource manager
----------------------------------

#. `Connect to Urika via the command-line <connecting.html#connect-cli>`__.
#. Get your Mesos password by running the following command::

    cat /security/secrets/<your-urika-username>.mesos

#. Within a web browser, visit http://urika1.turing.ac.uk/home (see `Use web browser to access Urika's applications software <connecting.html#use-browser>`__).
#. Scroll down the home page until you see a carousel of icons which includes "MESOS".
#. Click on the "MESOS" icon to select it.
#. Click on the "MESOS" icon again.
#. The Mesos dashboard will open in a new browser tab, with a dialog prompting you for a User Name and Password. Enter your Urika username and Mesos password.
#. The Mesos dashboard will refresh with its current data.
