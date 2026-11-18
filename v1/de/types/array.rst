.. _array-type:

Array
*****

Eine YAML-Sequenz von Werten. Jedes Element MUSS einen vom Schlüssel
erlaubten Typ haben. Wenn ein Schlüssel mehrere Typen erlaubt, DARF
ein Array diese mischen. Zum Beispiel darf
``description/[lang]/screenshots`` sowohl Pfade als auch URLs enthalten.

Ein Schlüssel dieses Typs MUSS auch bei nur einem Element eine Liste
enthalten. Zum Beispiel: ``platforms: [web]``.

Ein Array MUSS mindestens ein Element enthalten und DARF KEINE
Duplikate enthalten. Ein optionaler Schlüssel ist wegzulassen, wenn
keine Elemente aufzulisten sind.
