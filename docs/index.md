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
