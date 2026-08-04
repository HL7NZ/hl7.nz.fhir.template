# HL7 New Zealand FHIR template

Template for FHIR implementation guides published by [HL7 New Zealand](http://www.hl7.org.nz).

It applies the colour scheme, adds the HL7 New Zealand logo to the left of the page
header and the FHIR logo to the right, and adds an HL7 New Zealand link to the page footer.

This template is based on package `fhir.base.template`, which supplies the underlying IG
layouts, scripts and assets.

## Package ID

package id = `hl7.nz.fhir.template`

## Using this template

In `ig.ini`:

```ini
template = https://github.com/HL7NZ/hl7.nz.fhir.template
```

Referencing the GitHub URL makes the publisher fetch the current `main` branch on each build.
To pin a published version instead, use `template = hl7.nz.fhir.template#0.1.0`.

## Adding an IG-specific logo

The template uses `#hl7-nav` for the HL7 NZ logo and `#family-nav` for the FHIR logo, leaving
`#project-nav` free. An IG that needs its own logo can add
`input/includes/_append.fragment-header.html` in the IG repo with a `#project-nav` block.
The page header is a flex row, and `#project-nav` is ordered between the two.

