## Projekt testów API z użyciem Postman, Newman CLI, raportami HTML i integracją CI.

![CI](https://github.com/piotrapl/postman-javascript-cities-api-tests/actions/workflows/api-tests.yml/badge.svg)

### Przegląd

- Testy pozytywne i negatywne

- Testy danych z JSON

- Walidacja SLA (czas odpowiedzi)

- Walidacja JSON Schema

- Raporty HTML

- CI z GitHub Actions

### Struktura projektu
```bash
postman-api-automation-demo/
├── postman/
│   └── collection.json
├── data/
│   ├── positive-cities.json
│   └── negative-cities.json
├── reports/
│   ├── report-positive.html
│   └── report-negative.html
├── package.json
└── README.md
```

### Instalacja i uruchomienie
```bash
npm install   # instalacja zależności
npm test      # wszystkie testy
npm run test:positive   # tylko pozytywne
npm run test:negative   # tylko negatywne
```
### Raporty

HTML w folderze reports/:

report-positive.html

report-negative.html

Technologie

Node.js, Newman, Postman, newman-reporter-htmlextra, GitHub Actions

CI

Automatyczne uruchomienie testów i upload raportów przy push/pull request do głównej gałęzi.

Strategia testów

Pozytywne: poprawne dane, status 200, JSON schema, SLA

Negatywne: błędne dane, status 404, pola message, SLA