# Scenari Reali — Come il Cloud viene usato in Azienda

La teoria ha senso solo quando la colleghi a casi concreti. Questi sono tre scenari reali che spiegano perché le aziende scelgono il cloud.

---

## Scenario 1 — Sito E-commerce con Picchi di Traffico

### Il problema
Un e-commerce italiano ha un traffico normale di 1.000 visitatori al giorno. Durante il Black Friday, il traffico schizza a 50.000 visitatori in poche ore.

**Senza cloud:**
- Compri server dimensionati per 50.000 utenti
- Per 360 giorni l'anno quei server sono quasi inutilizzati
- Costi fissi altissimi, rischio di crash comunque

**Con cloud (IaaS + Auto Scaling):**
```
Traffico normale          Picco Black Friday
─────────────────         ──────────────────
2 istanze attive          20 istanze attive
                          (scalate automaticamente)
                              │
                          Tornato normale
                              │
                          2 istanze attive
                          (le altre spente)
```

**Risultato:** Paghi per 2 istanze per 360 giorni e per 20 istanze solo durante il picco. Risparmio stimato: 70-80% rispetto all'infrastruttura fissa.

**Servizi utilizzati:**
- AWS: EC2 + Auto Scaling + Elastic Load Balancer
- Azure: Virtual Machine Scale Sets + Load Balancer
- GCP: Managed Instance Groups + Cloud Load Balancing

---

## Scenario 2 — Disaster Recovery

### Il problema
Un'azienda ha il suo server principale in un data center a Milano. Se il data center va a fuoco, alluvione o subisce un blackout prolungato — tutto si ferma e i dati potrebbero andare persi.

**Senza cloud:**
- Secondo data center fisico → costi enormi
- Backup su nastro → ripristino richiede ore o giorni
- RTO (Recovery Time Objective) alto

**Con cloud:**
```
Data Center Milano          Cloud (es. Azure North Europe)
──────────────────          ────────────────────────────────
Server primario    ──────>  Replica continua dei dati
                            VM in standby (spente = costo zero)
                                │
                            Guasto a Milano
                                │
                            VM si accendono in automatico
                            Traffico reindirizzato
                            RTO: minuti invece di giorni
```

**Risultato:** Business continuity garantita con costi minimi. Le VM in standby nel cloud non costano finché sono spente — paghi solo lo storage per la replica.

**Concetti chiave:**
- **RPO** (Recovery Point Objective): quanti dati posso perdere? Con replica continua → quasi zero
- **RTO** (Recovery Time Objective): quanto tempo per tornare online? Con cloud → minuti

---

## Scenario 3 — Architettura Serverless

### Il problema
Una startup deve inviare una email di conferma ogni volta che un utente si registra. Con un server tradizionale, devi mantenere attivo un processo 24/7 che gestisce le email — anche di notte quando non arriva nessuna registrazione.

**Con serverless:**
```
Utente si registra
        │
        ▼
Evento trigger (es. nuovo record nel DB)
        │
        ▼
Funzione Lambda/Azure Function si avvia
(dura 200ms, elabora l'email)
        │
        ▼
Email inviata → Funzione si spegne
```

**Costi:**
- Modello tradizionale: server attivo 24/7 = ~30€/mese
- Serverless: paghi solo i 200ms × numero di esecuzioni
- Con 10.000 registrazioni/mese → meno di 0.20€

**Quando usare serverless:**
- Task discontinui e a breve durata
- Elaborazione di eventi (upload file, webhook, notifiche)
- API con traffico variabile
- Automazioni e cron job

**Quando NON usare serverless:**
- Processi lunghi (>15 minuti per Lambda)
- Applicazioni che richiedono stato persistente
- Workload costanti e prevedibili (conviene un server dedicato)

---

## Scenario 4 — Startup che scala da 0 a 1 milione di utenti

### Il percorso tipico

```
Fase 1 — MVP (0-1.000 utenti)
    Una singola VM piccola, tutto su un server
    Costo: ~20€/mese

Fase 2 — Crescita (1.000-100.000 utenti)
    Separa database dal server web
    Aggiungi CDN per i file statici
    Costo: ~200€/mese

Fase 3 — Scala (100.000-1.000.000 utenti)
    Load balancer + multiple VM
    Database managed con replica
    Cache con Redis
    Costo: ~2.000€/mese

Fase 4 — Enterprise (1.000.000+ utenti)
    Architettura microservizi
    Kubernetes per orchestrazione
    Multi-region deployment
    Costo: variabile
```

**Il vantaggio del cloud:** ogni fase si raggiunge senza cambiare provider, senza migrazioni complesse e pagando solo quello che serve in quel momento.

---

> Questi scenari mostrano che il cloud non è solo "mettere i server su internet" — è un cambiamento nel modo di pensare all'infrastruttura: da risorsa fissa a risorsa elastica.
