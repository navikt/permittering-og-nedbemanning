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

## Notifikasjoner/sak for meldinger
[Dokumentasjon](https://navikt.github.io/permittering-og-nedbemanning/notifikasjoner) Dokumentasjon
## Informasjonssider om permitteringer
Ligger i Enonic

## Applikasjon for å sende meldinnger til bedrifter i altinn (skal slettes?)
**altinn-meldinger-web** (Frontend for meldinger til AG via altinn)

**altinn-meldinger-api** (Backend for meldinger)

**altinn-meldinger-dokgen** (journalføring for meldinger)
