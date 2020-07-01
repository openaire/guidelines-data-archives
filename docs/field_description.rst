.. _description:
.. _dci:description:

Description (MA, 0-n)
===========

``datacite:creator``

Property description (MA, 0-n)
--------------------

It is a best practice to supply a description. Also all additional information that does not fit in any of the other categories. May be used for technical information.

.. _@descriptionType:
.. _d:descriptiontype:

Attribute descriptionType (M, 1)
~~~~~~~~~~~~~~~~~~~~~~~~~

The type of the description.

**Allowed values, other constraints**

*Controlled List Values:*

* ``Abstract``
* ``Methods``
* ``SeriesInformation``
* ``TableOfContents``
* ``TechnicalInfo``
* ``Other``

.. _xml:lang:
.. _d:descriptionlang:

Attribute xml:lang (R, 0-1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The language of the description.

**Allowed values, other constraints**

*Recommendation:* take values from one of the following lists:

* IETF BCP 47 - |IETF BCP 47|
* ISO 639-x - |ISO 639-x|

Examples
--------

.. code-block:: xml
   :linenos:

   <descriptions>
      <description descriptionType="Abstract" xml:lang="eng">
        This is an abstract
      </description>
      <description descriptionType="Other">
        This is e.g. a note.
      </description>
   </descriptions>

Context
-------

**Do Not Confuse With**

* :ref:`d:title` (Use ``title`` for the name of the resource)
* :ref:`d:subject` (Use ``subject`` for topics)
* :ref:`d:resourceType` (Use ``resourceType`` for the type)

**DataCite v4.3 Differentiation**

* description_ with `@descriptionType`_\ ="Abstract" is *mandatory when applicable* in OpenAIRE instead of *recommended* in DataCite.
* `xml:lang`_ is *recommenced* in OpenAIRE instead of *optional* in DataCite.

**OpenAIRE Data Guidelines v Differentiation**

* `xml:lang`_ is newly added.
