.. include:: vocabularies/replacements.rst

.. _dci:relatedIdentifier:

Related Identifier (MA, 0-n)
==========================

``datacite:relatedIdentifier``

Identifiers of related resources other than the resource being registered. OpenAIRE especially encourages relating datasets with publications and software, but appreciatively welcomes other kinds of relations too.

Property relatedIdentifier (MA, 0-n)
----------------

**Allowed values, other constraints**

A related identifier must be globally unique and should be durable. Preferrably it is registered with an established identification system, or is a permalink or stable URL.

The format is free text - a unique string that unambiguously identifies a resource within its given context and follows the respective specifications.

Attribute relatedIdentifierType (M, 1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The type of the related identifier.

**Allowed values, other constraints**

*Controlled List Values:*

* ``ARK`` - |ARK| 
* ``arXiv`` - |arXiv|
* ``bibcode`` - |bibcode|
* ``DOI`` - |DOI|
* ``EAN13`` - |EAN13|
* ``Handle`` - |Handle|
* ``ISBN`` - |ISBN|
* ``ISSN`` - |ISSN|, ``EISSN`` - |EISSN|, ``LISSN`` - |LISSN|, ``PISSN`` - |PISSN|
* ``IGSN`` - |IGSN|
* ``ISTC`` - |ISTC|
* ``LSID`` - |LSID|
* ``PMID`` - |PMID|
* ``PURL`` - |PURL|
* ``UPC`` - |UPC|
* ``URL`` - |URL|
* ``URN`` - |URN|
* ``w3id`` - |w3id|
* ``WOS`` - |WOS|

.. _d:relationtype:

Attribute relationType (M, 1)
~~~~~~~~~~~~~~~~~~~~~~

The relationship of the resource being registered (A) with the related resource (B).

**Allowed values, other constraints**

*Controlled List Values:*

* ``IsCitedBy``, ``Cites`` (B includes A in a citation), (A includes B in a citation)
* ``IsSupplementTo``, ``IsSupplementedBy`` (A is a supplement to B), (B is a supplement to A)
* ``IsContinuedBy``, ``Continues`` (A is continued by the work B), (A is a continuation of the work B)
* ``Describes``, ``IsDescribedBy`` (A describes B), (A is described by B)
* ``HasMetadata````IsMetadataFor`` (resource A has additional metadata B), (additional metadata A for a resource B)
* ``HasVersion``, ``IsVersionOf`` (A has a version (B)), (A is a version of B)
* ``IsNewVersionOf``, ``IsPreviousVersionOf`` (A is a new edition of B, where the new edition has been modified or updated), (A is a previous edition of B)
* ``IsPartOf``, ``HasPart`` (A is a portion of B, may be used for elements of a series), (A includes the part B)
* ``IsReferencedBy``, ``References`` (A is used as a source of information by B), (B is used as a source of information for A)
* ``IsDocumentedBy``, ``Documents`` (B is documentation about/explaining A), (A is documentation about/explaining B)
* ``isCompiledBy``, ``Compiles`` (B is used to compile or create A), (B is the result of a compile or creation event using A)
* ``IsVariantFormOf``, ``IsOriginalFormOf`` (A is a variant or different form of B, e.g. calculated or calibrated form or different packaging), (A is the original form of B)
* ``IsIdenticalTo`` (A is identical to B, for use when there is a need to register two separate instances of the same resource)
* ``IsReviewedBy``, ``Reviews`` (A is reviewed by B), (A is a review of B)
* ``IsDerivedFrom``, ``IsSourceOf`` (B is a source upon which A is based), (A is a source upon which B is based)
* ``IsRequiredBy``, ``Requires`` (A is required by B), (A requires B)
* ``IsObsoletedBy``, ``Obsoletes`` (A is replaced by B), (A requires B)





.. note::
   ``Cites`` and ``IsCitedBy`` is dedicated to publications/datasets directly citing other publications/datasets in their references, whereas ``References`` and ``IsReferencedBy`` describes datasets/publications being used as information sources without direct citations.

.. _d:resourceTypeGeneral:

Attribute resourceTypeGeneral (O, 0-1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The main category the related resource belongs to.

*Controlled List Values:*

* ``literature``
* ``dataset``
* ``software``
* ``other``

.. _d:relatedmetadatascheme:

Attribute relatedMetadataScheme (O, 0-1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The name of the metadata scheme.

**Allowed values, other constraints**

Use only with this relation pair: (``HasMetadata``/``IsMetadataFor``).

.. _d:relatedidentifier_schemuri:

Attribute schemeURI (O, 0-1)
~~~~~~~~~~~~~~~~~~

The URI of the relatedMetadataScheme.

**Allowed values, other constraints**

Use only with this relation pair: (``HasMetadata``/``IsMetadataFor``).

.. _d:relatedidentifier_schemeType:

Attribute schemeType (O, 0-1)
~~~~~~~~~~~~~~~~~~~

The type of the relatedMetadataScheme, linked via the schemeURI.

**Allowed values, other constraints**

Use only with this relation pair: (``HasMetadata``/``IsMetadataFor``).

*Examples:*

* ``XSD`` - XML Schema Definition
* ``DTD`` - Document Type Definition
* ``Turtle`` - Terse RDF Triple language

Examples
--------

.. code-block:: xml
   :linenos:

   <relatedIdentifiers>
     <relatedIdentifier
       relatedIdentifierType="URN"
       relationType="IsCitedBy"
       resourceTypeGeneral="literature">
       urn:nbn:de:gbv:089-2683311469
     </relatedIdentifier>
   </relatedIdentifiers>

.. code-block:: xml
   :linenos:

   <relatedIdentifiers>
     <relatedIdentifier 
       relatedIdentifierType="URL" 
       relationType="HasMetadata" 
       relatedMetadataScheme="citeproc+json" 
       schemeURI="https://github.com/citation-style-language/schema/raw/master/csl-data.json">
       https://data.datacite.org/application/citeproc+json/10.5072/example-full
     </relatedIdentifier>
   <relatedIdentifiers>

Context
-------

**Do Not Confuse With**

* :ref:`dci:identifier` (Use ``identifier`` for the primary identifier of the same resource instance.)
* :ref:`dci:alternativeIdentifier` (Use ``alternateIdentifier`` for secondary or local identifiers of the same resource, and also for landing pages and download pages.)

**DataCite v4.3 Differentiation**

* relatedIdentifier_ is *mandatory when applicable* in OpenAIRE instead of *recommended* in DataCite.
* relatedIdentifierType_ allows more types in OpenAIRE than in DataCite.
* resourceTypeGeneral_ suggests other types in OpenAIRE than in DataCite.


**OpenAIRE Data Guidelines v Differentiation**

