# HL7 New Zealand FHIR template

Template for FHIR implementation guides published by [HL7 New Zealand](http://www.hl7.org.nz).

It applies the HL7 NZ colour scheme, adds the HL7 New Zealand logo to the left of the page
header and the FHIR logo to the right, and adds an HL7 New Zealand link to the page footer.

This template is based on package `fhir.base.template`, which supplies the underlying IG
layouts, scripts and assets.

## Package ID

package id = `hl7.nz.fhir.template`

## Using this template

In your IG's `ig.ini`:

```ini
template = https://github.com/HL7NZ/hl7.nz.fhir.template
```

Referencing the GitHub URL makes the publisher fetch the current `main` branch on each build.
To pin a published version instead, use `template = hl7.nz.fhir.template#0.1.0`.

## Layout

| Path | Purpose |
| --- | --- |
| `package/package.json` | Template package manifest — id, version, and the `fhir.base.template` dependency |
| `package-list.json` | Publication history for the template package |
| `includes/_append.fragment-css.html` | Appended to the base template's `fragment-css.html`; links `hl7nz.css` |
| `includes/_append.fragment-header.html` | Appended to the base template's `fragment-header.html`; HL7 NZ and FHIR logos |
| `includes/_append.fragment-footer.html` | Appended to the base template's `fragment-footer.html`; Version History and HL7 NZ links |
| `content/assets/css/hl7nz.css` | HL7 NZ theme — overrides the standard theming custom properties |
| `content/assets/images/` | HL7 NZ and FHIR logos |

`_append.*` files are merged onto the base template's fragment of the same name by the IG
publisher, so this template only has to carry the parts that differ from `fhir.base.template`.

## History

This template replaces `nzBaseTemplate`, an interim template used by the
[NZ Base IG](https://github.com/HL7NZ/nzbase).
