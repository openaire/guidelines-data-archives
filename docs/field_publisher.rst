.. _dci:publisher:

Publisher (MA)
==============

``datacite:publisher``

Cardinality
~~~~~~~~~~~

*Mandatory if applicable*

*Occurrence: 0-n*

Definition and Usage Instruction
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The name of the entity that holds, archives, publishes prints, distributes, releases, issues, or produces the resource. This property will be used to formulate the citation, so consider the prominence of the role. For software, use Publisher for the code repository. If there is an entity other than a code repository, that "holds, archives, publishes, prints, distributes, releases, issues, or produces" the code, use the property Contributor/contributorType/hostingInstitution for the code repository.

An entity responsible for making the resource available. Examples of a Publisher include a person, an organization, or a service. Typically, the name of a Publisher should be used to indicate the entity.

**Usage Instruction**

The (commercial or non-commercial) publisher of the resource; not the (sub)institution the author is affiliated with. Publisher is used only in the bibliographic / functional sense, not an organisational one. Use only the full name of the given (commercial) publisher, not the name of an organization or institute that is otherwise [in a broader sense] associated with the creator.

With university publications place the name of the faculty and/or research group or research school after the name of the university. In the case of organizations where there is clearly a hierarchy present, list the parts of the hierarchy from largest to smallest, separated by full stops. If it is not clear whether there is a hierarchy present, or unclear which is the larger or smaller portion of the body, give the name as it appears in the eprint.

The use of publisher names from authority lists constructed according to local or national thesaurus files is optional.

**Do Not Confuse With**


In most cases the publisher and the creator are not the same.

**Remarks**

* adapted from `DataCite MetadataKernel`_ v4.3

Property publisher (MA, 0-n)
----------------------------

Use the name of the publisher as value.

Example
~~~~~~~

.. code-block:: xml
   :linenos:

    <datacite:publisher xml:lang="en-US">
     Loughborough University. Department of Computer Science
    </datacite:publisher>
    <datacite:publisher xml:lang="en-US">John Wiley &amp; Sons, Inc. (US)</datacite:publisher>

.. _DataCite MetadataKernel: http://schema.datacite.org/meta/kernel-4.3/
.. _DRIVER Guidelines v2 element publisher: https://wiki.surfnet.nl/display/DRIVERguidelines/Publisher

