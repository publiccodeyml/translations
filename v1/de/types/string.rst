.. _string-type:

Zeichenkette
************

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
