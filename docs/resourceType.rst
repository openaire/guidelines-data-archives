.. _dci:resourcetype:

10. ResourceType (M, 0-1)
--------------------
A description of the resource.

**Allowed values, examples, other constraints**

The format is open, but the preferred format is a single term of some detail so that a pair can be formed with the sub-property.

10.1 resourceTypeGeneral (M)
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
