Tipi
====

Le regole seguenti si applicano a tutte le chiavi dei tipi descritti
in questa pagina.

.. _string-type:

Stringa
-------

Una sequenza di caratteri Unicode. I valori di tipo data, stringa
enumerata, tag di lingua, codice paese, indirizzo e-mail, percorso,
URI e URL sono stringhe e DEVONO seguire anch'essi queste regole.

I parser DEVONO ignorare gli spazi bianchi iniziali e finali. Il
valore rimanente NON DEVE essere vuoto.

Una stringa NON DEVE contenere interruzioni di riga, a meno che la
sua chiave non le consenta.

Contare i caratteri dopo aver rimosso gli spazi bianchi iniziali e
finali. Usare i cluster di grafemi estesi definiti in `Unicode
Standard Annex #29 <https://www.unicode.org/reports/tr29/>`__. Ad
esempio, ``é`` conta come un carattere sia quando è memorizzato come
un solo punto di codice sia come ``e`` seguito da un accento
combinante.

Il valore DEVE essere una stringa YAML: un numero, un booleano o
null è un errore.

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
