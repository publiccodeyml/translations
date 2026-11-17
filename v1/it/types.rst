Tipi
====

Le regole seguenti si applicano a tutte le chiavi di tipo array
(elenco).

.. _array-type:

Array
-----

Una sequenza YAML di valori. Ogni elemento DEVE avere un tipo
consentito dalla chiave. Quando una chiave consente più tipi, un
array PUÒ combinarli. Ad esempio,
``description/[lang]/screenshots`` può contenere sia percorsi sia URL.

Una chiave di questo tipo DEVE contenere un elenco anche quando ha
un solo elemento. Ad esempio, scrivere ``platforms: [web]``.

Un array DEVE contenere almeno un elemento e NON DEVE contenere
duplicati. Omettere una chiave opzionale se non ci sono elementi
da elencare.
