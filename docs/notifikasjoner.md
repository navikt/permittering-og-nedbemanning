---
layout: page
title: Notifikasjoner/sak for meldinger
permalink: /notifikasjoner
---
# Notifikasjoner/sak for meldinger

## Bakgrunn og motivasjon for applikasjonen
Arbeidsgivere har hatt problemer med å finne igjen innsendte skjemaer. Team Fager har utviklet en løsning for notifikasjoner og sak/innboks på Min Side Arbeidsgiver. Ved å vise lenke til melding som en sak på Min Side AG kan arbedsgiver enklere finne tilbake til skjemaer.

**permitteringsmelding-notifikasjon**
Selve applikasjonen. Baseres på Kotlin, Kafka og grapqhl. Applikasjonen konsumerer eventer på den samme kafka-topicen som brukes av Salesforce og Datavarehus. Eventer konsumeres og sendes til Min Side Arbeidsgiver.

Applikasjonen konsumerer fra slette-topic hvor id'er til meldinger som skal blir slettet blir produsert. Når disse leses sendes en slette request til Min Side-api.

Applikasjonen er stateless og lagrer ikke eventuell status fra Min Side. Meldingens ID kan benyttes ved kommunikasjon med Min Side api.

## Sikkerhet og autentisering
Applikasjonen har ikke noen frontend og da ikke pålogging for brukere. Applikasjonen sikrer meldinger med maskin-maskin autentisering med Azure AD.

## Teknisk

