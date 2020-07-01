.. _dci:identifier:

Identifier (M, 1)
==============

``datacite:identifier``

The identifier is a unique string that identifies a resource.

Property identifier (M, 1)
----------------

**Allowed values, examples, other constraints**

Format should be “10.1234/foo”.

.. _d:identifiertype:

Attribute identifierType (M, 1)
-----------------------

The type of the identifier.

**Allowed values, examples, other constraints**

*Controlled list values (DataCite)*

* DOI

*Controlled list values (OpenAIRE)*

* ARK
* DOI
* Handle
* PURL
* URN
* URL

Example
-------

.. code-block:: xml
   :linenos:

   <identifier identifierType="DOI">10.5281/zenodo.44383</identifier>
   
Context
-------

**Do Not Confuse With**



**DataCite v4.3 Differentiation**

* Unlike DataCite, OpenAIRE allows for DOIs and other types of identifiers also.

**OpenAIRE Data Guidelines v2 Differentiation**
