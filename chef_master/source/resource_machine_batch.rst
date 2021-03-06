=====================================================
machine_batch
=====================================================


.. include:: ../../includes_resources_common/includes_resources_common_generic.rst

.. include:: ../../includes_resources/includes_resource_machine_batch.rst

.. note:: |warning provisioning|


Syntax
=====================================================
.. include:: ../../includes_resources/includes_resource_machine_batch_syntax.rst

Actions
=====================================================
.. include:: ../../includes_resources/includes_resource_machine_batch_actions.rst

In-Parallel Processing
-----------------------------------------------------
.. include:: ../../includes_provisioning/includes_provisioning_parallel.rst

Attributes
=====================================================
.. include:: ../../includes_resources/includes_resource_machine_batch_attributes.rst

Providers
=====================================================
.. include:: ../../includes_resources_common/includes_resources_common_provider.rst

.. include:: ../../includes_resources_common/includes_resources_common_provider_attributes.rst

.. include:: ../../includes_resources/includes_resource_machine_batch_providers.rst

Examples
=====================================================
|generic resource statement|

**Set up multiple machines, in-parallel**

.. include:: ../../step_resource/step_resource_machine_batch_setup_n_machines.rst

**Converge multiple machines, in-parallel**

.. include:: ../../step_resource/step_resource_machine_batch_converge_n_machines.rst

**Stop multiple machines, in-parallel**

.. include:: ../../step_resource/step_resource_machine_batch_stop_n_machines.rst

**Destroy multiple machines, in-parallel**

.. include:: ../../step_resource/step_resource_machine_batch_destroy_n_machines.rst

**Destroy all machines**

.. include:: ../../step_resource/step_resource_machine_batch_destroy_all_machines.rst

**Converge multiple machine types, in-parallel**

.. include:: ../../step_resource/step_resource_machine_batch_multiple_machine_types.rst

**Set up primary and secondary machines for high availability**

.. include:: ../../step_resource/step_resource_machine_batch_setup_primary_and_secondary.rst