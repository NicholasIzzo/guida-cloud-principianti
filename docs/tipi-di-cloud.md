# Tipi di Cloud

Oltre ai modelli di servizio, il cloud si distingue anche per **dove si trovano fisicamente le risorse** e **chi le gestisce**.

---

## Cloud Pubblico

Le risorse (server, storage, rete) sono di proprietà del provider e condivise tra migliaia di clienti. Tu accedi via internet e paghi solo quello che usi.

**Provider principali:** AWS, Microsoft Azure, Google Cloud

**Caratteristiche:**
- Pay-as-you-go — paghi solo l'utilizzo effettivo
- Scalabilità immediata — aggiungi risorse in pochi secondi
- Nessuna manutenzione hardware — ci pensa il provider
- Disponibile ovunque nel mondo

**Ideale per:**
- Startup e PMI che non vogliono investire in hardware
- Applicazioni con traffico variabile
- Sviluppo e testing
- Backup e disaster recovery

---

## Cloud Privato

L'infrastruttura cloud è dedicata esclusivamente a una singola organizzazione. Può essere ospitata nel data center aziendale o da un provider esterno, ma le risorse non sono condivise.

**Tecnologie comuni:** VMware, OpenStack, Microsoft Azure Stack

**Caratteristiche:**
- Controllo totale su dati e configurazioni
- Maggiore sicurezza e isolamento
- Personalizzazione completa
- Costi fissi più elevati

**Ideale per:**
- Banche, ospedali, pubblica amministrazione
- Settori con requisiti normativi stringenti (GDPR, PCI-DSS)
- Aziende con dati molto sensibili
- Chi ha già investito in hardware e vuole virtualizzare

---

## Cloud Ibrido

Combinazione di cloud pubblico e privato, con dati e applicazioni che possono spostarsi tra i due ambienti in base alle necessità.

```
                    Cloud Ibrido
                         │
          ┌──────────────┴──────────────┐
          │                             │
   Cloud Privato                 Cloud Pubblico
   (Data center aziendale)       (AWS / Azure / GCP)
          │                             │
   Dati sensibili              Workload variabili
   App legacy                  Backup / DR
   Compliance                  Scale-out
```

**Caratteristiche:**
- Flessibilità massima
- I dati sensibili restano in locale
- I picchi di carico vengono gestiti dal cloud pubblico
- Complessità di gestione più alta

**Ideale per:**
- Aziende in transizione verso il cloud
- Chi ha investimenti esistenti in hardware
- Settori regolamentati che devono mantenere alcuni dati on-premise

---

## Multi-Cloud

Utilizzo di servizi da **più provider cloud pubblici** contemporaneamente — ad esempio AWS per il computing e Azure per l'identità e Microsoft 365.

**Perché usarlo:**
- Evitare il vendor lock-in (dipendenza da un solo provider)
- Usare il servizio migliore di ogni provider
- Ridondanza e continuità in caso di down di un provider

**Complessità:** Alta — richiede competenze su più piattaforme e strumenti di orchestrazione.

---

## Confronto finale

| Tipo | Controllo | Costo | Scalabilità | Complessità |
|---|---|---|---|---|
| **Pubblico** | Basso | Pay-as-you-go | Alta | Bassa |
| **Privato** | Alto | Fisso/elevato | Limitata | Media |
| **Ibrido** | Medio-alto | Misto | Alta | Alta |
| **Multi-cloud** | Medio | Variabile | Molto alta | Molto alta |

---

> Per chi inizia: il **cloud pubblico** è il punto di partenza ideale. Costa poco per sperimentare, non richiede hardware e ti dà accesso agli stessi strumenti usati dalle grandi aziende.
