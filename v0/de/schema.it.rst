.. _italian-sections:

Italien (*veraltet*)
--------------------

The entire Italian country-specific section is deprecated and will be
removed in publiccode.yml 1.0. Use the generic ``supports`` key for
compliance with national regulations and integration with national
platforms, and the ``organisation`` key to reference the publishing
administration.

All the keys listed below are specific for Italy and, as such, they must
be inserted in a section named with the ``IT`` code.


Key ``countryExtensionVersion`` (*veraltet*)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Typ: string
- Vorhandensein: mandatory
- Wert: ``"1.0"``


This key **MUST** always be set to ``1.0``.

This key is deprecated together with the rest of the Italian section.

Key ``conforme`` (*veraltet*)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section contains the keys for auto-declaring the compliance with the
current legislation, with respect to the following sections.
Not including these keys implies that the compliance is not known or not
declared.

Key ``conforme/lineeGuidaDesign`` (*veraltet*)
''''''''''''''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional

If present and set to ``true``, the software is compliant with the Italian accessibility
laws (L. 4/2004), as further explained in the 
`linee guida di
design <https://docs.italia.it/italia/designers-italia/design-linee-guida-docs>`__ (Italian language).

Don't use this deprecated key, those guidelines are no longer current.

Key ``conforme/modelloInteroperabilita`` (*veraltet*)
'''''''''''''''''''''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional

If present and set to ``true``, the software is compliant with the linee guida
sull’interoperabilità.

Regulatory reference: `Art. 73 del
CAD <https://docs.italia.it/italia/piano-triennale-ict/codice-amministrazione-digitale-docs/it/v2017-12-13/_rst/capo8_art73.html>`__ (Italian language).

Don't use this deprecated key, those guidelines are no longer current.

Key ``conforme/misureMinimeSicurezza`` (*veraltet*)
'''''''''''''''''''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional

If present and set to ``true``, the software is compliant with the `Misure
minime di sicurezza ICT per le Pubbliche
amministrazioni <https://www.agid.gov.it/it/sicurezza/misure-minime-sicurezza-ict>`__ (Italian language).


Key ``conforme/gdpr`` (*veraltet*)
''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional

If present and set to ``true``, the software respects the GDPR.

Use the ``supports`` key with ``alias:gdpr`` instead.


Section ``piattaforme`` (*veraltet*)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Key ``piattaforme/spid`` (*veraltet*)
'''''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional


If present and set to ``true``, the software interfaces with `SPID
- il Sistema Pubblico di Identità
Digitale <https://developers.italia.it/it/spid>`__.

Use the ``supports`` key with ``alias:spid`` instead.

Key ``piattaforme/cie`` (*veraltet*)
''''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional

If present and set to ``true``, the software interfaces with the Italian
electronic ID card (``Carta di Identità Elettronica``).

Use the ``supports`` key with ``alias:cie`` instead.

Key ``piattaforme/anpr`` (*veraltet*)
'''''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional

If present and set to ``true``, the software interfaces with ANPR.

Use the ``supports`` key with ``alias:anpr`` instead.

Key ``piattaforme/pagopa`` (*veraltet*)
'''''''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional

If present and set to ``true``, the software interfaces with pagoPA.

Use the ``supports`` key with ``alias:pagopa`` instead.

Key ``piattaforme/io`` (*veraltet*)
'''''''''''''''''''''''''''''''''''

- Typ: boolean
- Vorhandensein: optional

If present and set to ``true``, the software interfaces with `IO - the public services app <https://io.italia.it/>`__.

Use the ``supports`` key with ``alias:io`` instead.


Section ``riuso`` (*veraltet*)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section contains a set of keys related to the publication of the software
inside the reuse catalog of `Developers Italia <https://developers.italia.it>`__.

Key ``riuso/codiceIPA`` (*veraltet*)
''''''''''''''''''''''''''''''''''''

- Typ: string (iPA code)
- Vorhandensein: mandatory if ``repoOwner`` is a Public Administration
- Beispiel: ``c_h501``

This key represents the administration code inside the Public Administration
index (codice IPA).

This key is deprecated, use ``organisation/uri`` instead.
