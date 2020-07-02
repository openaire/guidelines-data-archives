.. _dci:publisher:

Publisher (MA, 0-n)
==============

``datacite:publisher``

An entity responsible for making the resource available. The entity that holds, archives, publishes prints, distributes, releases, issues, or produces the resource. Publishers may be persons, organizations, or services. A code/data repository might be put into publisher or, if several agents make the entity available, into contributor/contributorType/hostingInstitution.
This property is used for citations, and so gets prominently visible. 

Property publisher (MA, 0-n)
----------------------------

Use the name of the publisher as value.

*Allowed Values, other constraints:*

* With university publications place the name of the faculty and/or research group or research school after the name of the university.
* In the case of organizations where there is clearly a hierarchy, list the parts of the hierarchy from largest to smallest, separated by full stops. If it is not clear whether there is a hierarchy, or unclear which is the larger or smaller portion of the body, give the name as it appears in the print.
* The use of publisher names from authority lists constructed according to local or national thesaurus files is optional.

Examples
-------

.. code-block:: xml
   :linenos:

    <datacite:publisher xml:lang="en-US">
     Loughborough University. Department of Computer Science
    </datacite:publisher>
    <datacite:publisher xml:lang="en-US">John Wiley &amp; Sons, Inc. (US)</datacite:publisher>

.. _DataCite MetadataKernel: http://schema.datacite.org/meta/kernel-4.3/
.. _DRIVER Guidelines v2 element publisher: https://wiki.surfnet.nl/display/DRIVERguidelines/Publisher

Context
-------

**Do Not Confuse With**

* :ref:`dci:contributor`
* :ref:`dci:creator` Publisher is dedicated to the (commercial or non-commercial) publisher of the resource; not the (sub)institution the author is affiliated with. Publisher is used only in the bibliographic / functional sense, not an organisational one. Use only the full name of the given (commercial) publisher, not the name of an organization or institute that is otherwise [in a broader sense] associated with the creator.

**DataCite v4.3 Differentiation**



**OpenAIRE Data Guidelines v2 Differentiation**
