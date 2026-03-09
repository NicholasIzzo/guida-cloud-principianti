# 🍕 I Modelli di Servizio Cloud: IaaS, PaaS e SaaS

Quando decidi di passare al Cloud, devi scegliere quanto controllo vuoi mantenere e quanto lavoro vuoi delegare al provider (come AWS o Azure). 

Per capirlo facilmente, usiamo la famosa analogia della **Pizza**! Immagina di voler mangiare una pizza. Hai 4 opzioni:

---

### 1. On-Premises (Il Server in casa) = Fai la pizza a casa
Devi fare tutto tu: comprare gli ingredienti, impastare, avere un forno, pagare gas ed elettricità, cuocerla e poi lavare i piatti.
* **Nel mondo IT:** Compri i server fisici, li metti in una stanza (CED), paghi la corrente, l'aria condizionata, installi il sistema operativo, gestisci la sicurezza e i database. 
* *Sei responsabile del 100% delle cose.*

### 2. IaaS (Infrastructure as a Service) = Compri la pizza surgelata
Vai al supermercato e compri la pizza già fatta. Però devi comunque portarla a casa, accendere il tuo forno, usare il tuo gas e servirtela al tavolo.
* **Nel mondo IT:** Il provider ti affitta l'hardware (il server fisico, lo storage, la rete). Tu però devi installarci sopra il Sistema Operativo (Windows o Linux), aggiornarlo, installare il database e caricare la tua app.
* *Esempi:* Amazon EC2, Azure Virtual Machines.

### 3. PaaS (Platform as a Service) = Ordini la pizza a domicilio
Chiami la pizzeria e ti portano la pizza calda a casa. Tu devi solo metterci il tavolo, le sedie e le bibite.
* **Nel mondo IT:** Il provider gestisce l'hardware E ANCHE il sistema operativo. A te viene data una "piattaforma" pronta. Tu devi solo preoccuparti di scrivere il codice della tua applicazione e i tuoi dati. Zero sbattimenti su aggiornamenti di Windows o Linux.
* *Esempi:* Google App Engine, Heroku, Azure App Services.

### 4. SaaS (Software as a Service) = Vai a mangiare in Pizzeria
Ti siedi, ordini, mangi, paghi e te ne vai. Non devi fare assolutamente nulla, se non goderti l'esperienza.
* **Nel mondo IT:** È un software già pronto all'uso che usi tramite browser o app. Non vedi il server, non vedi il sistema operativo, non scrivi codice. Lo usi e basta.
* *Esempi:* Gmail, Netflix, Microsoft 365, Dropbox.

---

### 📊 Riassunto visivo di chi gestisce cosa:

| Cosa devi gestire | On-Premises | IaaS | PaaS | SaaS |
| :--- | :---: | :---: | :---: | :---: |
| **Applicazioni (Codice)** | Tu | Tu | Tu | Provider |
| **Dati** | Tu | Tu | Tu | Provider |
| **Sistema Operativo** | Tu | Tu | Provider | Provider |
| **Server (Hardware)** | Tu | Provider | Provider | Provider |
| **Rete / Storage** | Tu | Provider | Provider | Provider |

