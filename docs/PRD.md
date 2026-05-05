# Artly — Product Requirements Document

**Author:** Archetipo
**Date:** 2026-05-04
**Version:** 1.0

---

## Elevator Pitch

> Per i **neofiti curiosi** e i **creativi in cerca di ispirazione**, che hanno il problema di **non sapere cosa li attira nel mondo dell'arte**, **Artly** è un'**app mobile-first** che **trasforma la scoperta artistica in un gioco intuitivo, costruendo una mappa personalizzata dei propri gusti estetici**. A differenza di **gallerie online statiche o guide museali tradizionali**, il nostro prodotto **parte dalle reazioni istintive dell'utente per costruire un profilo di gusto unico e vivo, suggerendo opere e esperienze sempre più personalizzate**.

---

## Vision

Artly rende l'arte accessibile a chiunque, eliminando la barriera del "non me ne intendo". Vogliamo che ogni persona possa scoprire cosa la muove esteticamente — non attraverso studi o competenze, ma attraverso l'istinto e il gioco. Artly diventa il punto di ingresso nel mondo dell'arte per la generazione che swipa.

### Product Differentiator

Artly non è una galleria, non è un marketplace, non è un corso. È uno **strumento di auto-conoscenza estetica**. L'utente non viene giudicato per ciò che non sa — viene guidato a scoprire ciò che già sente. La mappa dei gusti non è un quiz da social media: è un riflesso vivo delle preferenze che si affina nel tempo, alimentato da un catalogo vasto e diversificato di opere reali da musei internazionali.

---

## User Personas

### Persona 1: Marco

**Role:** Neofita curioso
**Age:** 28 | **Background:** Lavora nel tech, nessuna formazione artistica

**Goals:**
- Capire cosa gli piacea nell'arte senza sentirsi ignorante
- Avere qualcosa di semplice e divertente da usare nei momenti liberi
- Condividere con gli amici una scoperta interessante su di sé

**Pain Points:**
- Si sente in colpa quando entra in un museo e "non capisce"
- Non sa da dove iniziare nel mondo dell'arte
- Le app esistenti sono troppo accademiche o troppo superficiali

**Behaviors & Tools:**
- Usa Instagram, Spotify, app con UX fluida
- Swipe naturale, consuma contenuti in sessioni brevi (5-10 minuti)
- Motivato da progressione visiva e piccole ricompense

**Motivations:** Curiosità, auto-conoscenza, social sharing
**Tech Savviness:** Alta — usa quotidianamente app mobile

#### Customer Journey — Marco

| Phase | Action | Thought | Emotion | Opportunity |
|---|---|---|---|---|
| Awareness | Vede la mappa di un amico su Instagram | "Aspetta, anche tu hai gusti nell'arte?" | Curiosità | Share virale della mappa |
| Consideration | Scarica l'app, vede che è semplice | "Non servono competenze, è un gioco" | Rassicurato | Onboarding chiaro, zero friction |
| First Use | Swipe 10 quadri, vede la barra di avanzamento | "Non pensavo avessi un gusto!" | Divertito, sorpreso | Progress bar + primo mini-insight |
| Regular Use | Torna ogni giorno per lo streak, sblocca badge | "Sono più Rinascimento o Impressionismo?" | Orgoglioso, curioso | Gamification + mappa che si affina |
| Advocacy | Condivide la mappa, invita amici | "Guarda, sono 60% Barocco!" | Fiero | Social share nativo |

---

### Persona 2: Giulia

**Role:** Creativa in cerca di ispirazione
**Age:** 22 | **Background:** Studentessa di design, sensibile all'estetica

**Goals:**
- Ampliare i propri riferimenti visivi oltre il noto
- Scoprire artisti e periodi che non conosce
- Usare Artly come fonte di ispirazione per i propri progetti

