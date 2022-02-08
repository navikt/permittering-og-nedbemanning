---
layout: page
title: Applikasjoner
permalink: /applikasjoner
---
# Applikasjoner

Team Permittering og Nedbemanning forvalter og utvikler et antall applikasjoner. De fleste er i produksjon, men noen er pt. under utvikling.
**I produksjon**
Dette er applikasjoner som er i produksjon og som brukes aktivt.
##  Skjema for melding av masseoppsigelser og permitteringer
[Dokumentasjon](https://navikt.github.io/permittering-og-nedbemanning/skjema) Dokumentasjon

**permittering**
Frontend for permitteringsskjema. Arbeidsgivere bruker denne applikasjonen til å sende in skjema for melding om masseoppsigelse, permittering eller nedbemanning.

**permitteringsskjema-api**
Backend for permitteringsskjema. Java-basert rest-api som lagrer skjemaer i database og legger de på kafka-topic.

**permittering-journalføring**
Backend for journalføring av skjema. Leser fra kafka-topic og journalfører til gosys.

## Informasjonssider om permitteringer
**permittering-og-omstilling**
Veiviseren for permittering og omstilling. Wiki basert på Sanity som cms.

**permitterings-kalkulator**
Kalkulator for lønnsplikt og lignende

## Applikasjon for å sende meldinnger til bedrifter i altinn
**altinn-meldinger-web** (Frontend for meldinger til AG via altinn)

**altinn-meldinger-api** (Backend for meldinger)

**altinn-meldinger-dokgen** (journalføring for meldinger)

## Under utvikling
**permitteringsportal** (Frontend for nye 040804)

**permitteringsportal-api** (Backend for nye 040804)