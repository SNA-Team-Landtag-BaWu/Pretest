---
title: "SNA: Codebuch Landtag BaWü"
date: "2024-07-01"
---

## Edgelist

- **from**: Definiert den „Sender“ der Beziehung (i.d.R. Politiker*in).  
  Entspricht ID der Nodelist.
- **to**: Definiert den „Empfänger“ der Beziehung (i.d.R. Organisation).  
  Entspricht ID der Nodelist.
- **relationship**: Definiert die Art der Beziehung wie folgt:
  - 1 = Mitgliedschaft
  - 2 = Vorstand von
  - 3 = Sonstiges

## Nodelist

Grundregel: die IDs der Nodelist müssen mit den IDs der Edgelist komplett übereinstimmen. Wir verwenden als Organisationen alle unter „Sonstige Funktionen und Mitgliedschaften“ erwähnten Organisationen.

### BEI PERSONEN UND ORGANISATIONEN:

- **id**: Eindeutige Identifikation jedes Knotens.  
  Darf nicht mehrfach vorkommen.  
  Keine Sonderzeichen.  
  Immer kleingeschrieben.  
  Schema:
  - Personen: erste zwei Buchstaben Vorname + erste zwei Buchstaben Nachname (z.B. „suas“ für Susanne Aschhoff)
  - Organisationen: erste zwei Buchstaben der ersten beiden Wörter (z.B. „tuwa“ für Turnverein Waiblingen e. V.)

- **name**: 
  - Bei Personen: Vor- und Nachname ohne Zusatz (z.B. „Dr.“)
  - Bei Organisationen: Vollständiger Name mit Zusatz (z.B. „e. V.“)

- **type**: Art des Knotens:
  - 1 = Person
  - 2 = Organisation

### NUR BEI PERSONEN:

- **sex**: Geschlecht der Person (falls unklar, recherchieren):
  - 1 = männlich
  - 2 = weiblich
  - 3 = divers

- **birthyear**: Geburtsjahr der Person (z.B. 1970)

- **profession**: Beruf der Person laut Volkshandbuch, bei mehreren Angaben nur die erste!

- **industry**: Branche des Berufs, der unter profession angegeben ist,:
  - 1 = Politik und öffentlicher Dienst
     z.B.:
    - Politiker/in (hauptberuflich)
    - Beamte/r
    - Lehrer/in
  - 2 = Wirtschaft und Unternehmertum
     z.B.:
    - Unternehmer/in
    - Kaufmann/Kauffrau
    - Geschäftsführer/in
  - 3 = Rechts- und Steuerwesen
     z.B.:    
    - Rechtsanwalt/Rechtsanwältin
    - Steuerberater/in
  - 4 = Gesundheitswesen
     z.B.:
    - Arzt/Ärztin
    - Apotheker/in
  - 5 = Ingenieurwesen und Technik
     z.B.:
    - Ingenieur/in
    - Techniker/in
  - 6 = Digitale Berufe
     z.B.:
    - IT-Spezialist/in
    - Softwareentwickler/in
  - 7 = Landwirtschaft
     z.B.:
    - Landwirt/in
    - Winzer/in
  - 8 = Soziales und Bildung
     z.B.:
    - Sozialarbeiter/in
    - Erzieher/in  
  - 9 = Kultur und Kunst
     z.B.:
    - Musiker/in
    - Schauspieler/in
    - Künstler/in
  - 10 = Medien und Kommunikation
     z.B.:
    - Journalist/in
    - PR-Berater/in
  - 11 = Handwerk
    - Verschiedene Handwerksberufe
  - 12 = Wissenschaft und Forschung
     z.B.:
    - Wissenschaftler/in
    - Historiker/in
  - 13 = Militär und Sicherheit
     z.B.:
    - Offizier/in
    - Polizist/in
  - 14 = geistliche Berufe
     z.B.:
    - Pfarrer/in
    - Diakon/in
  - 15 = Verkehr und Logistik
     z.B.:
    - Pilot/in
    - Logistikmanager/in
  - 16 = Sonstiges

- **birthcity**: Geburtsstadt der Person laut Volkshandbuch

- **party**: Aktuelle Partei der Person:
  - 1 = GRUENE
  - 2 = CDU
  - 3 = SPD
  - 4 = FDP/DVP
  - 5 = AfD
