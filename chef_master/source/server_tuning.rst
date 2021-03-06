=====================================================
Server Tuning
=====================================================

.. include:: ../../includes_server_tuning/includes_server_tuning.rst

.. note:: |note enterprise_chef_tuning|


Customize the Config File
=====================================================
.. include:: ../../includes_config/includes_config_rb_server.rst

Use Conditions
-----------------------------------------------------
.. include:: ../../step_config/step_config_add_condition.rst


Recommended Settings
=====================================================
.. include:: ../../includes_server_tuning/includes_server_tuning_general.rst

SSL Protocols
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_nginx.rst

Optional Settings
=====================================================
The following settings are often used to for performance tuning of the |chef server| in larger installations.

.. note:: When changes are made to the |chef server rb| file the |chef server| must be reconfigured by running the ``chef-server-ctl reconfigure`` command.

bookshelf
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_bookshelf.rst

opscode-chef
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_chef.rst

opscode-erchef
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_erchef.rst

opscode-expander
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_expander.rst

opscode-solr4
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_solr.rst

Update Frequency
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_server_tuning/includes_server_tuning_solr_update_frequency.rst

postgresql
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_postgresql.rst

rabbitmq
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_rabbitmq.rst
