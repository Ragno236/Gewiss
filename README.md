# GEWISS · AI Home Agent — User Research

Questo repository contiene tutti i materiali di **User Research** per il progetto AI Home Agent di Gewiss.

## Contenuto

| File / Cartella | Descrizione |
|---|---|
| `presentazione.html` | Deck di presentazione completo (8 slide) — apri direttamente nel browser |
| `customer-journeys/` | App interattiva con le 3 Customer Journey Map (Marco, Chiara, Pina) |
| `customer-journeys/index.html` | Entry point dell'app journey — apri nel browser |
| `docs/user-journeys.md` | Journey map narrative dettagliate — formato Markdown / handoff Figma |

## Come usarlo

### Presentazione
```bash
# Apri direttamente nel browser (nessuna dipendenza)
open presentazione.html
```

### Customer Journey App
```bash
# Avvia un server locale (opzione 1 — Python)
cd customer-journeys
python3 -m http.server 8080
# → apri http://localhost:8080

# oppure con Node (opzione 2)
npx serve .
```

## Struttura del progetto

```
GEWISS/
├── presentazione.html          ← Deck 8 slide (standalone HTML)
├── customer-journeys/
│   ├── index.html              ← App journey interattiva
│   ├── styles.css              ← Stili
│   └── app.js                  ← Logica e contenuti
├── docs/
│   └── user-journeys.md        ← Journey map narrative (Figma handoff)
└── README.md
```

## Personas

- **Marco Ferretti** — Project Manager, 41 anni · Due proprietà · Ottimizzazione energetica
- **Chiara Bellini** — Ricercatrice Ambientale, 34 anni · Bilocale · Sostenibilità e qualità aria
- **Giuseppina "Pina" Conti** — Pensionata, 68 anni · Sola · Sicurezza e continuità offline

## Feature GEWISS AI Home Agent coperte

- Progressive Autonomy (Manual → Assisted → Collaborative → Autonomous)
- Notification Center con gerarchia Insight / Warning / Critical
- Value Center con narrazione settimanale e CO2 evitata
- Modalità Continuità Offline (backup locale RF)
- Onboarding intelligente 10 giorni

---

*Progetto GEWISS · Research Phase · 2026*
