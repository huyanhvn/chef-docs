.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``GET`` method is used to view all of the key-value pairs in a data bag item.

This method has no parameters.

**Request**

.. code-block:: xml

   GET /organizations/NAME/data/NAME/ITEM

**Response**

The response is similar to:

.. code-block:: javascript

   {
     "real_name": "Adam Jacob",
     "id": "adam"
   }

**Response Codes**

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - |response code 200 ok|
   * - ``401``
     - |response code 401 unauthorized|
   * - ``403``
     - |response code 403 forbidden|
   * - ``404``
     - |response code 404 not found|
