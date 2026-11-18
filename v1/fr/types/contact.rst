.. _contact-type:

Contact
*******

Un Contact est un mapping comportant les propriétés suivantes :

-  ``name`` - **obligatoire** - Cette clé contient le nom complet d'un des contacts techniques. Ce doit être une personne physique ; NE PAS remplir cette clé avec des informations de contact génériques, relatives à des départements d'une entreprise, à une association, etc.
-  ``email`` - :ref:`adresse e-mail <email-type>` -  Cette clé contient l'adresse e-mail du contact technique. Il s'agit de l'adresse e-mail à laquelle le contact technique peut être directement contacté ; NE PAS remplir cette clé avec une liste de diffusion ou des points de contact génériques tels que “info@acme.inc”.
-  ``phone`` - le numéro de téléphone. Il DOIT inclure l'indicatif téléphonique
   international, en suivant le format `E.164 <https://www.itu.int/rec/T-REC-E.164/en>`_
   (ex. ``+3923113215112``). Il s'agit d'une chaîne de caractères.
-  ``affiliation`` - Cette clé contient une information explicite quant à l'affiliation du contact technique. Dans le cas où il y aurait plusieurs entités maintenant le logiciel, cette clé peut être utilisée pour créer une relation entre chaque contact technique et chaque entité maintenant le logiciel. Elle peut contenir, par exemple, le nom d'une entreprise, le nom d'une association, etc.
