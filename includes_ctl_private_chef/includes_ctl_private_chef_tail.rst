.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for Private Chef, an early version of the Chef Server.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The ``tail`` subcommand is used to follow all |chef server oec| logs for all services. This command can also be run for an individual service by specifying the name of the service in the command. 

This subcommand has the following syntax:

.. code-block:: bash

   $ private-chef-ctl tail name_of_service

where ``name_of_service`` represents the name of any service that is listed after running the ``service-list`` subcommand.
