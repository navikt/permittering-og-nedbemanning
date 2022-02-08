---
layout: page
title: Permittering og nedbemanning
permalink: /
---
# Permittering og nedbemanning
En samling teknisk dokumentasjon, arkitektur, og skisser for applikasjonene tilhørende teamet Permittering og nedbemanning

## Generelt om applikasjonene
Målet er at alle applikasjonene skal følge NAVs anbefalte retningslinjer. Appene baserer seg på Zero Trust når det gjelder autentisering. Vi bruker Kafka for å dele data med andre team.

## Teknologier
Appene bruker stort sett standardteknologier som er vel kjente på NAV: Java, react, next.js, kotlin, kafka, Spring, postgres.

## Integrasjoner
Vi integrerer med flere andre applikasjoner og team. Når det er mulig bruker vi Kafka-topics for å dele data.

- altinn-rettigheter-proxy (Hente altinn-roller)
- Altinn direkte (sende melding til AG)
- Idporten (Pålogging, men bruker wonderwall)
- Azure (Pålogging)
- pam-janzz (Henter beskrivelser av stillingstitler)
- Gosys (journalføring)

## Sikkerhet og autentisering
Alle applikasjoner som har pålogging baseres på Zero Trust. Idporten eller Azure ad autentiserer. Egne token hentes med TokenX og scopes til de apiene som kalles.

## Deploy
Team permittering og nedbemanning er stort sett over på GCP. All deploy skjer med Github actions.

# Applikasjoner

Team Permittering og Nedbemanning forvalter og utvikler et antall applikasjoner. De fleste er i produksjon, men noen er pt. under utvikling.
**I produksjon**
Dette er applikasjoner som er i produksjon og som brukes aktivt.
##  Skjema for melding av masseoppsigelser og permitteringer
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