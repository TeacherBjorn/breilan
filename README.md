# Utviklingsprosjekt: LAN-nettside

**Fag:** Utvikling | **Gruppearbeid:** 2–3 elever

---

## Bakgrunn

Skolen har i mange år brukt nettsiden breilan.no for sitt LAN-arrangement. Siden ble laget av tidligere elever, men er bygget på et komplisert rammeverk som gjør det vanskelig for nye elever å sette seg inn i og videreføre koden.

Oppgaven er å lage en ny, enkel og veldokumentert nettside som kan brukes av neste kull og kullet etter det igjen. Lesbar kode og god dokumentasjon er like viktig som et fint sluttprodukt.

> **Merk:** Dokumentasjonskravet er ikke valgfritt. Det er en del av vurderingen.

---

## Tekniske krav

| Teknologi | Krav | Begrunnelse |
|---|---|---|
| HTML / CSS / JS | Kun disse, ingen rammeverk | Neste kull skal forstå koden |
| GitHub | Koden skal ligge i et repo | Versjonskontroll og samarbeid |
| GitHub Actions | Automatisk deploy ved push til main | Enkel og trygg publisering |
| Firebase Hosting | Gratis hosting av statiske filer | Enkelt oppsett, god ytelse |
| Google Forms + Sheets | Påmelding og kontaktskjema | Embeddes via iframe. Svar lagres automatisk i Google Sheets. |

