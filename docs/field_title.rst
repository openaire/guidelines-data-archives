.. _dci:title:

.. _dci:title_title:

Title (M, 1-n)
==============

``datacite:title``

A name or title by which a resource is known.
Use the title name as value. Repeat this property for titles of different types or in different languages.

Property title (M, 1-n)
----------------

Attribute xml:lang (R, 0-1)
~~~~~~~~~~~~~~~~

The language of the title.

**Allowed values, examples, other constraints**

The value of the attribute should be chosen from IETF BCP 47, the `IANA Language Subtag Registry <http://www.iana.org/assignments/language-subtag-registry>`_.

Attribute titleType (O, 0-1)
~~~~~~~~~~~~~~~~

The title's type.

**Allowed values, examples, other constraints**

.. include:: vocabularies/titletype.rst

Examples
-------

.. code-block:: xml
   :linenos:

    <datacite:title xml:lang="en-US">
     National Institute for Environmental Studies and Center
     for Climate System Research Japan
    </datacite:title>
    <datacite:title xml:lang="en-US" titleType="Subtitle">A survey</datacite:title>

.. _DataCite MetadataKernel: http://schema.datacite.org/meta/kernel-4.3/

Context
-------

**Do Not Confuse With**



**DataCite v4.3 Differentiation**

* OpenAIRE recommends indicating the title's language.

**OpenAIRE Data Guidelines v2 Differentiation**