**Pain Points:**
- Pinterest è dispersivo e non strutturato per l'arte
- Le fonti accademiche sono noiose e lente
- Vuole qualcosa di curato ma accessibile

**Behaviors & Tools:**
- Usa Pinterest, Behance, Dribbble, Spotify
- Consuma contenuti con intenzione, salva e colleziona
- Condivide contenuti estetici con la propria community

**Motivations:** Ispirazione, scoperta, identità culturale, community
**Tech Savviness:** Molto alta — early adopter

#### Customer Journey — Giulia

| Phase | Action | Thought | Emotion | Opportunity |
|---|---|---|---|---|
| Awareness | Trova Artly citato in un blog di design | "Finalmente qualcosa di serio per l'arte" | Interessata | Content marketing su blog creativi |
| Consideration | Legge che ha opere dal Met e Rijksmuseum | "Questo ha contenuti reali, non roba stock" | Convinta | Pagina landing con catalogo esempio |
| First Use | Swipa con intenzione, salva opere, esplora epoche | "Sto scoprendo cose che non sapevo" | Stimolata | Funzione "esplora" + collezione |
| Regular Use | Usa la collezione come moodboard, scopre marketplace | "Questo artista emergente è perfetto per il mio progetto" | Ispirata | Marketplace + raccomandazioni |
| Advocacy | Condivide su Behance, porta le amiche | "Questo è il mio profilo estetico" | Ambasciatrice | Profilo condivisibile + community |

---

## Brainstorming Insights

> Key discoveries and alternative directions explored during the inception session.

### Assumptions Challenged

- **"Le persone vogliono conoscere i propri gusti"** — Non necessariamente. Il motore non è l'auto-conoscenza dichiarata, ma il divertimento del gioco. La mappa dei gusti è un effetto collaterale piacevole, non l'obiettivo.
- **"Il formato Tinder funziona per dating"** — La ricompensa nel dating è il match. In Artly, la ricompensa è la progressione visiva e la mappa finale. Bisogna progettare una ricompensa che tenga l'utente dopo il decimo quadro.
- **"Il catalogo è secondario"** — Al contrario: la diversità e qualità del catalogo è vita o morte del prodotto. Se le immagini sono noiose o ripetitive, l'utente non torna.

### New Directions Discovered

- **La mappa come identità social:** Profili estetici condivisibili ("Sono 73% Rinascimento, 18% Impressionismo") — virale per natura, simile al "qual è il tuo animale spirituale" ma per l'arte.
- **Goodreads dell'arte (Vision):** Non solo gusti personali, ma catalogo di cosa hai visto nei musei reali, recensioni, percorsi.
- **B2B Education (Vision):** Insegnanti d'arte che usano Artly in classe — studenti swipano e discutono i gusti. Mercato educativo.
- **Le tre leve di monetizzazione** possono coesistere: freemium (MVP), marketplace (Growth), esperienze fisiche (Vision).

---

## Product Scope

### MVP — Minimum Viable Product

- Autenticazione utente (OAuth GitHub/Google via Supabase — già configurato)
- Feed di immagini d'arte swipabili (piace / non piace / esplora / salva)
- Card opera con titolo, artista, epoca, stile
- Tracking delle preferenze per epoca, stile e palette cromatica
- Generazione della mappa dei gusti dopo ~50 swipe
- Mappa mostra percentuali per epoca, stile e palette
- Profilo utente con collezione "salvati"
- Barra di avanzamento verso la mappa
- Evitare di mostrare opere già swipate
- Condivisione base della mappa (link/screenshot)
- Mappa si aggiorna dinamicamente ad ogni sessione
- Cache delle immagini per performance
- Freemium: mappa base gratuita, dettagli premium

### Growth Features (Post-MVP)

- Badge, streak e gamification completa
- Feed "Scopri" con raccomandazioni basate su gusti
- Marketplace artisti emergenti
- Condivisione social nativa (Instagram Stories, etc.)
- Profilo estetico avanzato (composizione, soggetto, tecnica)
- Algoritmo di raccomandazione intermedio (clustering)
- Integrazione con musei locali

