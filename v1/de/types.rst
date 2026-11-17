Typen
=====

Die folgenden Regeln gelten für alle Schlüssel der auf dieser
Seite beschriebenen Typen.

.. _string-type:

Zeichenkette
------------

Eine Folge von Unicode-Zeichen. Werte der Typen Datum, enumerierte
Zeichenkette, Sprach-Tag, Ländercode, E-Mail-Adresse, Pfad, URI und URL sind
Zeichenketten und MÜSSEN ebenfalls diesen Regeln folgen.

Parser MÜSSEN führende und nachfolgende Leerraumzeichen ignorieren.
Der verbleibende Wert DARF NICHT leer sein.

Eine Zeichenkette DARF KEINE Zeilenumbrüche enthalten, es sei denn,
ihr Schlüssel erlaubt sie.

Zeichen werden nach dem Entfernen führender und nachfolgender
Leerraumzeichen gezählt. Dabei sind die in `Unicode Standard
Annex #29 <https://www.unicode.org/reports/tr29/>`__ definierten
erweiterten Graphemcluster zu verwenden. Zum Beispiel zählt ``é``
als ein Zeichen, unabhängig davon, ob es als ein einzelner Codepunkt
oder als ``e`` gefolgt von einem kombinierenden Akzent gespeichert ist.

Der Wert MUSS eine YAML-Zeichenkette sein: Eine Zahl, ein boolescher
Wert oder null ist ein Fehler.

.. _array-type:

Array
-----

Eine YAML-Sequenz von Werten. Jedes Element MUSS einen vom Schlüssel
erlaubten Typ haben. Wenn ein Schlüssel mehrere Typen erlaubt, DARF
ein Array diese mischen. Zum Beispiel darf
``description/[lang]/screenshots`` sowohl Pfade als auch URLs enthalten.

Ein Schlüssel dieses Typs MUSS auch bei nur einem Element eine Liste
enthalten. Zum Beispiel: ``platforms: [web]``.

Ein Array MUSS mindestens ein Element enthalten und DARF KEINE
Duplikate enthalten. Ein optionaler Schlüssel ist wegzulassen, wenn
keine Elemente aufzulisten sind.

.. _url-type:

URL
---

Eine absolute URL einschließlich Schema, zum Beispiel
``https://example.com/firefax``.

Das Schema MUSS ``http`` oder ``https`` sein, sofern der Schlüssel keine
anderen erlaubt.
