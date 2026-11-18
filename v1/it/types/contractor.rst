.. _contractor-type:

Contractor
**********

Un Contractor è un mapping con le seguenti proprietà:

-  ``name`` - **obbligatoria** - Il nome del contractor, sia esso
   un’azienda o una persona fisica.
-  ``until`` - **obbligatoria** - Questa è una data (YYYY-MM-DD). Questa
   chiave deve contenere una data alla quale la manutenzione finirà. Nel
   caso di manutenzione gestita dalla community, questo valore NON DOVREBBE
   essere maggiore di 2 anni nel futuro, e quindi deve essere
   regolarmente aggiornato man mano che la community continua a lavorare
   al progetto.
-  ``email`` - :ref:`indirizzo e-mail <email-type>` - Questa chiave contiene l’indirizzo email del contatto
   tecnico. Deve essere un indirizzo email per il contatto diretto con
   il tecnico; NON popolare questa chiave con mailing-list o punti di
   contatto generico tipo “info@acme.inc”.
-  ``website`` - Questa chiave punta al sito del maintainer. Può puntare
   al principale sito istituzionale, o ad una pagina o sito più
   specifico.