Firebase og GitHub Actions er sentrale verktøy i dette prosjektet. Introduksjon og guide for hvordan man setter opp firebase finner du her: [github.com/TeacherBjorn/bruk-av-firebase](https://github.com/TeacherBjorn/bruk-av-firebase)

---

## Anbefalt mappestruktur

Bruk denne strukturen som utgangspunkt. Mapper og filer kan tilpasses, men strukturen må dokumenteres i README.md.

```
breilan/
├── index.html          ← Forside
├── pamelding.html      ← Påmeldingsside
├── program.html        ← Tidsplan / program
├── info.html           ← Praktisk informasjon
├── kontakt.html        ← Kontaktside
├── css/
│   ├── style.css       ← Global styling
│   └── components.css  ← Navbar, footer, felles elementer
├── js/
│   ├── countdown.js    ← Nedtelling til arrangementet
│   └── nav.js          ← Mobilmeny
├── assets/
│   ├── logo.png
│   └── bilder/
├── .github/workflows/
│   └── deploy.yml      ← GitHub Actions
└── README.md           ← VIKTIG: dokumentasjon for neste kull
```

---

## Arbeidsflyt og faser

### Fase 1–3: Fellesarbeid med lærer (ca. 1–2 timer)

---

### Fase 1: Forstå eksisterende løsning

Gå gjennom breilan.no grundig. Identifiser hvilke sider og funksjoner som finnes, og diskuter i gruppen hva som bør beholdes og hva som bør endres.

**Leveranse:** Kort skriftlig oppsummering (½–1 side) av funn og planer.

---

### Fase 2: Wireframe

Lag enkle skisser av alle sider, for hånd eller digitalt (f.eks. Figma eller Balsamiq). Wireframen skal vise layout og innholdsplassering uten farger eller detaljer. Lag én versjon for desktop og én for mobil for hver side.

**Leveranse:** Wireframes for alle sider. Må godkjennes av lærer før dere går videre.

---

### Fase 3: Prototype

Bygg videre på wireframene i Figma og legg til farger, typografi og visuell stil. Prototypen skal være klikkbar slik at man kan navigere mellom sidene, og den skal vise hvordan siden ser ut på både desktop og mobil.

**Leveranse:** Klikkbar Figma-prototype. Må godkjennes av lærer før koding starter.

---

### Fase 4–7: Selvstendig gruppearbeid

---

### Fase 4: Planlegg, strukturer og sett opp infrastruktur

Dette er den teknisk mest krevende fasen. Bruk lærers guide aktivt: [github.com/TeacherBjorn/bruk-av-firebase](https://github.com/TeacherBjorn/bruk-av-firebase)

**Firebase og GitHub Actions:**

1. Opprett et Firebase-prosjekt på [console.firebase.google.com](https://console.firebase.google.com)
2. Aktiver Firebase Hosting i prosjektet
3. Installer Firebase CLI og kjør `firebase init` i prosjektmappen
4. Opprett GitHub-repo og inviter alle gruppemedlemmer
5. Sett opp `.github/workflows/deploy.yml` for automatisk deploy ved push til main
6. Legg til Firebase-hemmeligheter (Service Account) i GitHub repository secrets
7. Test at en enkel `index.html` deployes korrekt til Firebase Hosting

**Prosjektstruktur og dokumentasjon:**

1. Lag mappestruktur som beskrevet over
2. Skriv første utkast av README.md

**Leveranse:** En fungerende GitHub Actions-pipeline som deployer til Firebase Hosting.

---

### Fase 5: Bygg nettsiden

Kode nettsiden i HTML, CSS og JavaScript etter godkjent prototype. Siden skal være responsiv og fungere på mobil, nettbrett og PC. All kode skal ha kommentarer på norsk. Bruk Git aktivt med jevnlige commits og beskrivende commit-meldinger. Verifiser at GitHub Actions deployer automatisk ved hver push til main.

---

### Fase 6: Skjema og funksjonalitet

1. Opprett Google Forms-skjema for påmelding og kontakt under Breilan sin Gmail-konto
2. Koble hvert skjema til et Google Sheets-ark via Responses-fanen i Forms
3. Embed skjemaene på nettsiden med iframe-koden fra "Send > Embed" i Forms
4. Verifiser at testsvar dukker opp som rader i Google Sheets
5. Legg til nedtelling til arrangementet i JavaScript
6. Test siden i ulike nettlesere og på mobil

---

### Fase 7: Deploy og dokumentasjon

1. Verifiser at GitHub Actions deployer korrekt til Firebase ved push til main
2. Fullfør README.md (se krav under)
3. Gjennomgå all kode og vurder om kommentarene er gode nok til at neste kull forstår det

**Leveranse:** Lenke til GitHub-repo og lenke til live nettside på Firebase Hosting.

---

## Krav til README.md

README.md er det viktigste dokumentet i prosjektet og det første neste kull leser.

| Seksjon | Innhold |
|---|---|
| Hva er dette? | Kort beskrivelse av prosjektet og arrangementet |
| Slik kjører du siden lokalt | Steg-for-steg uten forutsetninger om forkunnskaper |
| Slik oppdaterer du innhold | Dato, sted, bilder, påmeldingsgrense |
| Google Forms og Sheets | Direktelenke til hvert skjema og tilhørende Sheets-ark. Hvilken Gmail-konto eier dem? Hvordan deles arket med arrangørene uten å gi tilgang til Gmail-kontoen? |
| Hosting og deploy | Firebase-prosjektnavn, GitHub Actions-oppsett, lenke til lærers guide |
| Kjente problemer / TODO | Hva ble ikke ferdig? Hva bør neste kull se på? |
| Laget av | Navn, kull og år |

---

## Vurderingskriterier

| Kriterium | Vekt | Beskrivelse |
|---|---|---|
| Planlegging | 15 % | Wireframe dekker alle sider i desktop og mobilversjon. Prototype er klikkbar og visuelt gjennomarbeidet. |
| Kode og struktur | 25 % | Ryddig mappestruktur, semantisk HTML, konsistent CSS. Ingen unødvendig kompleksitet. |
| Funksjonalitet | 20 % | Alle sider fungerer. Skjemaer sender korrekt. Nedtelling viser riktig tid. Responsiv på mobil og PC. |
| Dokumentasjon | 25 % | README er fullstendig og presis. Koden har kommentarer. Neste kull skal kunne sette opp og vedlikeholde siden uten hjelp. |
| Prosess og Git | 15 % | Jevnlige commits med beskrivende meldinger. Alle gruppemedlemmer har bidratt. GitHub Actions fungerer korrekt. |

---

## Innlevering

1. Lenke til GitHub-repositoriet (public, eller lærer må inviteres)
2. Lenke til live nettside på Firebase Hosting
3. Lenke til Figma-prototype (view-tilgang)
4. README.md ferdig utfylt i repoet

---

Spørsmål? Ta kontakt med faglærer.
