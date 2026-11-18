.. _contractor-type:

Prestataire
***********

Un Contractor (prestataire) est un mapping comportant les propriétés suivantes :

-  ``name`` - **obligatoire** - Le nom du prestataire, qu'il s'agisse d'une entreprise ou d'une personne physique.
-  ``until`` - **obligatoire** - Il s'agit d'une date (YYYY-MM-DD). Cette clé doit contenir la date à laquelle la maintenance prendra fin. Dans le cas où la maintenance serait réalisée par une communauté, la valeur NE DEVRAIT PAS excéder une période de deux ans, et devra donc être régulièrement mise à jour si la communauté continue à travailler sur le projet.
-  ``email`` - :ref:`adresse e-mail <email-type>` -  Cette clé contient l'adresse e-mail du contact technique. Il s'agit de l'adresse e-mail à laquelle le contact technique peut être directement contacté ; NE PAS remplir cette clé avec une liste de diffusion ou des points de contact génériques tels que “info@acme.inc”.
-  ``website`` - Cette clé pointe vers l'entité maintenant le site web. Elle peut pointer vers le site web principal d'une institution ou bien vers un site web ou une page plus spécifique au projet.
