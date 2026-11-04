# 🎵 MelodyHarmonizer

> **Generatore melodico algoritmico guidato da progressioni armoniche in tonalità maggiore e minore.**  
> Progettato per compositori, produttori musicali, studenti di teoria musicale e sound designer.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Tone.js](https://img.shields.io/badge/Tone.js-Web_Audio-purple?style=flat-square)
![MIDI](https://img.shields.io/badge/Standard_MIDI-0_/_1-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## 📖 Indice

- [Panoramica](#-panoramica)
- [Funzionalità Principali](#-funzionalità-principali)
- [Guida Rapida all'Uso](#-guida-rapida-alluso)
- [Parametri Algoritmici & Sintesi](#-parametri-algoritmici--sintesi)
- [Database delle Progressioni Incluse](#-database-delle-progressioni-incluse)
- [Workflow con DAW & Esportazione MIDI](#-workflow-con-daw--esportazione-midi)
- [Architettura Tecnica](#-architettura-tecnica)
- [Installazione & Pubblicazione su GitHub Pages](#-installazione--pubblicazione-su-github-pages)
- [Licenza](#-licenza)

---

## 🌟 Panoramica

**MelodyHarmonizer** risolve uno dei blocchi creativi più frequenti: come generare linee melodiche espressive e varie che mantengano al contempo una perfetta coerenza con gli accordi sottostanti.

A differenza dei generatori pseudo-casuali tradizionali, l'algoritmo di MelodyHarmonizer opera applicando le regole dell'armonia tonale:

1. Analizza la tonalità e l'accordo attivo in ciascuna misura.
2. Identifica le **note dell'accordo** (*chord tones*: tonica, 3ª, 5ª, 7ª) e le **note di passaggio** (*passing tones* della scala).
3. Pondera l'assegnazione delle altezze in funzione della **metrica musicale** (tempi forti vs tempi deboli) e di contorni melodici naturali (ad arco, a onda o a grado congiunto).

---

## ✨ Funzionalità Principali

- 🎹 **Database Armonico Curato:** Le progressioni più celebri della storia della musica classica, pop, jazz, rock, R&B e colonne sonore cinematografiche.
- 🎼 **Piano Roll Interattivo in Tempo Reale:** Tracciamento visuale delle note con codifica cromatica differenziata per tonica, note dell'accordo e note di passaggio della scala.
- 🧠 **Controlli Algoritmici Avanzati:** Personalizzazione della percentuale di aderenza armonica, della densità ritmica, della forma metrica (`AABA`, `AABB`, `ABCD`) e del profilo di fraseggio.
- 🔊 **Engine Audio Tone.js Integrato:** Sintesi FM, lead sottrattivo con filtri risonanti, pianoforte elettrico caldo, riverbero stereofonico spaziale e ping-pong delay.
- 💾 **Esportazione MIDI Nativa (.mid):** Generazione binaria istantanea e compatibile con qualsiasi DAW (Ableton Live, FL Studio, Logic Pro, Cubase, Reaper, GarageBand).
- 🚀 **Zero Dipendenze di Build:** Funziona come singola pagina autonoma nel browser senza necessità di `npm install`, Webpack o Vite.

---

## 🕹 Guida Rapida all'Uso

### 1. Selezione di Tonalità e Modo

- Dal box **Tonalità & Modo**, seleziona la nota fondamentale (es. *Do / C*, *Fa# / F#*) e il modo di riferimento (*Maggiore*, *Minore Naturale*, *Minore Armonica* o *Modo Dorico*).
- L'indicatore sottostante mostrerà in tempo reale le note che compongono la scala prescelta.

### 2. Scelta della Sequenza Armonica

- Nel menu **Progressioni Armoniche Celebri**, scegli la sequenza desiderata.
- Le 4 misure sottostanti si aggiorneranno visualizzando le sigle degli accordi, il grado in numeri romani e le singole note costituenti di ogni triade o quadriade.

### 3. Generazione della Melodia

- Clicca sul pulsante **Genera Melodia** (o usa le scorciatoie di mutazione rapida **Varia Note** / **Nuovo Ritmo**).
- Verrà calcolato istantaneamente un nuovo percorso melodico coerente con la griglia armonica.

### 4. Riproduzione & Ispezione

- Premi **Riproduci** o premi la **Barra Spaziatrice** per avviare il motore audio.
- Il playhead rosso scorrerà sul Piano Roll evidenziando la battuta attiva e le card degli accordi correnti.
- Puoi fare clic in qualsiasi punto del Piano Roll per ascoltare singole altezze con il timbro attivo.

---

## ⚙ Parametri Algoritmici & Sintesi

| Controllo                | Valori                                          | Descrizione Musicale                                                                                                      |
|:------------------------ |:----------------------------------------------- |:------------------------------------------------------------------------------------------------------------------------- |
| **Aderenza Armonica**    | $40\% - 100\%$                                  | Definisce quante note cadranno rigorosamente sulle note dell'accordo rispetto alle note di passaggio della scala.         |
| **Densità Ritmica**      | Spaziosa, Bilanciata, Fitta, Arpeggiata         | Determina i valori di durata (interi, metà, quarti, ottavi o sedicesimi sincopati).                                       |
| **Profilo / Contorno**   | Ad Arco, Onda, Grado Congiunto, Salti           | Guida l'andamento geometrico della linea melodica (salita verso il culmine e discesa distensiva, moto sinusoidale, ecc.). |
| **Pattern di Fraseggio** | `AABA`, `AABB`, `ABCD`                          | Stabilisce la simmetria tematica fra le 4 misure (es. ripetizione della battuta 1 nella battuta 2 con ponte e ripresa).   |
| **Umanizzazione**        | $0\% - 60\%$                                    | Introduce micro-variazioni dinamiche della velocity per simulare un'esecuzione umana non quantizzata rigidamente.         |
| **Timbro Lead**          | Electric Piano, Synth Lead, Bell, Pluck, Flauto | Modifica il modello di sintesi sonora (FM, sottrattiva, a inviluppo percussivo).                                          |

---

## 📚 Database delle Progressioni Incluse

### Tonalità Maggiore

1. **Pop Axis (`I - V - vi - IV`):** La sequenza più usata nella storia delle classifiche globali (The Beatles, U2, Coldplay, Journey).
2. **Jazz Cadence (`ii7 - V7 - Imaj7 - vi7`):** Circolo delle quinte discendenti e perno fondamentale dell'armonia jazz e bossa nova.
3. **Rock & Blues (`I - IV - V - IV`):** Semplice, energica e propulsiva; cardine del rock delle origini e garage rock.
4. **50s Doo-Wop (`I - vi - IV - V`):** Dolce e nostalgica, celebre per evergreen come *Stand By Me* e le ballad classiche.
5. **Sensibile / Introspettiva (`vi - IV - I - V`):** Inizia sulla relativa minore fornendo drammatismo cinematografico ed enfasi epica.
6. **Royal Road / Oudo (`IVmaj7 - V7 - iii7 - vi`):** Popolarissima nel J-Pop, City Pop e colonne sonore anime per il suo colore agrodolce.
7. **Canone Barocco (`I - V - vi - iii`):** Architettura discendente barocca basata sul Canone in Re di Pachelbel.

### Tonalità Minore

1. **Dark Pop (`i - VI - III - VII`):** Tensione oscura e aperture epiche (Radiohead, Muse, Billie Eilish).
2. **Cadenza Andalusa (`i - VII - VI - V`):** Basso discendente a gradi congiunti tipico del flamenco e del rock passionale.
3. **Jazz Minore (`iiø7 - V7b9 - i - i`):** Armonia sofisticata ricca di dissonanze e risoluzioni noir.
4. **Classica Drammatica (`i - iv - V - i`):** Tensione formale bachiana con la sensibile sollevata dell'accordo di dominante maggiore.
5. **R&B / Neo-Soul (`i7 - v7 - VImaj7 - VII`):** Uso del quinto grado minore per un andamento vellutato e rilassato senza cadenze aspre.
6. **Epic Cinematic (`i - VI - iv - V`):** Crescendo tragico e drammatico impiegato nei temi sonori per il grande schermo.

---

## 🎛 Workflow con DAW & Esportazione MIDI

1. Crea la melodia desiderata all'interno della webapp.
2. Clicca su **Scarica .MID**.
3. Verrà generato un file MIDI Standard conforme contenente due tracce logicamente separate:
   - **Canale 1:** Linea melodica principale con timing quantizzato ed espressività di velocity.
   - **Canale 2:** Accompagnamento armonico polifonico a supporto.
4. Trascina direttamente il file `.mid` salvato all'interno del sequencer della tua DAW:
   - Assegna al canale melodico il tuo VST/instrument preferito (Serum, Omnisphere, Kontakt, Diva, Vital, ecc.).
   - Utilizza la traccia accordi per pilotare pad orchestrali, pianoforti o sintetizzatori polifonici.

---

## 🛠 Architettura Tecnica

- **Motore Audio & Scheduling:** Gestito interamente da [Tone.js](https://tonejs.github.io/) tramite l'API nativa `Web Audio`. Tutti gli eventi usano il transport ad alta precisione con lookahead per evitare jitter temporale.
- **Visualizer Piano Roll:** Sviluppato su Canvas HTML5 dinamico con compensazione del pixel ratio Retina (`devicePixelRatio`) per rendering nitido a qualsiasi risoluzione.
- **Algoritmo MIDI Standalone:** Costruzione binaria dei chunk `MThd` e `MTrk` con delta-time Variable-Length Quantity (VLQ) senza necessità di librerie pesanti di terze parti.
- **Interfaccia Utente:** Stilizzata tramite classi funzionali [Tailwind CSS](https://tailwindcss.com/) con layout responsive adattabile a tablet e desktop.

---

## 🚀 Installazione & Pubblicazione su GitHub Pages

Non è richiesta alcuna compilazione. Il progetto è composto da un unico file `index.html`.

### Esecuzione in Locale

Puoi aprirlo direttamente facendo doppio clic su `index.html`, oppure avviando un server di sviluppo locale:

```bash
# Con Python 3
python3 -m http.server 8000

# Oppure con Node (npx)
npx serve .
```

Apri quindi `http://localhost:8000` nel browser.

---

## 📄 Licenza

Distribuito sotto licenza **MIT**. Consulta il file `LICENSE` per ulteriori dettagli.  
Sentiti libero di clonare, modificare, estendere e utilizzare le melodie generate per le tue produzioni musicali personali o commerciali!
