# Guida Cloud per Principianti

Guida pratica e open-source in italiano dedicata a chi vuole muovere i primi passi nel mondo del Cloud Computing. Concetti base, certificazioni, panoramiche sui provider e casi d'uso reali — senza prerequisiti.

> Pensata per chi sente parlare di "cloud" ogni giorno ma non sa ancora da dove iniziare.

---

## Cosa trovi in questa guida

- Differenze tra IaaS, PaaS e SaaS spiegate con analogie semplici
- Confronto tra i tre grandi provider: AWS, Azure, GCP
- Roadmap certificazioni entry-level con costi e ordine consigliato
- Casi d'uso reali: e-commerce, backup, serverless
- Risorse gratuite per studiare: corsi, canali YouTube, documentazione

---

## I Modelli di Servizio

| Modello | Significato | Cosa gestisci tu | Esempi |
|---|---|---|---|
| **On-Premises** | Tutto in casa | Hardware, OS, Rete, Dati, App | Data center aziendale, Homelab |
| **IaaS** | Infrastructure as a Service | OS, Dati, App | Amazon EC2, Azure VM |
| **PaaS** | Platform as a Service | Dati, App | Heroku, Google App Engine |
| **SaaS** | Software as a Service | Solo utilizzo | Gmail, Microsoft 365, Dropbox |

---

## I Provider Principali

| Provider | Sviluppatore | Quota Mercato | Punto di forza |
|---|---|---|---|
| **AWS** | Amazon | ~32% | Leader di mercato, ecosistema vastissimo |
| **Azure** | Microsoft | ~23% | Ideale per ambienti Enterprise e Microsoft 365 |
| **GCP** | Google | ~10% | Eccellente per Big Data, ML e Kubernetes |

---

## Architettura Cloud vs On-Premise

```
Utente
  │
  ▼
Internet
  │
  ├── Cloud Pubblico (AWS, Azure, GCP)
  │     └── Server di terze parti, scalabili, pay-as-you-go
  │
  ├── Cloud Privato (Data Center)
  │     └── Server proprietari, rete chiusa, controllo totale
  │
  └── Cloud Ibrido
        └── Mix strategico tra infrastruttura pubblica e privata
```

---

## Certificazioni Entry-Level

| Certificazione | Provider | Livello | Costo |
|---|---|---|---|
| **AZ-900** Azure Fundamentals | Microsoft | Principiante | ~165€ |
| **AWS Cloud Practitioner** CLF-C02 | Amazon | Principiante | ~100€ |
| **Google Cloud Digital Leader** | Google | Principiante | ~200€ |

**Ordine consigliato:** AZ-900 → AWS CCP → Google CDL

---

## Struttura del Repository

```
guida-cloud-principianti/
├── README.md
├── 01-Le-Basi/
│   ├── 1-modelli-cloud.md          # IaaS, PaaS, SaaS (Analogia della Pizza)
│   └── 2-tipi-di-cloud.md          # Pubblico, Privato, Ibrido
├── 02-I-Provider/
│   └── 1-panoramica-provider.md    # Differenze tra AWS, Azure e GCP
├── 03-Certificazioni/
│   └── 1-roadmap-principianti.md   # Roadmap esami e costi
├── 04-Casi-d-Uso/
│   └── 1-scenari-reali.md          # E-commerce, Backup, Serverless
└── 05-Risorse-Utili/
    └── 1-link-e-corsi.md           # Piattaforme di studio e canali YouTube
```

---

## Casi d'Uso Pratici

**Siti Web Scalabili** — Auto-scaling per gestire picchi di traffico (es. Black Friday) senza crash o sovra-provisioning.

**Disaster Recovery** — Backup distribuiti geograficamente per azzerare il rischio di perdita dati in caso di guasto.

**Architetture Serverless** — Esecuzione di codice a evento pagando solo i millisecondi di utilizzo effettivo.

---

## Note

- Il materiale è pensato per **principianti assoluti** — non è richiesta programmazione
- L'obiettivo è fornire una mappa per orientarsi tra gli acronimi del cloud
- Progetto open-source: puoi contribuire aprendo una Pull Request

---

## Autore

**Nicholas Izzo** — Sistemista, studente L31 Informatica (specializzazione AI) @ Università Pegaso

[nicholasiszzo.github.io](https://NicholasIzzo.github.io) · [Homelab](https://github.com/NicholasIzzo/homelab) · [AI Practical Guide](https://github.com/NicholasIzzo/ai-practical-guide)
