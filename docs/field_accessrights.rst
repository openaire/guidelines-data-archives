.. _dci:accessrights:

Access Rights (M, 1)
=================

``datacite:rights``

Access right of the resource.
Information about the right or mode the resource can be accessed.
If the metadata describe more than one resource, e.g. fulltext and supplementary material, the access right of the main resource should be provided.

*Allowed values, other constraints:*

Use terms from the `COAR Access Right Vocabulary`_.

======================================== ========================
conceptURI                               label
======================================== ========================
http://purl.org/coar/access_right/c_abf2 ``open access``
http://purl.org/coar/access_right/c_f1cf ``embargoed access``
http://purl.org/coar/access_right/c_16ec ``restricted access``
http://purl.org/coar/access_right/c_14cb ``metadata only access``
======================================== ========================

Property rights (M, 1)
----------------------------

The label of the vocabulary term.

Attribute uri (M, 1)
~~~~~~~~~~~~~~~~

The conceptURI of the vocabulary term.

Examples
-------

.. code-block:: xml
   :linenos:

   <datacite:rights uri="http://purl.org/coar/access_right/c_abf2">open access</datacite:rights>

.. _COAR Access Right Vocabulary: http://vocabularies.coar-repositories.org/documentation/access_rights/

Context
-------

**Do Not Confuse With**

* :ref:`aire:licenseCondition` (Use ``oaire:licenseCondition`` for license information related to the resource.)

**DataCite v4.3 Differentiation**

* Unlike DataCite, OpenAIRE restricts the use of this property to indicate access rights.

**OpenAIRE Data Guidelines v2 Differentiation**

* Former versions of the OpenAIRE Guidelines used the `info:eu-repo-Access-Terms vocabulary <https://wiki.surfnet.nl/display/standards/info-eu-repo/#info-eu-repo-AccessRights>`_.