### Vision (Future)

- Esperienze fisiche (biglietti mostre, percorsi città)
- "Goodreads dell'arte" — catalogo personale delle opere viste dal vivo
- B2B Education — strumento per insegnanti d'arte
- Community e commenti sulle opere
- Profilo estetico con embedding vettoriali (ML)

---

## Technical Architecture

> **Proposed by:** Leonardo (Architect)

### System Architecture

Architettura Modular Monolith su Next.js 15, con backend e frontend nello stesso progetto. Le opere d'arte provengono da API esterne (musei internazionali), aggregate tramite adapter pattern e cachate lato server per performance e resilienza.

**Architectural Pattern:** Modular Monolith (App Router)

**Main Components:**
- **Web App (Next.js 15):** UI swipe, mappa, profilo, collezione
- **API Routes:** Proxy opere, registrazione swipe, calcolo mappa, raccomandazioni
- **Prisma + PostgreSQL (Supabase):** Persistenza utenti, swipe, collezioni, mappa gusti
- **Supabase Auth:** Autenticazione OAuth
- **Art Adapters:** Integrazione con Met, Art Institute of Chicago, Rijksmuseum
- **Taste Engine:** Calcolo percentuali per epoca/stile/palette (algoritmo semplice, Opzione A)

### Technology Stack

| Layer | Technology | Version | Rationale |
|---|---|---|---|
| Language | TypeScript | 5.x | Tipizzazione forte, ecosistema Next.js |
| Frontend Framework | Next.js (React) | 15.x / 19.x | Boilerplate esistente, App Router, SSR/ISR |
| CSS | Tailwind CSS | v4 | Boilerplate esistente, utility-first |
| UI Components | shadcn/ui | latest | Boilerplate esistente, componenti accessibili |
| Backend | Next.js API Routes | 15.x | Stesso progetto, zero overhead infrastrutturale |
| Database | PostgreSQL (Supabase) | 16 | Boilerplate esistente, affidabile |
| ORM | Prisma | 5.x | Boilerplate esistente, type-safe |
| Auth | Supabase Auth | - | Boilerplate esistente, OAuth configurato |
| Storage | Supabase Storage | - | Per cache immagini opere se necessario |
| Deploy | Vercel | - | Boilerplate esistente, ottimizzato per Next.js |

### Project Structure

**Organizational pattern:** Feature-based con directory `app/` per route e `lib/` per logica

```
src/
  app/
    page.tsx                  # Landing / onboarding
    swipe/page.tsx            # Schermata principale di swipe
    map/page.tsx              # Mappa dei gusti
    collection/page.tsx       # Collezione salvati
    profile/page.tsx          # Profilo utente
    share/[id]/page.tsx       # Pagina condivisione mappa
    api/
      artworks/route.ts       # Proxy API opere (cache + shuffle)
      swipe/route.ts          # Registra swipe utente
      map/route.ts            # Calcola mappa gusti
      recommendations/route.ts # Raccomandazioni base
  components/
    ui/                       # shadcn/ui esistenti
    swipe-card.tsx            # Card opera con swipe gestures
    art-map.tsx               # Visualizzazione mappa gusti
    progress-bar.tsx          # Barra avanzamento verso mappa
    badge.tsx                 # Componente badge gamification
  lib/
    prisma.ts                 # Già esistente
    supabase/                 # Già esistente
    artworks/
      met.ts                  # Adapter API Metropolitan Museum
      artic.ts                # Adapter API Art Institute of Chicago
      rijksmuseum.ts          # Adapter API Rijksmuseum
      index.ts                # Unified fetcher + caching
    taste-engine.ts           # Calcolo mappa gusti
    recommendations.ts        # Algoritmo raccomandazioni
prisma/
  schema.prisma               # Esteso con nuovi modelli
```

