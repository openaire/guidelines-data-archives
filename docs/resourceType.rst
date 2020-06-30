.. _dci:resourcetype:

10. ResourceType (M, 1)
--------------------
A description of the resource.

**Allowed values, examples, other constraints**

Use the label of the resource type term as value. In the below table the preferred english labels are listed, but labels (preferred or alternative) in other languages can be chosen from the COAR Resource Type Vocabulary.

10.1 resourceTypeGeneral (M, 1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The main category the described resource belongs to.

*Controlled List Values:*

* ``literature``
* ``dataset``
* ``software``
* ``other``

Attribute uri (M, 1)

Use terms from the COAR Resource Type Vocabulary.

.. include:: vocabularies/resourcetype.rst

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <resourceType resourceTypeGeneral="dataset" uri=" 	http://purl.org/coar/resource_type/c_cb28">clinical trial</resourceType>

