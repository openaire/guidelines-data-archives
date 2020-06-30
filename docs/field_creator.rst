.. _dci:creator:

Creator (M)
===========

``datacite:creator``

The authors of the software in priority order. May be a corporate/institutional or personal name.

Cardinality
~~~~~~~~~~~

*Mandatory*

*Occurrence: 1-n*


Definition and Usage Instruction
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The authors of the publication in priority order. May be a corporate/institutional or personal name.

**Do Not Confuse With**

.. * :ref:`dci:contributor`
.. * :ref:`dci:publisher`

**Remarks**

* adapted from `DataCite MetadataKernel`_ v4.3


.. _datacite:creator_creatorName:

0.1 creatorName (M)
-------------------

The name of the author (occurrence: 1). 
The format should be: family, given. Non-roman names may be transliterated according to the `ALA-LC <http://www.loc.gov/catdir/cpso/roman.html>`_ schemas.

.. The name of the author.
.. Use inverted name, so the syntax will be the following: “surname”, “initials” (“first name”) “prefix”.

Distinguished by attribute:   *xml:lang*

0.1.1 nameType (R)
------------------

Attribute: The type of name (occurrence: 0-1).

.. include:: vocabularies/nametype.rst


.. _datacite:creator_givenName:

0.2 givenName (R)
-----------------

The personal or first name of the author.

.. _datacite:creator_familyName:

0.3 familyName (R)
------------------

The surname or last name of the author.

.. _datacite:creator_nameIdentifier:

0.4 nameIdentifier (R)
----------------------

Uniquely identifies an individual or legal entity, according to various schemes.

.. _datacite:creator_nameIdentifier_nameIdentifierScheme:

0.4.1 nameIdentifierScheme (R)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Attribute: The name of the name identifier scheme.
Uniquely identifies an individual or legal entity, according to various schemes (occurrences: 0-n).
The format is dependent upon scheme.

**Allowed values, examples, other constraints**

Examples:

* ``ISNI`` - |ISNI|
* ``ORCID`` - |ORCID|
* ``VIAF`` - |VIAF|
* ``ResearcherID`` - |ResearcherID|
* national organisation ID authoritative systems

.. note::
   OpenAIRE recommends including a nameIdentifier such as an ORCID or a ISNI if available.

.. _datacite:creator_nameIdentifier_schemeURI:

0.4.2 schemeURI (O)
^^^^^^^^^^^^^^^^^^^

Attribute: The URI of the name identifier scheme.

.. _datacite:creator_affiliation:

0.5 affiliation (O)
-------------------

The organizational or institutional affiliation of the creator.

**Usage Instruction**

 For example John Hubert de Smit becomes

.. code-block:: xml

  <creator>
     <creatorName>Smit, J.H. (John Hubert) de</creatorName>
  </creator>

When initials and first name are both available use this formatting:

.. code-block:: xml

  <creator>
    <creatorName>Janssen, J. (John)</creatorName>
  </creator>

Generational suffixes (Jr., Sr., etc.) should follow the surname. When in doubt, give the name as it appears, and do not invert. Omit titles (like “Dr”). For example: “Dr. John H. de Smit Jr.” becomes

.. code-block:: xml

  <creator>
    <creatorName>Smit Jr., J.H. (John) de</creatorName>
  </creator>

In the case of an organization name which clearly includes an organizational hierarchy, list the parts of the hierarchy from largest to smallest, separated by full stops.

For example:

.. code-block:: xml

  <creator>
    <creatorName>Utrecht University. Department of Computer Sciences</creatorName>
  </creator>

If it is not clear whether there is a hierarchy present, or unclear which is the larger or smaller portion of the body, give the name as it appears in the resource. Only encode organisations in this element to indicate corporate authorship, not to indicate the affiliation of an individual.

The inclusion of personal and corporate name headings from authority lists constructed according to local or national thesaurus files is optional.

It is recommended to encode thesauri with an URI, for service providers to recognise the thesaurus schema. For example:

.. code-block:: xml

  <creator>
    <creatorName>Smit Jr., J.H. (John) de</creatorName>
    <affiliation>Institute of Science and Technology</affiliation>
    <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org">
        1234-5678-0987-1234
    </nameIdentifier>
  </creator>

In cases of lesser responsibility, other than authorship, use ``datacite:contributor``. 

**Example**

.. code-block:: xml
   :linenos:

   <creator>
     <creatorName>Evans, R.J.</creatorName>
     <affiliation></affiliation>
     <nameIdentifier nameIdentifierScheme="ORCID"
                     schemeURI="http://orcid.org">
       1234-1234-1234-1234
     </nameIdentifier>
   </creator>
