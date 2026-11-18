.. _array-type:

Tableau
*******

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
