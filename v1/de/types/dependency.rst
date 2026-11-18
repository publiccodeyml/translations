.. _dependency-type:

Dependency
**********

A ``dependency`` is a mapping with the following properties:

-  ``name`` - **mandatory** - The name of the dependency (e.g. MySQL,
   NFC Reader)
-  ``versionMin`` - the first compatible version
-  ``versionMax`` - the latest compatible version
-  ``version`` - the only major version for which the software is
   compatible. It assumes compatibility with all patches and bugfixes
   later applied to this version.
   Der Schlüssel DARF NICHT zusammen mit ``versionMin`` oder
   ``versionMax`` vorhanden sein.
-  ``optional`` - boolescher Wert: Bei ``true`` funktioniert die Software
   auch ohne die Abhängigkeit. Der Standardwert ist ``false``.


Complex versioning
~~~~~~~~~~~~~~~~~~

It is of course possible to use the various keys to specify a complex
compatibility matrix.

*Ex. 1*

.. code:: yaml

   - name: PostgreSQL
     version: "3.2"
     optional: true

This snippet marks an optional dependency on PostgreSQL exactly version
3.2.

*Ex. 2*

.. code:: yaml

   - name: MySQL
     versionMin: "1.1"
     versionMax: "1.3"

This snippet marks a mandatory dependency on MySQL, allowing any version
between 1.1 and 1.3.
