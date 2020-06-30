.. include:: vocabularies/replacements.rst

.. _dci:relatedIdentifier:

Related Identifier (MA, 0-n)
==========================

``datacite:relatedIdentifier``

Identifiers of related resources other than the resource being registered. OpenAIRE especially encourages relating datasets with publications and software, but appreciatively welcomes other kinds of relations too.

**Allowed values, other constraints**

A relatedIdentifier must be globally unique and should be durable. Preferrably it is registered with an established identification system, or is a permalink or stable URL.

The format is free text - a unique string that unambiguously identifies a resource within its given context and follows the respective specifications.

12.1 @relatedIdentifierType (M, 1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The type of the RelatedIdentifier.

**Allowed values, other constraints**

*Controlled List Values:*

* ``ARK`` - |ARK| 
* ``arXiv`` - |arXiv|
* ``bibcode`` - |bibcode|
* ``DOI`` - |DOI|
* ``EAN13`` - |EAN13|
* ``Handle`` - |Handle|
* ``ISBN`` - |ISBN|
* ``ISSN`` - |ISSN| :raw-html:`<br/>` ``EISSN`` - |EISSN| :raw-html:`<br/>` ``LISSN`` - |LISSN| :raw-html:`<br/>` ``PISSN`` - |PISSN|
* ``IGSN`` - |IGSN|
* ``ISTC`` - |ISTC|
* ``LSID`` - |LSID|
* ``PMID`` - |PMID|
* ``PURL`` - |PURL|
* ``UPC`` - |UPC|
* ``URL`` - |URL|
* ``URN`` - |URN|
* ``WOS`` - |WOS|

.. _d:relationtype:

12.2 @relationType (M, 1)
~~~~~~~~~~~~~~~~~~~~~~

The relationship of the resource being registered (A) with the related resource (B).

**Allowed values, other constraints**

*Controlled List Values:*

* ``IsCitedBy`` (B includes A in a citation) :raw-html:`<br/>` ``Cites`` (A includes B in a citation)
* ``IsSupplementTo`` (A is a supplement to B) :raw-html:`<br/>` ``IsSupplementedBy`` (B is a supplement to A)
* ``IsContinuedBy`` (A is continued by the work B) :raw-html:`<br/>` ``Continues`` (A is a continuation of the work B)
* ``Describes`` (A describes B) :raw-html:`<br/>` ``IsDescribedBy`` (A is described by B)
* ``HasMetadata`` (resource A has additional metadata B) :raw-html:`<br/>` ``IsMetadataFor`` (additional metadata A for a resource B)
* ``HasVersion`` (A has a version (B)) :raw-html:`<br/>` ``IsVersionOf`` (A is a version of B)
* ``IsNewVersionOf`` (A is a new edition of B, where the new edition has been modified or updated) :raw-html:`<br/>` ``IsPreviousVersionOf`` (A is a previous edition of B)
* ``IsPartOf`` (A is a portion of B;may be used for elements of a series) :raw-html:`<br/>` ``HasPart`` (A includes the part B)
* ``IsReferencedBy`` (A is used as a source of information by B) :raw-html:`<br/>` ``References`` (B is used as a source of information for A)
* ``IsDocumentedBy`` (B is documentation about/explaining A) :raw-html:`<br/>` ``Documents`` (A is documentation about/explaining B)
* ``isCompiledBy`` (B is used to compile or create A) :raw-html:`<br/>` ``Compiles`` (B is the result of a compile or creation event using A)
* ``IsVariantFormOf`` (A is a variant or different form of B, e.g. calculated or calibrated form or different packaging) :raw-html:`<br/>` ``IsOriginalFormOf`` (A is the original form of B)
* ``IsIdenticalTo`` (A is identical to B, for use when there is a need to register two separate instances of the same resource)
* ``IsReviewedBy`` (A is reviewed by B) :raw-html:`<br/>` ``Reviews`` (A is a review of B)
* ``IsDerivedFrom`` (B is a source upon which A is based) :raw-html:`<br/>` ``IsSourceOf`` (A is a source upon which B is based)
* ``IsRequiredBy`` (A is required by B) :raw-html:`<br/>` ``Requires`` (A requires B)

.. note::
   ``Cites`` and ``IsCitedBy`` is dedicated to publications/datasets directly citing other publications/datasets in their references, whereas ``References`` and ``IsReferencedBy`` describes datasets/publications being used as information sources without direct citations.
