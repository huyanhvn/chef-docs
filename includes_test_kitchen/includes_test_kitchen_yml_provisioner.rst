.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


|kitchen| can configure the |chef zero| provisioner with the following |chef|-specific settings:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``chef_omnibus_url``
     - The URL for an ``install.sh`` script that will install |chef client| on the machine under test. Default value: ``https://www.chef.io/chef/install.sh``.
   * - ``client_rb``
     - A list of |client rb| file settings. For example:

       .. code-block:: yaml

          client_rb:
            audit_mode: :audit_only

   * - ``clients_path``
     - The relative path to the directory in which client data is located. This data must be defined as |json|.
   * - ``cookbook_files_glob``
     - A file glob (pattern) that matches files considered to be part of the cookbook. (Typically, this value does not need to be modified from the default.)
   * - ``data_path``
     - Use to specify the path from which non-cookbook files are copied to a |kitchen| instance.
   * - ``data_bags_path``
     - The relative path to a directory in which data bags and data bag items are defined. This data must be structured as if it were in the |chef repo|.
   * - ``driver``
     - Use to specify a driver for a platform. This will override the default driver.
   * - ``encrypted_data_bag_secret_key_path``
     - The path to an RSA key file that is used to decrypt encrypted data bag items.
   * - ``environments_path``
     - The relative path to the directory in which environment data is located. This data must be defined as |json|.
   * - ``kitchen_root``
     - The directory in which |kitchen| will stage all content on the target node. This directory should be large enough to store all the content and must be writable. (Typically, this value does not need to be modified from the default value.) Default value: ``/tmp/kitchen``.
   * - ``nodes_path``
     - The relative path to the directory in which node data is located. This data must be defined as |json|.
   * - ``require_chef_omnibus``
     - Use to install the latest version of the |chef client| in a node. Set to ``true`` to install the latest version, ``false`` to not install |chef client| (assumes the box already has it installed), or a version specifier like ``11.8.0`` to install a particular version. When set to ``true`` or a version number, the ``chef_omnibus_url`` may be used to specify the URL of an ``install.sh`` that will install the indicated version of |chef client|. Default value: ``false``.
   * - ``roles_path``
     - The relative path to the directory in which role data is located. This data must be defined as |json|.

These settings may be added to the ``provisioner`` section of the |kitchen yml| file when |chef zero| is used as the provisioner.
