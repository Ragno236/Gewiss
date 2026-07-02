# Handoff completo — GEWISS

Documento operativo per continuare il lavoro in Antigravity senza perdere lo stato attuale.

## 1. Repository e branch

- Repository GitHub: `https://github.com/Ragno236/Gewiss`
- Branch di lavoro e pubblicazione: `main`
- Commit di riferimento dei due deliverable: `238a63474a06c37eacfe706724526dc9fbbfa49f`
- Cartella locale usata finora: `/Users/ragno/Documents/New project`

Prima di lavorare:

```bash
cd "/Users/ragno/Documents/New project"
git pull origin main
git status
```

La working tree deve essere pulita prima di iniziare. Conservare sempre le modifiche già presenti e non riscrivere file non coinvolti nella richiesta.

## 2. File sorgente corretti

Esistono due deliverable distinti:

1. `presentazione.html` — presentazione cliente.
2. `prototipo-iphone17.html` — prototipo interattivo dell’app in una cornice iPhone 17.

Questi sono gli unici file da modificare per i rispettivi deliverable. Non creare copie come `presentazione-cliente.html`, `presentazione-definitiva.html`, `prototipo-v2.html` o simili, salvo richiesta esplicita. In passato la duplicazione dei file ha generato confusione perché il cliente continuava a vedere il file originale su GitHub.

Gli altri contenuti del repository (`customer-journeys/`, `docs/`) sono materiale di ricerca e non devono essere modificati per interventi sul deck o sul prototipo.

## 3. Presentazione cliente

### File

`presentazione.html`

### Stato attuale

Deck HTML standalone di 8 slide:

1. Copertina
2. Indice
3. Contesto & obiettivi
4. Metodologia & partecipanti
5. User Personas
6. Insights
7. User journey
8. Opportunità di design

Decisioni già applicate e da non far regredire:

- Il gruppo loghi GEWISS / Talent Garden è dentro le slide, non nella cornice esterna.
- Il logo Talent Garden è stato riequilibrato otticamente rispetto a GEWISS.
- In copertina non deve esserci il vecchio riquadro arancione: lo sfondo usa un gradiente coerente con la palette, più saturo sul lato destro.
- Titolo della copertina organizzato su due righe e loghi allineati a sinistra con il titolo.
- Il titolo “Dal controllo dei dispositivi / alla collaborazione con la casa” ha un’interruzione di riga intenzionale.
- La pagina Insights è stata resa più contemporanea e meno piatta.
- La presentazione supporta il fullscreen con il tasto `F`.
- Navigazione: frecce, Page Up/Page Down, spazio, pulsanti, click sui lati e swipe mobile.

### Link

Link stabile che segue `main`:

`https://htmlpreview.github.io/?https://github.com/Ragno236/Gewiss/blob/main/presentazione.html`

Link congelato alla versione dell’handoff:

`https://htmlpreview.github.io/?https://raw.githubusercontent.com/Ragno236/Gewiss/238a63474a06c37eacfe706724526dc9fbbfa49f/presentazione.html`

## 4. Prototipo iPhone 17

### File

`prototipo-iphone17.html`

### Obiettivo del prodotto

Il prototipo rappresenta GEWISS come agente domestico intelligente chiamato Casper. Il principio è “generare diagnosi, non numeri”: l’interfaccia porta in primo piano poche informazioni rilevanti, propone azioni contestuali e impara gradualmente dalle abitudini della casa. Il tono è calmo, affidabile, non tecnico e non allarmistico.

### Schermate attuali

Il selettore desktop contiene 6 viste:

1. Dashboard
2. Apprendimento
3. Case
4. Widget
5. Profilo
6. Modalità essenziale

Sono accessibili anche con i tasti numerici `1`–`6`.

### Stato e decisioni da preservare

