---
layout: page
title: Skjema for melding av masseoppsigelser, permitteringer og nedbemanninger
permalink: /skjema
---
# Skjema for melding av masseoppsigelser, permitteringer og nedbemanninger

## Bakgrunn og motivasjon for applikasjonen
Skal bedrifter permittere, si opp eller innskrenke arbeidstiden til 10 eller flere ansatte har de meldeplikt til NAV. De kan også melde ifra til NAV dersom det gjelder færre enn 10 ansatte om de ønsker det. For at arbeidsgivere skal gjøre det enkelt, har vi utviklet en digital løsning som arbeidsgivere kan bruke. Oppfordrer arbeidsgiver å sende inn meldingen som tidlig som mulig, og senest 14 dager før iverksatt permittering.



Dette er bestemt av:

<a href="https://lovdata.no/dokument/NL/lov/2004-12-10-76/KAPITTEL_3#%C2%A78">Arbeidsmarkedsloven §8</a> <br>
<a href="https://lovdata.no/dokument/NL/lov/2005-06-17-62/KAPITTEL_17#%C2%A715-2">Arbeidsmarkedsloven §15-2</a>


## Hvilket problem skal det løse?

1. **For arbeidsgivere:** Arbeidsgivere som må permittere, omstille eller nedbemanne står i en vanskelig og uoversiktlig situasjon. De er redde for den økonomiske situasjonen i bedriften samtidig som de er redde for å miste forretningskritisk kompetanse og de må håndtere den situasjonen det er ved å sette deres ansatte utenfor arbeidslivet. Gjennom denne meldingen får arbeidsgivere mulighet til å få hjelp og støtte under denne prosessen slik at de tar de riktige valgene for bedriften, men også kan lene seg mot NAV slik at de gjør ting riktig og ivaretar de berørte ansatte. Kanskje det finnes andre løsninger?

2. **Internt i NAV:** Gjennom denne meldingen skal NAV kunne komme i forkjøpet og jobbe sammen med bedriften som er i vanskeligheter. På denne måten kan man se på andre alternativer som ivaretar bedriften på kort og lang sikt og man ivaretar arbeidsplasser og sikrer gode prosesser. På denne måten kan man vinne igjen når bedriften kanskje på et senere tidspunkt er i stand til å inkludere og samarbeide med NAV på andre måter.

## Hvordan kan bruke løsningen?
Innholdet i disse meldingene er vurdert til beskyttelsesverdig informasjon hvor det er behov for å sikre konfidensialitet. Meldingene blir derfor tilgangsstyrt for NAV-ansatte og begrenset etter prinsippet om tjenstlig behov.

Arbeidsgivere finner lenke til løsningen i veiviser for permittering. For å bruke løsningen må man logge inn via ID-porten. I permitteringsmeldingen vil man måtte fylle ut årsak til at man vurderer å permittere eller nedbemanne, samt fylle inn hvor mange som de tror vil bli berørte og den antatte lengden på denne. Den innsendte meldingen vil deretter bli vurdert av NAV-ansatte (med tjenstlig behov) og fulgt opp i mer eller mindre grad.

Du finner testversjonen <a href="https://permitteringsskjema.labs.nais.io/permittering/">Arbeidsmarkedsloven §15-2</a>av løsningen her:


## Viktig å vite om løsningen
Løsningen er vurdert til strengt taushetsbelagt de første to uker etter den er innsendt til NAV, og det er derfor vurdert til at det inntil videre ikke skal skapes dataprodukter av løsningen - heller ikke av konsumerende team innad i NAV. Løsningen anbefales "flagget" i løsningen som gjør at konsumerende team ikke deler data videre.

## Teknisk om løsningen

**permittering**
Frontend for permitteringsskjema. Arbeidsgivere bruker denne applikasjonen til å sende in skjema for melding om masseoppsigelse, permittering eller nedbemanning.

**permitteringsskjema-api**
Backend for permitteringsskjema. Java-basert rest-api som lagrer skjemaer i database og legger de på kafka-topic.

## Sikkerhet og autentisering
Innlogging med ID-porten. Applikasjonen benytter seg av TokenX for å hente ny access token til de ulike apiene som benyttes. Både backend for applikasjonen og videre i verdikjeden.
## Teknisk
React, Java, Spring, Kafka, Postgres. Designen er relativt standard lagdelt med api, repository og diverse integrasjoner. Spring sitt meldingssystem brukes internt i applikasjonen.
### Tekniske skisser
![teknisk skisse](assets/images/permitteringsmelding.png)