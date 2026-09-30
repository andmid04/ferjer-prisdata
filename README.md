# Ferjer prisdata

Dette repoet publiserer et validert og komprimert prisgrunnlag for
[Ferjer iOS](https://github.com/andmid04/ferjer-ios). Mobilappen laster bare den
offentlige JSON-filen. Innloggingen til pris-API-et finnes aldri i appen eller
dette repoet.

- Fil: [`fare-catalog.json`](fare-catalog.json)
- Oppdatering: kontroll én gang per døgn, ny commit bare når prisinnholdet endres
- Feilhåndtering: ukjente eller tvetydige strekninger får ingen pris
- Valuta: NOK i heltalls øre
- Lisens for kildedata: [Creative Commons Navngivelse 4.0](https://creativecommons.org/licenses/by/4.0/deed.no)

## Kilder

- Takster: Statens vegvesen / AutoPASS for ferje
- Takster: Statens vegvesen / det nasjonale ferjebillettsystemet AutoPASS for ferje

Prisene er veiledende. Kontroller alltid endelig pris og avtalevilkår hos
[AutoPASS for ferje](https://autopassferje.no/priser/).

## Snapshotkontrakt

`schemaVersion: 2` inneholder én rettet Entur-strekning og kjøretøyklasse per
rad, med eksplisitte offisielle totalbeløp for vanlig/nullutslippskjøretøy og
fire betalingsprofiler. Bompengeandelen er inkludert i totalbeløpet når den
finnes. Gyldighetsdatoene er inkluderende norske kalenderdatoer.

`sourceSHA256` endres bare når de publiserte prisradene eller dekningen endres.
Klienter skal validere hele filen og beholde forrige gyldige kopi ved feil.

