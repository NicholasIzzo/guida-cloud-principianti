# Modelli di Servizio Cloud

Quando si parla di cloud, la prima cosa da capire è **cosa gestisce il provider e cosa gestisci tu**. I modelli di servizio rispondono esattamente a questa domanda.

---

## L'analogia della pizza

Il modo più semplice per capire IaaS, PaaS e SaaS è paragonarli a come mangi una pizza.

```
On-Premises    IaaS           PaaS           SaaS
─────────────  ─────────────  ─────────────  ─────────────
Fai tutto      Usi il forno   Usi il forno   Ordini a
in casa        di qualcuno    e gli ingredienti domicilio
               ma cucini tu   pronti
```

| Modello | Significato | Gestisci tu | Gestisce il provider | Esempi |
|---|---|---|---|---|
| **On-Premises** | Tutto in casa | Hardware, OS, rete, dati, app | Niente | Data center aziendale, homelab |
| **IaaS** | Infrastructure as a Service | OS, dati, app | Hardware, rete, virtualizzazione | Amazon EC2, Azure VM, Google Compute Engine |
| **PaaS** | Platform as a Service | Dati e app | Tutto il resto incluso OS e runtime | Heroku, Azure App Service, Google App Engine |
| **SaaS** | Software as a Service | Solo l'utilizzo | Tutto | Gmail, Microsoft 365, Dropbox, Notion |

---

## On-Premises

Tutto il hardware è fisicamente tuo — server, rack, switch, alimentatori. Tu compri, installi, mantieni e aggiorni tutto.

**Vantaggi:**
- Controllo totale su dati e infrastruttura
- Nessun costo ricorrente per il cloud
- Latenza minima per applicazioni locali

**Svantaggi:**
- Costi iniziali elevati
- Scalabilità lenta e costosa
- Responsabilità completa per guasti e sicurezza

---

## IaaS — Infrastructure as a Service

Il provider ti fornisce l'infrastruttura virtualizzata (CPU, RAM, storage, rete). Tu ci installi sopra il sistema operativo e tutto il resto.

**Quando usarlo:**
- Hai bisogno di controllo sull'OS e sulla configurazione
- Stai migrando server fisici sul cloud (lift & shift)
- Vuoi scalare rapidamente senza comprare hardware

**Esempi pratici:**
- Spinare una VM Ubuntu su Azure per ospitare un'applicazione
- Usare Amazon EC2 per un server web scalabile
- Google Compute Engine per workload di calcolo

---

## PaaS — Platform as a Service

Il provider gestisce anche il sistema operativo, il runtime e il middleware. Tu ti concentri solo sul codice e sui dati.

**Quando usarlo:**
- Vuoi deployare un'applicazione senza gestire server
- Il tuo team è piccolo e non vuole occuparsi di infrastruttura
- Hai bisogno di scalabilità automatica

**Esempi pratici:**
- Deployare un'app Node.js su Heroku senza configurare nessun server
- Azure App Service per un'applicazione .NET
- Google App Engine per un backend Python

---

## SaaS — Software as a Service

Usi direttamente un'applicazione via browser o app. Non gestisci nulla — solo usi il software.

**Quando usarlo:**
- Hai bisogno di uno strumento pronto all'uso
- Non vuoi (o non puoi) gestire l'infrastruttura
- Vuoi aggiornamenti automatici e zero manutenzione

**Esempi pratici:**
- Gmail per la posta aziendale
- Microsoft 365 per documenti e collaborazione
- Salesforce per il CRM

---

## Come scegliere

```
Hai bisogno di controllo totale sull'infrastruttura?
    → On-Premises o IaaS

Vuoi deployare codice senza gestire server?
    → PaaS

Ti serve uno strumento pronto all'uso?
    → SaaS
```

---

> La maggior parte delle aziende usa tutti e tre i modelli contemporaneamente — SaaS per produttività (email, documenti), PaaS per applicazioni interne, IaaS per workload che richiedono controllo.
