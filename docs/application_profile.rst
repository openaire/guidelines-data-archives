Application Profile Overview
----------------------------

The properties of the Application Profile for OpenAIRE Guidelines for Data Archives are listed in this section. The following requirement levels for the metadata properties are used:

Mandatory (M)
  The property must always be present in the metadata. An empty value for the property is not allowed.

Mandatory if Applicable (MA)
  When the property value can be obtained it must be present in the metadata

Recommended (R)
  The use of the property is recommended
  
Recommended than Mandatory (RtM)
  If the recommend element is used, then this is Mandatory.

Optional (O)
  It is not important whether the property is used or not, but if used it may provide complementary information about the resource

Optional than Mandatory (OtM)
  If the optional element is used, then this is Mandatory.

This documentation uses the following namespace abbreviations:

* ``datacite``: http://datacite.org/schema/kernel-4


======================================== ============================= ========================================================================================
OpenAIRE-Field                           Metadata Element              Refinement by Vocabulary
======================================== ============================= ========================================================================================
:ref:`dci:title`                         datacite:title           	:ref:`title type <vocab:titletype_titletype>`
:ref:`dci:creator`                       datacite:creator         	:ref:`name type <vocab:nametype_nametype>`
:ref:`dci:contributor`                   datacite:contributor          | :ref:`name type <vocab:nametype_nametype>`
                                                                       | :ref:`contributor type <vocab:contributortype_contributortype>`
:ref:`dci:datePublication`	         datacite:date                 :ref:`date type <vocab:datetype_datetype>`
:ref:`dci:publicationYear`	         datacite:date                 :ref:`date type <vocab:datetype_datetype>`
:ref:`dci:publisher`                     datacite:publisher
:ref:`dci:subject`                       datacite:subject         	
:ref:`dci:description`                   datacite:description
:ref:`dci:language`			  datacite:language		Allowed values are taken from IETF BCP 47, ISO 639-1 language codes. Examples: en, de, fr
:ref:`dci:identifier`                    datacite:identifier           :ref:`identifier type <vocab:identifiertype_identifiertype>`
:ref:`dci:alternativeIdentifier`         datacite:alternateIdentifier  :ref:`alternateIdentifier type <vocab:alternateIdentifiertype_identifiertype>`
:ref:`dci:relatedIdentifier`             datacite:relatedIdentifier    | :ref:`relatedIdentifier type <vocab:relatedIdentifiertype_identifiertype>`
                                                                       | :ref:`relation type <vocab:relationtype_relationtype>`
                                                                       | :ref:`resourcetype general <vocab:resourcetypegeneral_resourcetypegeneral>`
:ref:`dci:resourceType`                  datacite:resourceType         `COAR Resource Type Vocabulary`_
:ref:`dci:accessrights`                  datacite:rights               `COAR Access Right Vocabulary`_
:ref:`dci:size`                          datacite:size
:ref:`dci:version`                       datacite:version              `COAR Version Vocabulary`_ 
:ref:`dci:geolocation`                   datacite:geoLocation
:ref:`dci:fundingReference`              datacite:fundingReference     :ref:`funderIdentifier type <vocab:funderIdentifiertype_identifiertype>`
======================================== ============================= ========================================================================================

The application profile is implemented in XML Schema.

Not listed elements from DataCite schema v4.3 could be used as further optional (O) elements.

