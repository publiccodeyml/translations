.. _contact-type:

Contact
*******

Ein Kontakt ist ein Mapping mit den folgenden Eigenschaften:

-  ``name`` - **obligatorisch** - Dieser Schlüssel enthält den
   vollständigen Namen eines der technischen Kontakte. Es muss sich um
   eine reale Person handeln. Tragen Sie hier KEINE allgemeinen
   Kontaktinformationen, Unternehmensabteilungen, Vereine usw. ein.
-  ``email`` - :ref:`E-Mail-Adresse <email-type>` - Dieser Schlüssel enthält die E-Mail-Adresse des
   technischen Kontakts. Es muss eine E-Mail-Adresse sein, unter der der
   technische Kontakt direkt erreichbar ist. Tragen Sie hier KEINE
   Mailinglisten oder allgemeinen Kontaktadressen wie „info@acme.inc“
   ein.
-  ``phone`` - Telefonnummer. Sie MUSS die internationale Vorwahl
   enthalten und dem Format
   `E.164 <https://www.itu.int/rec/T-REC-E.164/en>`_ folgen (z. B.
   ``+3923113215112``). Der Wert muss eine Zeichenkette sein.
-  ``affiliation`` - Dieser Schlüssel enthält eine ausdrückliche Angabe
   zur Zugehörigkeit des technischen Kontakts. Bei mehreren Maintainern
   kann damit jeder technische Kontakt einem Maintainer zugeordnet
   werden. Er kann zum Beispiel den Namen eines Unternehmens oder eines
   Vereins enthalten.
