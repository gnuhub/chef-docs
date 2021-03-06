.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

|description resource_attributes_intro|

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``admin``
     - Use to specify whether the |chef client| is an API client.
   * - ``allow_overwrite_keys``
     - Use to overwrite the key on a machine when it is different from the key specified by ``source_key``.
   * - ``attribute``
     - Use to specify a path to an attribute, and then modify that attribute with the specified value. Each modified attribute should be specified separately. This attribute should not be used in the same recipe as ``attributes``.
   * - ``attributes``
     - Use to specify a |ruby hash| that contains all of the attributes to be applied to a machine. This attribute should not be used in the same recipe as ``attribute``.
	   SEE NOTES.
   * - ``chef_environment``
     - |name environment|
   * - ``chef_server``
     - |chef_server_url|
   * - ``complete``
     - Use to specify if all of the normal attributes specified by this resource represent a complete specification of normal attributes for a machine. When ``true``, any attributes not specified will be reset to their default values. For example, if a |resource machine| resource is empty and sets ``complete`` to ``true``, all existing attributes will be reset:

       .. code-block:: ruby

          machine "foo" do
            complete "true"
          end
   * - ``converge``
     - Use to manage convergence when used with the ``:create`` action. Set to ``false`` to prevent convergence. Set to ``true`` to force convergence. When ``nil``, the machine will converge only if something changes. Default value: ``nil``.
   * - ``driver``
     - Use to specify the URL for the driver to be used for provisioning.
   * - ``files``
     - A list of files to upload. Syntax: ``REMOTE_PATH => LOCAL_PATH_OR_HASH``.
       
       For example:
       
       .. code-block:: ruby
       
          files '/remote/path.txt' => '/local/path.txt'
       
       or:
       
       .. code-block:: ruby
       
          files '/remote/path.txt' => { :local_path => '/local/path.txt' }
       
       or:
       
       .. code-block:: ruby
       
          files '/remote/path.txt' => { :content => 'foo' }
   * - ``from_image``
     - Use to specify an image created by the |resource machine_image| resource.
   * - ``machine_options``
     - A |ruby hash| that is specifies driver options.
   * - ``name``
     - The name of the machine.
   * - ``ohai_hints``
     - |hint| For example: ``'ec2' => { 'a' => 'b' } creates file ec2.json with json contents { 'a': 'b' }``.
   * - ``private_key_options``
     - Use to generate a private key of the desired size, type, and so on.
   * - ``public_key_format``
     - Use to specify the format of a public key. Possible values: ``pem`` and ``der``. Default value: ``pem``.
   * - ``public_key_path``
     - The path to a public key.
   * - ``raw_json``
     - The machine as |json| data. For example:
       
       .. code-block:: javascript
       
		  {
		    "name": "node1",
		    "chef_environment": "_default",
		    "json_class": "Chef::Node",
		    "automatic": {
		      "languages": {
		        "ruby": {
		          ...
		        },
				...
          ...
          }
   * - ``recipe``
     - Use to add a recipe to the run-list for a machine. Use this attribute multiple times to add multiple recipes to a run-list. Use this attribute along with ``role`` to define a run-list. The order in which the ``recipe`` and ``role`` attributes are specified will determine the order in which they are added to the run-list. This attribute should not be used in the same recipe as ``run_list``. For example:
       
       .. code-block:: ruby
       
          recipe 'foo'
          role 'bar'
          recipe 'baz'
   * - ``remove_recipe``
     - Use to remove a recipe from the run-list for the machine.
   * - ``remove_role``
     - Use to remove a role from the run-list for the machine.
   * - ``remove_tag``
     - Use to remove a tag.
   * - ``role``
     - Use to add a role to the run-list for the machine. Use this attribute multiple times to add multiple roles to a run-list. Use this attribute along with ``recipe`` to define a run-list. The order in which the ``recipe`` and ``role`` attributes are specified will determine the order in which they are added to the run-list. This attribute should not be used in the same recipe as ``run_list``. For example:
	 
       .. code-block:: ruby
       
          recipe 'foo'
          role 'bar'
          recipe 'baz'
   * - ``run_list``
     - Use to specify the run-list to be applied to the machine. This attribute should not be used in the same recipe as ``recipe`` and ``role``.

       .. include:: ../../includes_node/includes_node_run_list.rst
       
       .. include:: ../../includes_node/includes_node_run_list_format.rst

   * - ``source_key``
     - Use to copy a private key, but apply a different ``format`` and ``password``. Use in conjunction with ``source_key_pass_phrase``` and ``source_key_path``.
   * - ``source_key_pass_phrase``
     - The pass phrase for the private key. Use in conjunction with ``source_key``` and ``source_key_path``.
   * - ``source_key_path``
     - The path to the private key. Use in conjunction with ``source_key``` and ``source_key_pass_phrase``.
   * - ``tag``
     - Use to add a tag.
   * - ``tags``
     - Use to add one (or more) tags. This will remove any tag currently associated with the machine. For example: ``tags :a, :b, :c``.
   * - ``validator``
     - Use to specify if the |chef client| is a |chef validator|.
