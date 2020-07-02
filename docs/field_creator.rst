.. _dci:creator:

Creator (M, 1-n)
===========

``datacite:creator``

The authors of the research output in priority order. May be corporate/institutional or personal creators.

.. _datacite:creator_creatorName:

Property creator (M, 1-n)
----------------

A single creator.

Subproperty creatorName (M, 1)
~~~~~~~~~~~~~~~~

The name of the author. 

*Allowed values, other constraints:*

* Personal names:

  * The format should be: family, given. When in doubt, give the name as it appears, and do not invert.
  * Omit titles (like “Dr”).
 
* Organizational names:

  * In the case of an organization name which clearly includes an organizational hierarchy, list the parts of the hierarchy from largest to smallest, separated by full stops.
  * If it is not clear whether there is a hierarchy, or unclear which is the larger or smaller portion of the body, give the name as it appears in the resource. Only encode organisations in this element to indicate corporate authorship, not to indicate the affiliation of an individual. 
* Non-roman names may be transliterated according to the `ALA-LC <http://www.loc.gov/catdir/cpso/roman.html>`_ schemas. 
* The inclusion of personal and corporate name headings from authority lists constructed according to local or national thesaurus files is optional.

.. The name of the author.
.. Use inverted name, so the syntax will be the following: “surname”, “initials” (“first name”) “prefix”.

Attribute xml:lang (O, 0-1)
^^^^^^^^^^^^^^^^^

The language in which the name is given.

Attribute nameType (R, 0-1)
^^^^^^^^^^^^^^^^^

The type of name denotes whether the creator is corporate/institutional or personal.

.. include:: vocabularies/nametype.rst

.. _datacite:creator_givenName:

Subproperty givenName (R, 0-1)
~~~~~~~~~~~~~~~~

The personal or first name of the author.

.. _datacite:creator_familyName:

Subproperty familyName (R, 0-1)
~~~~~~~~~~~~~~~~

The surname or last name of the author.

.. _datacite:creator_nameIdentifier:

Subproperty nameIdentifier (R, 0-n)
~~~~~~~~~~~~~~~~

Uniquely identifies an individual or legal entity, according to various schemes.

.. _datacite:creator_nameIdentifier_nameIdentifierScheme:

Attribute nameIdentifierScheme (R, 0-1)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The name of the name identifier scheme.
Uniquely identifies an individual or legal entity, according to various schemes.
The format is dependent upon scheme.

*Examplary values:*

* ``ISNI`` - |ISNI|
* ``ORCID`` - |ORCID|
* ``VIAF`` - |VIAF|
* ``ResearcherID`` - |ResearcherID|
* national organisation ID authoritative systems

.. _datacite:creator_nameIdentifier_schemeURI:

Attribute schemeURI (O, 0-1)
^^^^^^^^^^^^^^^^^^^

The URI of the name identifier scheme.

.. _datacite:creator_affiliation:

Subproperty affiliation (O, 0-n)
~~~~~~~~~~~~~~~~

The organizational or institutional affiliation of the creator.

Examples
-------

With initials:

.. code-block:: xml
   :linenos:

   <creator>
     <creatorName>Evans, R.J.</creatorName>
     <affiliation></affiliation>
     <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="http://orcid.org">1234-1234-1234-1234</nameIdentifier>
   </creator>

With predicates like de, van etc.:

.. code-block:: xml
   :linenos:

  <creator>
     <creatorName>Smit, J.H. (John Hubert) de</creatorName>
  </creator>

With both initials and first name:

.. code-block:: xml

  <creator>
    <creatorName>Janssen, J. (John)</creatorName>
  </creator>

With generational suffixes (Jr., Sr., etc.):

.. code-block:: xml

  <creator>
    <creatorName>Smit Jr., J.H. (John) de</creatorName>
  </creator>

When the creator is an organization/institution:

.. code-block:: xml

  <creator>
    <creatorName>Utrecht University. Department of Computer Sciences</creatorName>
  </creator>

With affiliation:

.. code-block:: xml

  <creator>
    <creatorName>Smit Jr., J.H. (John) de</creatorName>
    <affiliation>Institute of Science and Technology</affiliation>
    <nameIdentifier nameIdentifierScheme="ORCID" schemeURI="https://orcid.org">1234-5678-0987-1234</nameIdentifier>
  </creator>

Context
-------

**Do Not Confuse With**

* :ref:`dci:contributor` (In cases of lesser responsibility, other than authorship, use ``datacite:contributor``).
* :ref:`dci:publisher`

**DataCite v4.3 Differentiation**

* OpenAIRE recommends including a nameIdentifier such as an ORCID or a ISNI if available.

**OpenAIRE Data Guidelines v2 Differentiation**
