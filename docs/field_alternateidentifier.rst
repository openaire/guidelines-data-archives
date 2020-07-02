.. include:: vocabularies/replacements.rst

.. _dci:alternativeIdentifier:

Alternative Identifier (R, 0-n)
==========================

``datacite:alternateIdentifier``

The alternateIdentifier serves two purposes:

* Collecting all or many identifiers other than the primary identifier applied to the resource being registered (same instance - same location, same file).
* Registering two especially relevant kinds of web pages dedicated to the resource, namely landing pages and download pages.

Property alternateIdentifier (R, 0-n)
----------------

*Allowed values, other constraints:*

* Secondary identifiers preferably should be durable, and also comprise local identifiers. All existing identifiers for the resource are appreciated.
* The format is free text - any alphanumeric string which is unique within its domain of issue and follows the respective specifications.
* Web pages dedicated to the resource, i.e. landing pages or download pages, are given as URLs. PIDs are fine, but should be prefixed with their respective resolver URL.

.. _d:alternateidentifiertype:

Attribute alternateIdentifierType (M, 1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The type of the alternateIdentifier.

*Exemplary values for secondary identifiers (established and non-standard identifier types):*

* ``ARK`` - |ARK|
* ``DOI`` - |DOI|
* ``EAN13`` - |EAN13|
* ``Handle`` - |Handle|
* ``IGSN`` - |IGSN|
* ``LSID`` - |LSID|
* ``PURL`` - |PURL|
* ``UPC`` - |UPC|
* ``URN`` - |URN|
* ``local`` - a local accession number
* ``URL`` - |URL|

*Controlled values for specific, important web pages dedicated to the resource:*

* ``LandingPage`` - landing pages  
* ``DistributionLocation`` - distribution locations

Examples
--------

Secondary identifiers:

.. code-block:: xml
   :linenos:

   <alternateIdentifiers>
     <alternateIdentifier alternateIdentifierType="DOI">
       10.5447/IPK/2015/9
     </alternateIdentifier>
   </alternateIdentifiers>

.. code-block:: xml
   :linenos:

   <alternateIdentifiers>
     <alternateIdentifier alternateIdentifierType="local">
       oai:hup.sub.uni-hamburg.de.giga:article/491
     </alternateIdentifier>
   </alternateIdentifiers>

Landing pages and download pages:

.. code-block:: xml
   :linenos:

   <alternateIdentifiers>
     <alternateIdentifier alternateIdentifierType="LandingPage">
       http://hdl.handle.net/10316/33181
     </alternateIdentifier>
   </alternateIdentifiers>

.. code-block:: xml
   :linenos:

   <alternateIdentifiers>
     <alternateIdentifier alternateIdentifierType="DistributionLocation">
       http://some-distribution-location.org
     </alternateIdentifier>
   </alternateIdentifiers>
   
Context
-------

**Do Not Confuse With**

* :ref:`dci:identifier` (Use ``identifier`` for the primary identifier of the same resource instance.)
* :ref:`dci:relatedIdentifier` (Use ``relatedIdentifier`` for identifiers of related resources.)

**DataCite v4.3 Differentiation**

* alternateIdentifier_ is *recommended* in OpenAIRE instead of *optional* in DataCite.
* OpenAIRE uses alternateIdentifier_ also for the specific web targets *landing page* and *distribution location*.

**OpenAIRE Data Guidelines v Differentiation**

* Registering landing pages and download pages is newly introduced in the current guideline version.
* alternateIdentifier_ is *recommended* in this version instead of *optional*.
