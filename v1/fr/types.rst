Types
=====

Les règles suivantes s'appliquent à toutes les clés des types
décrits sur cette page.

.. _string-type:

Chaîne de caractères
--------------------

Une séquence de caractères Unicode. Les valeurs de type date,
chaîne énumérée, étiquette de langue, code pays, adresse e-mail,
chemin, URI et URL sont des chaînes et DOIVENT aussi suivre ces
règles.

Les analyseurs DOIVENT ignorer les espaces blancs en début et en
fin de chaîne. La valeur restante NE DOIT PAS être vide.

Une chaîne NE DOIT PAS contenir de sauts de ligne, sauf si sa clé
les autorise.

Compter les caractères après avoir supprimé les espaces blancs en
début et en fin de chaîne. Utiliser les grappes de graphèmes
étendues définies dans `Unicode Standard Annex #29
<https://www.unicode.org/reports/tr29/>`__. Par exemple, ``é`` compte
pour un caractère, qu'il soit stocké comme un seul point de code ou
comme ``e`` suivi d'un accent combinant.

La valeur DOIT être une chaîne YAML : un nombre, un booléen ou null
est une erreur.

.. _array-type:

Tableau
-------

Une séquence YAML de valeurs. Chaque élément DOIT avoir un type
autorisé par la clé. Lorsqu'une clé autorise plusieurs types, un
tableau PEUT les mélanger. Par exemple,
``description/[lang]/screenshots`` peut contenir à la fois des chemins
et des URL.

Une clé de ce type DOIT contenir une liste même pour un seul élément.
Par exemple, écrire ``platforms: [web]``.

Un tableau DOIT contenir au moins un élément et NE DOIT PAS contenir
de doublons. Omettre une clé facultative s'il n'y a aucun élément
à lister.
