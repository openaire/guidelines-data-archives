.. _dci:language:

Language (MA, 0-n)
=============

``datacite:language``

*DCMI Definition*

A language of the intellectual content of the resource.

**Usage Instruction**

Allowed values are taken from IETF BCP 47, ISO 639-1 language codes.
Examples: en, de, fr

# A specific resource (an instance of scientific output) is either written in one human language or more. In these cases all used languages are used in the DC element ``language``. If a specific resource (an instance of scientific output) is written in one human language and is translated into other human languages, each translation does have its own record.
#
# Recommendation: take values from one of the following lists: 
#
# * IETF BCP 47, the `IANA Language Subtag Registry <http://www.iana.org/assignments/language-subtag-registry>`_
# * ISO 639-x, where x can be 1,2 or 3. Best Practice: we use ISO 639-3 and by doing so we follow: http://www.sil.org/iso639-3/

If necessary, repeat this element to indicate multiple languages.

# If ISO 639-2 and 639-1 are sufficient for the contents of a repository they can be used alternatively. Since there is a unique mapping this can be done during an aggregation process.

Property language (MA, 0-n)
---------------------------

Use the language code as value.

Examples
-------

.. code-block:: xml
   :linenos:

   <datacite:language>en-US</datacite:language>
   <datacite:language>de-DE</datacite:language>

.. _DRIVER Guidelines v2 element language: https://wiki.surfnet.nl/display/DRIVERguidelines/Language
.. _DataCite MetadataKernel: http://schema.datacite.org/meta/kernel-4.3/

Context
-------

**Do Not Confuse With**



**DataCite v4.3 Differentiation**



**OpenAIRE Data Guidelines v2 Differentiation**
