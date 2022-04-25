---
layout: page
title: Journalføring av meldinger om masseoppsigelser, permitteringer og nedbemanninger
permalink: /journalforing
---
# Journalføring av meldinger om masseoppsigelser, permitteringer og nedbemanninger

## Bakgrunn og motivasjon for applikasjonen
Arbeidsgivere er lovpålagd å sende beksjed til NAV ved masseoppsigelse, permittering eller nedbemanning av 10 eller flere ansatte. Arbeidsgivere kan gjøre det digitalt med skjema-applikasjonen.
Meldingene skal journalføres og sendes som oppgaver til saksbehandlere og markedskontakter. Dette skjer med appen
permittering-journalforing.

## Teknisk
Appen konsumerer fra kafka-topic og leser meldinger. Disse lagres i en database for å har kontroll på status. Appen integrerer
med joark for journalføring og oppgavehåndtering.


