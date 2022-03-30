---
layout: page
title: Notifikasjoner/sak for meldinger
permalink: /notifikasjoner
---
# Notifikasjoner/sak for meldinger

## Bakgrunn og motivasjon for applikasjonen
Arbeidsgivere har hatt problemer med å finne igjen innsendte skjemaer. Team Fager har utviklet en løsning for notifikasjoner og sak/innboks på Min Side Arbeidsgiver. Ved å vise lenke til melding som en sak på Min Side AG kan arbedsgiver enklere finne tilbake til skjemaer.

**permitteringsmeldin-notifikasjon**
Selve applikasjonen. Baseres på Kotling, kafka og grapqhl. Applikasjonen konsumerer eventer på den samme kafka-topicen som brukes av Salesforce og Datavarehus. Eventer konsumeres og sendes til Min Side Arbeidsgiver.

Applikasjonen er stateless og lagrer ikke eventuell status fra Min Side. Meldingens ID kan benyttes ved kommunikasjone med Min Side api.


