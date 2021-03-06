=====================================================
Authentication and Authorization
=====================================================

.. include:: ../../includes_chef_auth/includes_chef_auth.rst

Authentication
=====================================================
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication.rst

|chef validator|
-----------------------------------------------------
.. include:: ../../includes_security/includes_security_chef_validator.rst

During a |chef client_title| Run
-----------------------------------------------------
.. include:: ../../includes_security/includes_security_key_pairs_chef_client.rst

|knife_title|
-----------------------------------------------------
.. include:: ../../includes_security/includes_security_key_pairs_knife.rst

|knife| can also use the |subcommand knife exec| subcommand to make specific, authenticated requests to the |chef server|. |knife| plugins can also make authenticated requests to the |chef server| by leveraging the |subcommand knife exec| subcommand.

From the Web Interface
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_webui.rst

Other Options
-----------------------------------------------------
The most common ways to interact with the |chef server| using the |api chef server| abstract the API from the user. That said, the |api chef server| can be interacted with directly. The following sections describe a few of the ways that are available for doing that.

|curl|
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_other_curl.rst

|pychef|
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_other_pychef.rst

|ruby|
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_other_ruby.rst

Debug Authentication Issues
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_debug.rst

Authorization
=====================================================
.. include:: ../../includes_chef_auth/includes_chef_auth_authorization.rst

|chef server_title|
-----------------------------------------------------
.. include:: ../../includes_server_rbac/includes_server_rbac.rst

The |chef server| uses organizations, groups, and users to define role-based access control:

.. list-table::
   :widths: 60 420
   :header-rows: 1

   * - Feature
     - Description
   * - .. image:: ../../images/icon_server_organization.png
     - .. include:: ../../includes_server_rbac/includes_server_rbac_orgs.rst
   * - .. image:: ../../images/icon_server_group.png
     - .. include:: ../../includes_server_rbac/includes_server_rbac_groups.rst
   * - .. image:: ../../images/icon_server_users.png
     - .. include:: ../../includes_server_rbac/includes_server_rbac_users.rst
   * - .. image:: ../../images/icon_chef_client.png
     - .. include:: ../../includes_server_rbac/includes_server_rbac_clients.rst

.. include:: ../../includes_server_rbac/includes_server_rbac_workflow.rst

Object Permissions
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_server_rbac/includes_server_rbac_permissions_object.rst

Global Permissions
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_server_rbac/includes_server_rbac_permissions_global.rst

Node Permissions
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. note:: This is only necessary after migrating the |chef client| and/or node objects from one |chef server| to another because the permissions for the nodes must be reset.

.. include:: ../../includes_server_rbac/includes_server_rbac_permissions_client.rst

Default Groups
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_server_rbac/includes_server_rbac_groups_default.rst

Multiple Organizations
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_server_rbac/includes_server_rbac_orgs_multi.rst

.. include:: ../../includes_server_rbac/includes_server_rbac_orgs_multi_use.rst

Many Users, Same Repo
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. include:: ../../includes_chef_repo/includes_chef_repo_many_users_same_repo.rst

|api chef server|
=====================================================
.. include:: ../../includes_api_chef_server/includes_api_chef_server.rst

Authentication Headers
-----------------------------------------------------
.. include:: ../../includes_api_chef_server/includes_api_chef_server_headers.rst

Header Format
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_format.rst

Required Headers
+++++++++++++++++++++++++++++++++++++++++++++++++++++
The following authentication headers are required:

.. list-table::
   :widths: 130 400
   :header-rows: 1

   * - Feature
     - Description
   * - ``Accept``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_accept.rst
   * - ``Host``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_host.rst
   * - ``X-Chef-Version``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_chef_version.rst
   * - ``X-Ops-Authorization-N``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_authorization.rst
   * - ``X-Ops-Content-Hash``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_content_hash.rst
   * - ``X-Ops-Sign``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_sign.rst
   * - ``X-Ops-Timestamp``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_timestamp.rst
   * - ``X-Ops-UserId``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_userid.rst

Example
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_example.rst

Endpoints
-----------------------------------------------------
.. include:: ../../includes_api_chef_server/includes_api_chef_server_endpoints.rst

For more information about the |api chef server| endpoints see :doc:`api_chef_server`.

