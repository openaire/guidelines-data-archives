.. _dci:identifier:

Identifier (M, 1)
==============

``datacite:identifier``

The identifier is a unique string that identifies a resource.

Property identifier (M, 1)
----------------

*Allowed Values, Other Constraints*

* Format should be “10.1234/foo” (in the case of DOIs).

.. _d:identifiertype:

Attribute identifierType (M, 1)
~~~~~~~~~~~~~~~~

The type of the identifier.

*Controlled List Values (DataCite)*

* DOI

*Controlled List Values (OpenAIRE)*

* ARK
* DOI
* Handle
* PURL
* URN
* URL

Examples
-------

.. code-block:: xml
   :linenos:

   <identifier identifierType="DOI">10.5281/zenodo.44383</identifier>
   
Context
-------

**Do Not Confuse With**

* :ref:`dci:relatedIdentifier` (Use ``relatedIdentifier`` for to indicate related resources, as e.g. cited or citing resources.)
* :ref:`dci:alternativeIdentifier` (Use ``alternateIdentifier`` for secondary or local identifiers of the same resource, and also for landing pages and download pages.)

**DataCite v4.3 Differentiation**

* Unlike DataCite, OpenAIRE allows for DOIs and other types of identifiers also.

**OpenAIRE Data Guidelines v2 Differentiation**
