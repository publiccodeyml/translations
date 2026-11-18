.. _dependency-type:

Dependency
**********

Una ``dependency`` è un mapping con le seguenti proprietà:

-  ``name`` - **obbligatoria** - Il nome della dipendenza (e.g. MySQL,
   NFC Reader);
-  ``versionMin`` - la prima versione compatibile;
-  ``versionMax`` - l’ultima versione compatibile;
-  ``version`` - l’unica versione major con la quale il software è
   compatibile. Si assume la compatibilità con tutte le *patch* e i
   *bugfix* che saranno applicati successivamente a questa versione.
   La chiave NON DEVE essere presente insieme a ``versionMin`` o
   ``versionMax``;
-  ``optional`` - booleano: se ``true``, il software funziona anche senza
   la dipendenza. Il valore predefinito è ``false``.


Versioning complesso
~~~~~~~~~~~~~~~~~~~~

E’ ovviamente possibile utilizzare le varie chiavi per specificare una
matrice di compatibilità complessa.

*Ex. 1*

.. code:: yaml

   - name: PostgreSQL
     version: "3.2"
     optional: true

Questo snippet segnala una dipendenza opzionale verso PostgreSQL,
nell’esattezza la sua versione 3.2.

*Ex. 2*

.. code:: yaml

   - name: MySQL
     versionMin: "1.1"
     versionMax: "1.3"

Questo snippet segnala una dipendenza obbligatoria verso MySQL,
permettendo ogni versione tra la 1.1 e la 1.3.
