.. _contact-type:

Contatto
********

Un Contatto è un mapping con le seguenti proprietà:

-  ``name`` - **obbligatoria** - Questa chiave contiene il nome completo
   di uno dei contatti tecnici. Deve essere una persona reale; NON
   popolare questa chiave con informazioni di contatto generiche,
   dipartimenti dell’azienda, associazioni, etc.
-  ``email`` - :ref:`indirizzo e-mail <email-type>` - Questa chiave contiene l’indirizzo email del contatto
   tecnico. Deve essere un indirizzo email per il contatto diretto con
   il tecnico; NON popolare questa chiave con mailing-list o punti di
   contatto generico tipo “info@acme.inc”.
-  ``phone`` - Numero telefonico. DEVE includere il prefisso internazionale,
   seguendo il formato `E.164 <https://www.itu.int/rec/T-REC-E.164/en>`_
   (es. ``+3923113215112``). Questa chiave deve essere una stringa.
-  ``affiliation`` - Questa chiave contiene informazioni esplicite sui
   contatti tecnici. Nel caso esistano diversi maintainer, questa chiave
   può essere usata per creare relazioni tra diversi contatti tecnici e
   entità di manutenzione. Ad esempio, può contenere il nome di
   un’azienda, il nome di un’associazione, etc.