### Development Environment

- **Runtime:** Node.js 20+
- **Dev server:** `npm run dev` (Turbopack)
- **Database:** Supabase cloud (PostgreSQL)
- **Dev tools:** Prisma Studio (`npx prisma studio`), Supabase Dashboard

**Required tools:** Node.js 20+, npm, Supabase CLI (opzionale per local dev)

### CI/CD & Deployment

**Build tool:** Next.js built-in (Turbopack per dev, Webpack per prod)

**Pipeline:** Push su GitHub → Vercel auto-deploy

**Deployment:** Vercel (serverless, edge functions per API routes)

**Target infrastructure:** Vercel (scalabile, zero configurazione per Next.js)

### Architecture Decision Records (ADR)

| # | Decision | Rationale |
|---|---|---|
| ADR-001 | Usare il boilerplate esistente invece di React Native | Velocità di sviluppo, zero configurazione infrastrutturale, web responsive su mobile |
| ADR-003 | Adapter pattern per API musei | Astrazione uniforme, facilità di aggiungere nuove fonti, resilienza |
| ADR-004 | Taste engine semplice (percentuali per categoria) | Trasparenza per l'utente, velocità di implementazione, evoluzione futura verso ML |
| ADR-005 | Cache server-side delle opere | Indipendenza da disponibilità API esterne, performance, UX fluida |
| ADR-006 | Freemium come modello MVP | Barriera d'ingresso zero, conversione naturale su mappa dettagliata |

---

## Functional Requirements

| # | Requisito | Area |
|---|---|---|
| FR1 | L'utente può autenticarsi tramite OAuth (GitHub, Google) | Auth |
| FR2 | L'app presenta opere d'arte in formato card swipabile | Core |
| FR3 | L'utente può swipare: piace, non piace, esplora, salva | Core |
| FR4 | Le opere mostrate includono titolo, artista, epoca, stile | Core |
| FR5 | Lo swipe viene registrato con metadata dell'opera | Data |
| FR6 | Dopo ~50 swipe, l'utente sblocca la mappa dei gusti | Gamification |
| FR7 | La mappa mostra percentuali per epoca, stile e palette | Map |
| FR8 | L'utente può salvare opere in una collezione personale | Collection |
| FR9 | L'utente può condividere la propria mappa (link/screenshot) | Social |
| FR10 | La mappa si aggiorna dinamicamente ad ogni nuova sessione | Map |
| FR11 | L'utente vede una barra di avanzamento verso la mappa | UX |
| FR12 | Il feed evita di mostrare opere già swipate | Core |
| FR13 | L'utente può visualizzare e modificare il proprio profilo | Profile |
| FR14 | L'app pre-carica e cache le immagini per performance | Performance |

---

## Non-Functional Requirements

### Security

- Dati utente protetti via Supabase Auth (JWT, refresh token rotation)
- Nessun dato PII esposto nelle API pubbliche
- Row Level Security (RLS) su Supabase per isolamento dati utente
- HTTPS su tutte le comunicazioni (Vercel default)

### Integrations

- **The Metropolitan Museum of Art API** — opere dominio pubblico, no API key
- **Art Institute of Chicago API** — opere open access, no API key
- **Rijksmuseum API** — alta risoluzione, API key gratuita
- **Supabase Auth** — OAuth provider (GitHub, Google)
- **Vercel** — hosting e deploy

---

## Next Steps

1. **UX Design** — Wireframe dettagliati per flow swipe, mappa e profilo
2. **Backlog** — Decomposizione dei 14 FR in epics e user stories
3. **Sviluppo** — Implementazione incrementale partendo dal core (swipe + catalogo)
4. **Validazione** — Test con 10-20 utenti beta per verificare retention e engagement

---

_PRD generated via Archetipo Product Inception — 2026-05-04_
_Session conducted by: User with the Archetipo team_
