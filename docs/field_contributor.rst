.. include:: vocabularies/replacements.rst

.. _dci:contributor:

Contributor (MA, 0-n)
================

``datacite:contributor``

An institution or person responsible for collecting, managing, distributing, or otherwise contributing to the development of the resource.

Property contributor (MA, 0-n)
------------------------------

.. _dci:contributor_contributorType:

Attribute contributorType (M, 1)
~~~~~~~~~~~~~~~~

The type of the resource's contributor.

.. include:: vocabularies/contributortype.rst

.. _dci:contributor_contributorName:

Subproperty contributorName (M, 1)
~~~~~~~~~~~~~~~~

The name of the contributor.

.. _dci:contributor_nameType:

Attribute nameType (R, 0-1)
**********************

The type of the name, or rather of the contributor.

.. include:: vocabularies/nametype.rst

.. _dci:contributor_familyName:

Subproperty familyName (O, 0-1)
~~~~~~~~~~~~~~~~

The surname or last name of the contributor.

.. _dci:contributor_givenName:

Subproperty givenName (O, 0-1)
~~~~~~~~~~~~~~~~

The personal or first name of the contributor.

.. _dci:contributor_nameIdentifier:

Subproperty nameIdentifier (R, 0-n)
~~~~~~~~~~~~~~~~

Unique identifier of an individual or legal entity, according to various schemes.

.. _dci:contributor_nameIdentifierScheme:

Attribute nameIdentifierScheme (M, 1)
**********************************

The name of the name identifier scheme.

*Exemplary values:*

* ``ISNI`` - |ISNI|
* ``ORCID`` - |ORCID|
* ``VIAF`` - |VIAF|
* ``ResearcherID`` - |ResearcherID|
* ``CrossrefFunder`` - |CrossrefFunder|
* ``ISIL`` - |ISIL|
* ``GRID`` - |GRID|
* ``OrgRef`` - |OrgRef|
* ``ROR`` - |ROR|
* national organisation ID authoritative systems (e.g. PTCRIS_OrgID (Portugal))

.. _dci:contributor_schemeURI:

Attribute schemeURI (R, 0-1)
***********************

The URI of the name identifier scheme.

.. _dci:contributor_affiliation:

Subproperty affiliation (R, 0-n)
~~~~~~~~~~~~~~~~

The organisational or institutional affiliation of the contributor.

Attribute affiliationIdentifier (O, 0-n)
**********************************


Unique identifier of the organizational affiliation of the creator.

Examples
-------

.. code-block:: xml
   :linenos:

   <datacite:contributors>
      <datacite:contributor>
         <datacite:contributorName>Evans, R. J.</datacite:contributorName>
      <datacite:contributor>
      <datacite:contributor>
         <datacite:contributorName>International Human Genome Sequencing Consortium</datacite:contributorName>
      </datacite:contributor>
   </datacite:contributors>

.. _DataCite MetadataKernel: http://schema.datacite.org/meta/kernel-4.3/

Context
-------

**Do Not Confuse With**

* :ref:`dci:creator`
* :ref:`dci:publisher`

**DataCite v4.3 Differentiation**

* OpenAIRE recommends including name identifiers if available.
* OpenAIRE allows for more identifer types than DataCite.

**OpenAIRE Data Guidelines v2 Differentiation**