- Tutta la UI è in italiano.
- La tipografia parte da body `10px` e usa la scala: `10, 13, 16, 20, 25, 31, 39, 78px`.
- Le icone/mascotte grafiche di Casper sono state rimosse per ora.
- Sopra “Bentornato.” non deve esserci la label “CASPER”.
- Spaziature, margini e padding sono stati aumentati su tutte le pagine per ridurre l’affollamento.
- La Dashboard contiene una proposta sul riscaldamento, una decisione e una notifica sintetica sull’altra casa.
- Testo attuale della notifica: “Sei fuori da qualche giorno, nell’altra casa sono rimasti alcuni dispositivi accesi.”
- Il testo della notifica ha la stessa dimensione e forza d’asta (`font-weight: 700`) di “Prepara il soggiorno”.
- I pulsanti della notifica hanno corpo e padding coerenti con il pulsante “Riscalda prima”.
- Sono state eliminate le label “1 suggerimento” e “Dall’ultima visita”.
- La schermata Apprendimento usa una mappa delle stanze: la saturazione del colore indica quanto Casper conosce ogni ambiente.
- “Casa relax” è una seconda casa normalmente online e connessa. Selezionarla non deve aprire una schermata offline.
- La Modalità essenziale è una pagina autonoma nel selettore (`06`) per mostrarla volontariamente al cliente.
- Il profilo permette di aprire il form “Aggiungi una casa”, con errore e conferma in italiano.

### Dati correnti delle case

Casa principale:

- Posizione riconosciuta.
- 12 dispositivi.
- 4 routine.
- Comfort buono.
- Tutto connesso.

Casa relax:

- L’utente è altrove.
- Casa connessa.
- 8 dispositivi.
- 2 routine.
- Comfort eco.
- Clima eco e protezione perimetrale attiva.

### Link

Link stabile che segue `main`:

`https://htmlpreview.github.io/?https://github.com/Ragno236/Gewiss/blob/main/prototipo-iphone17.html`

Link congelato alla versione dell’handoff:

`https://htmlpreview.github.io/?https://raw.githubusercontent.com/Ragno236/Gewiss/238a63474a06c37eacfe706724526dc9fbbfa49f/prototipo-iphone17.html`

## 5. Anteprima locale

Avviare il server dalla radice del repository:

```bash
cd "/Users/ragno/Documents/New project"
python3 -m http.server 8765
```

Aprire:

- `http://127.0.0.1:8765/presentazione.html`
- `http://127.0.0.1:8765/prototipo-iphone17.html`

Preferire `http://127.0.0.1` a `file://` per test e automazioni browser.

## 6. Pubblicazione corretta su GitHub

Dopo ogni modifica:

```bash
git diff --check
git status --short
git add presentazione.html
# oppure: git add prototipo-iphone17.html
git commit -m "Descrizione concisa della modifica"
git push origin main
git rev-parse HEAD
```

Mettere in stage soltanto il file coinvolto. Non includere modifiche collaterali.

## 7. Regola importante sui link HTMLPreview

Un URL che contiene uno SHA, per esempio:

`.../raw.githubusercontent.com/Ragno236/Gewiss/238a634.../prototipo-iphone17.html`

è immutabile: continuerà sempre a mostrare quel commit. Dopo una nuova pubblicazione bisogna generare un nuovo link con il nuovo SHA.

Il link con `blob/main/...` segue invece il branch `main`, ma HTMLPreview o il browser possono mostrare temporaneamente una copia in cache. In caso di dubbio:

1. controllare `git rev-parse origin/main`;
2. generare un link `raw.githubusercontent.com` con lo SHA nuovo;
3. fare un hard refresh.

## 8. Checklist prima della consegna

### Presentazione

- Verificare tutte le 8 slide a 16:9.
- Controllare che loghi e testi restino dentro la slide.
- Provare frecce, click, swipe e tasto `F`.
- Controllare le interruzioni di riga dei titoli.

### Prototipo

- Provare le viste `1`–`6` dal selettore.
- Verificare che Casa relax resti nella pagina Case e non apra Modalità essenziale.
- Verificare i pulsanti Dashboard e il form Aggiungi casa.
- Controllare che non esistano overflow orizzontali.
- Verificare la resa nella cornice iPhone e lo scroll verticale.
- Controllare coerenza tipografica, margini e forza d’asta.

## 9. Prompt pronto per Antigravity

```text
Lavora sul repository https://github.com/Ragno236/Gewiss, branch main.

Leggi integralmente HANDOFF-ANTIGRAVITY.md prima di modificare qualsiasi file. I due deliverable sono separati:
- presentazione.html = presentazione cliente;
- prototipo-iphone17.html = prototipo interattivo iPhone 17.

Non creare copie o file alternativi. Modifica esclusivamente il file pertinente alla mia richiesta, preserva le decisioni già documentate, verifica la resa su http://127.0.0.1:8765 e pubblica su main. Dopo il push forniscimi un link HTMLPreview basato sul nuovo SHA del commit, non su uno SHA precedente.
```
