.. _contractor-type:

Contractor
**********

A Contractor is a mapping with the following properties:

-  ``name`` - **mandatory** - The name of the contractor, whether it’s a
   company or a physical person.
-  ``until`` - **mandatory** - This is a date (YYYY-MM-DD). This key
   must contain the date at which the maintenance is going to end. In
   case of community maintenance, the value should not be more than 2
   years in the future, and thus will need to be regularly updated as
   the community continues working on the project.
-  ``email`` - :ref:`E-Mail-Adresse <email-type>` - This key contains the e-mail address of the technical
   contact. It must be an email address of where the technical contact
   can be directly reached; do NOT populate this key with mailing-lists
   or generic contact points like “info@acme.inc”.
-  ``website`` - This key points to the maintainer website. It can
   either point to the main institutional website, or to a more
   project-specific page or website.
