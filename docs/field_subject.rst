.. _dci:subject:

Subject (MA, 0-n)
============

``datacite:subject``

Subject, keyword, classification code, or key phrase describing the resource.
In general, choose the most significant and unique words for keywords, avoiding those too general to describe a particular resource.

**Usage Instruction**

For keywords/keyphrases that are not controlled by a vocabulary or thesaurus either encode multiple terms with a semi-colon separating each keyword/keyphrase;
or repeat the element for each term. There are no requirements regarding the capitalization of keywords though internal (within archive) consistency is recommended.

Where terms are taken from a standard classification schema: encode each term using the additional attributes of the subject property. Encode the complete subject descriptor according to the relevant scheme. Use the capitalisation and punctuation used in the original scheme.
It is recommended to use an URI when using classification schemes or controlled vocabularies especially when codified schemes are used like DDC or UDC. Service providers can recognise encoding schemas more easily when the schema is “URI-fied” by an authority namespace. 

If no specific classification scheme is used we recommend the Dewey Decimal Classification (DDC). 
More information about the DDC and the DDC Summaries can be found at https://www.oclc.org/en/dewey/resources.html . Please note that OCLC owns all copyright rights in the Dewey Decimal Classification system. Dewey, Dewey Decimal Classification, DDC, OCLC and WebDewey are registered trademarks of OCLC.

Property subject (MA, 0-n)
--------------------------

Use subject name or keyword as value.

.. _dci:subject_subjectScheme:

Attribute subjectScheme (O, 0-1)
---------------------------
The name of the subject scheme or classification code or authority if one is used.

**Allowed values, examples, other constraints**

*Exemplary Values:*

* ``DDC`` - |DDC|
* ``STW`` - |STW|
* ``AGROVOC`` - |AGROVOC|

.. _dci:subject_schemeUri:

Attribute schemeURI (O, 0-1)
-----------------------
The URI of the subject identifier scheme.

**Allowed values, examples, other constraints**

*Exemplary Values:*

* http://id.loc.gov/authorities/subjects
* http://zbw.eu/stw
* http://aims.fao.org/standards/agrovoc

Attribute valueURI (O, 0-1)
----------------------
The URI of the subject term.

Attribute xml:lang (R, 0-1)
-----------------------

The language of the subject synonym.

**Allowed values, other constraints**

*Recommendation:* take values from one of the following lists:

* IETF BCP 47 - |IETF BCP 47|
* ISO 639-x - |ISO 639-x|

Examples
-------

.. code-block:: xml
   :linenos:

   <datacite:subjects>
    <datacite:subject>Earth sciences and geology</datacite:subject>
    <datacite:subject subjectScheme="DDC" schemeURI="http://dewey.info/" valueURI="">
    551 Geology, hydrology, meteorology
    </datacite:subject>
   </datacite:subjects>

.. _DataCite MetadataKernel: http://schema.datacite.org/meta/kernel-4.3/

Context
-------

**Do Not Confuse With**

* :ref:`dci:description` (Use ``description`` for an abstract)
* :ref:`dci:title` (Use ``title`` for the name of the resource)
* :ref:`dci:resourceType` (Use ``resourceType`` for the type)

**DataCite v4.3 Differentiation**

* `@xml:lang`_ is *recommenced* in OpenAIRE instead of *optional* in DataCite.

**OpenAIRE Data Guidelines v Differentiation**

* `@xml:lang`_ is newly added.
* `@valueUri`_ is newly added.
