.. _dependency-type:

Dépendance
**********

Une ``dependency`` est un mapping comportant les propriétés suivantes :

-  ``name`` - **obligatoire** - Le nom de la dépendance (ex. MySQL,
   NFC Reader) ;
-  ``versionMin`` - la version compatible la plus ancienne ;
-  ``versionMax`` - la version compatible la plus récente ;
-  ``version`` - la version principale avec laquelle le logiciel est compatible. Cela suppose une compatibilité avec l'ensemble des correctifs et des corrections de bogues appliqués ultérieurement à cette version.
   La clé NE DOIT PAS être présente en même temps que ``versionMin`` ou
   ``versionMax`` ;
-  ``optional`` - booléen : si ``true``, le logiciel fonctionne aussi sans
   la dépendance. La valeur par défaut est ``false``.


Gestion de versions complexe
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il est bien sûr possible d'utiliser les différentes clés pour spécifier une matrice de compatibilité complexe.


*Ex. 1*

.. code:: yaml

   - name: PostgreSQL
     version: "3.2"
     optional: true

Cet extrait précise le caractère facultatif et la version exacte (3.2.) de la dépendance PostgreSQL.

*Ex. 2*

.. code:: yaml

   - name: MySQL
     versionMin: "1.1"
     versionMax: "1.3"

Cet extrait précise le caractère obligatoire de la dépendance MySQL ainsi que les versions autorisées (versions comprises entre 1.1 et 1.3).
