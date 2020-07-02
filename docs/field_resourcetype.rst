.. _dci:resourcetype:

Resource Type (M, 1)
--------------------

``datacite:resourceType``

A declaration of the resource's type.

Property resourceType (M, 1)
----------------

*Allowed values, examples, other constraints:*

Use the label of the resource type term as value. In the below table the preferred English labels are listed, but labels (preferred or alternative) in other languages can be chosen from the COAR Resource Type Vocabulary.

Attribute resourceTypeGeneral (M, 1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The main category the described resource belongs to.

*Controlled list values:*

* ``literature``
* ``dataset``
* ``software``
* ``other``

Attribute uri (M, 1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use terms from the COAR Resource Type Vocabulary.

.. include:: vocabularies/resourcetype.rst

Examples
-------

.. code-block:: xml
   :linenos:

   <resourceType resourceTypeGeneral="dataset" uri="http://purl.org/coar/resource_type/c_cb28">clinical trial</resourceType>

Context
-------

**Do Not Confuse With**



**DataCite v4.3 Differentiation**



**OpenAIRE Data Guidelines v2 Differentiation**
