---
title: "Information security per i servizi web della PA"
lang: it
ref: information-security-per-i-servizi-web-della-pa
categories: [publications, articles]
tags: []
featured_image: /assets/images/2020-04-14-information-security-per-i-servizi-web-della-pa.jpg
publication: OFCS.Report
canonical: https://ofcs.report/cyber/information-security-per-i-servizi-web-della-pa/
archive: http://web.archive.org/web/*/https://ofcs.report/cyber/information-security-per-i-servizi-web-della-pa/
---

La cura della sicurezza informatica è un **processo olistico** che attraversa
tutte le fasi di un progetto ICT, coinvolgendo figure professionali ad ampio
spettro.

### Premessa

La partita, oggi, si gioca su campi impensabili sino a qualche anno fa, e
richiede la messa in opera di contromisure e **tecniche di prevenzione ad ampio
spettro**. Né potrebbe essere altrimenti in un mondo in cui gli strumenti a
disposizione di eventuali attacchi si fanno sempre più potenti e i fini sempre
più politicizzati.

Alla necessità di contrastare attacchi brute force si è aggiunta inoltre
l’esigenza di difendersi tanto da accessi non autorizzati ai dati sensibili
(**data leaking**) quanto da pratiche di vandalismo (**defacement**) con forte
impatto mediatico.

L’opera di prevenzione, se intende essere adeguata, deve iniziare nel momento
stesso in cui il software nasce; la sensibilità al problema della sicurezza, in
altri termini, deve informare tutte le fasi di analisi, progetto,
implementazione e verifica del software stesso, con un grado di attenzione non
inferiore a quello che si richiede durante la conduzione in esercizio.

Durante tutte le fasi del progetto è essenziale stabilire una **gerarchia della
sensibilità dei dati e dei sistemi**, cui far corrispondere una differenziazione
dei livelli e dei requisiti minimi di sicurezza da applicare.

L’esigenza di difendersi da vulnerabilità o codice malevolo conduce naturalmente
a prediligere procedure, formati, librerie e componenti software aperti, come
richiesto d’altra parte dal **Codice dell’Amministrazione Digitale**.

Scopo del presente documento sarà dunque la descrizione dei metodi, standard e
best practice da adottare per la messa in sicurezza di un sistema informatico,
con particolare attenzione ai **portali web informativi o di servizi**.

### Progettazione

La fase progettuale dovrà riposare sui seguenti principi-cardine:

-   articolazione dell’architettura in **moduli indipendenti**;

-   scelta di una piattaforma aperta e di protocolli aperti ([art. 68](https://docs.italia.it/italia/piano-triennale-ict/codice-amministrazione-digitale-docs/it/v2018-09-28/_rst/capo6_art68.html) del **Codice dell’Amministrazione Digitale**);

-   rigetto del paradigma intrinsecamente insicuro della “security through
    obscurity”;

-   adozione di un **modello di sicurezza verificabile** e minimizzazione della
    superficie di attacco;

-   **gestione gerarchica e capillare** dei privilegi associati ai processi
    coinvolti; in particolare, l’applicazione del principio di least privilege;

-   isolamento dei dati, ossia separazione rigorosa e irrevocabile tra logica
    applicativa (il codice) e conservazione, accesso e verifica degli archivi
    informatizzati;

-   nel caso particolare di applicazioni web, l’adozione di principi dettati
    dall’Open Web Application Security Project (OWASP).

### Sviluppo

Lo sviluppo dovrà tener conto di buone prassi volte a prevenire precocemente i
rischi legati alla sicurezza. Tra queste citiamo:

-   Protezione da **SQL injection**. La classe di attacchi che va sotto il nome
    di SQL injection è in grado di sfruttare vulnerabilità introdotte da cattive
    abitudini di sviluppo per guadagnare accesso ai dati o per comprometterne la
    corretta archiviazione. Ci si salvaguarda da attacchi di questo tipo
    ricorrendo, tra l’altro, a librerie specializzate (object-relational
    mappers) che si facciano carico di tutte le procedure di accesso, rendendo
    impossibile l’inserzione malevola di codice proveniente dall’esterno.

-   Protezione da **code injection**. Codice maligno che riuscisse a penetrare
    nel sistema potrebbe facilmente condurre ad aggirare i criteri di protezione
    dei dati: è perciò vitale mettere in atto tecniche adeguate di protezione.
    Contromisure efficaci sono: l’uso di un’interfaccia di programmazione
    consolidata; una struttura rigorosamente modulare del codice, realizzata
    tramite raggruppamento delle funzionalità in components indipendenti e tra
    di loro e dal nucleo interno del software; una corretta codifica
    dell’output, volta in particolare a prevenire una classe specializzata di
    attacchi (HTML injection/XSS).

-   Protezione da **buffer overrun**. Il buffer overrun viene scatenato da dati
    di input malevoli atti ad alterare le modalità naturali di esecuzione del
    software. Le conseguenze di un attacco di questo sito includono accessi non
    autorizzati ad aree di memoria od archiviazione nonché la compromissione
    generale della sicurezza, suscettibile di favorire intrusioni maggiormente
    invasive. Ci si tutela dai buffer overrun operando un controllo incrociato
    in due aree critiche: validazione dell’input e verifica a runtime dei tipi
    di dati.

### Collaudo

Il ciclo di collaudo dev’essere condotto in base ad un programma rigoroso e deve
far uso di una infrastruttura **quality of service** (copia esatta
dell’infrastruttura di esercizio) con simulazione degli attacchi tramite
strumenti specializzati. La gestione del progetto prevede inoltre una
formalizzazione del flusso di informazioni critiche relative alla sicurezza tra
sviluppatori, collaudatori e sistemisti.

### Collaudo security-oriented

Si tratta di un supplemento alla fase di collaudo vera e propria, che andrà ad
individuare e catalogare eventuali debolezze residuali. Si seguiranno alcune
linee guida:

-   individuazione dei punti con maggiore vulnerabilità nonché dei dati
    sensibili;

-   tracciamento del profilo di un possibile attaccante;

-   individuazione di tutte le possibili direzioni d’attacco;

-   catalogazione delle vulnerabilità individuate;

-   adozione di **certificazioni specifiche** (la già citata OWASP, OSSTMM,
    etc.).

### Esercizio

La conduzione in esercizio di un progetto ICT è probabilmente la fase più
delicata e complessa; ed è quella in cui l’**esposizione al grande pubblico**
rende maggiormente critici eventuali difetti nella tutela della sicurezza.
Intanto, si individuano i seguenti requisiti:

-   **continuità del servizio**, alta disponibilità, resilienza;

-   resistenza ai guasti hardware e software (fault tolerance) e predisposizione
    ad un accesso intenso con potenziali picchi;

-   interconnessione ben definita con altre piattaforme;

-   controllo dei livelli di accesso ai dati;

-   difesa efficace da attacchi di tipo **denial-of-service** e **defacement**
    (danno d’immagine);

-   semplicità di gestione.

Il rispetto di tali requisiti passa attraverso alcuni punti essenziali:

-   stesura di **procedure** che coprano tutti gli aspetti operativi, alla
    normale manutenzione alle condizioni di emergenza e al disaster recovery, e
    di protocolli che assicurino la continuità operativa;

-   gestione che faccia sue le **direttive stabilite in sede di progetto**
    nonché durante i successivi momenti di messa a punto e di aggiornamento;

-   una condivisione libera e piena della conoscenza all’interno del gruppo
    sistemi, dell’intero progetto e dell’Amministrazione.

Ne scaturisce la visione di un’architettura che:

-   garantisca la piena integrità e validazione dell’interscambio dati
    appoggiandosi a **protocolli sicuri**;

-   faccia uso di ACL (Access Control List) per definire i **permessi** sulla
    creazione, modifica e visualizzazione dei contenuti;

-   preveda **aggiornamenti** continui, garantiti eventualmente dal supporto a
    lungo termine (TLS);

-   adotti strumenti ad alta protezione attestati sui **segmenti più esposti**
    (firewall, strumenti per la prevenzione e la rivelazione di intrusioni nella
    rete, port scanning, geolocalizzazione degli accessi);

-   faccia sue buone prassi di affinamento progressivo delle configurazioni
    (**hardening**).

Parte essenziale della conduzione in esercizio di un progetto IT sarà la scelta
ed il deploying di uno **strumento di monitoraggio**, il quale assista lo staff
sistemistico nella pronta percezione dei problemi, nella diagnosi e ricerca
dell’eziologia e, nella misura del possibile, anche in un intervento attivo.

Ad un apparato del genere si chiederà, in altre parole, di dotarsi di una
“intelligenza” che gli consenta di incrementare la proattività del sistemista,
ossia la capacità di prevenire ed anticipare i problemi e, più in generale, i
bisogni futuri.

Individuiamo i seguenti requisiti come preferenziali:

-   possibilità di attingere ad un vasto patrimonio di moduli aggiuntivi
    (plugin);

-   strumenti di amministrazione che consentano uno **sguardo olistico** sullo
    stato dell’intera infrastruttura;

-   strumenti per la verifica dell’integrità delle componenti del sistema
    (eventuale manomissione di file di configurazione, alterazione di privilegi
    d’accesso, caricamento di documenti non autorizzati);

-   supporto per il monitoraggio di apparati di rete;

-   capacità di operare in una **configurazione distribuita**.

Il sistema di monitoraggio dovrà proteggere l’infrastruttura critica del
progetto (**IT core infrastructure**) da attacchi di tipo invasivo che possano
compromettere, a vari livelli, la **sicurezza** del sistema, la sua **capacità
operativa**, il **valore in termini di immagine** del servizio erogato.

In particolare, dovranno essere fronteggiati in modo il più possibile
automatizzato attacchi delle tipologie seguenti:

-   **Web site defacement**: consiste nel minare la reputazione di una
    organizzazione modificando una home page ufficiale o sostituendola con
    un’altra fabbricata ad arte, con l’obiettivo di lanciare un messaggio
    denigratorio.

-   **Denial of Service**: attacco il cui scopo è quello di **rendere
    indisponibile un servizio**. Si mette in atto inondando i server di
    richieste (anche fasulle) in modo tale da saturarne la capacità operativa.

In entrambi i casi il servizio di monitoraggio dovrà essere in grado non
soltanto di notificare immediatamente il personale IT preposto, ma anche di
effettuare delle **azioni di tipo proattivo** (ad esempio, il ripristino
automatico della pagina web compromessa).

### Sicurezza globale

Per garantire una sicurezza a livello globale sarà opportuno:

-   abilitare l’accesso fisico ai locali server tramite Card Keys e
    identificazione biometrica;

-   abilitare l’audit delle attività svolte sul sistema, in modo da intercettare
    operazioni non autorizzate o sospette.

Qualsiasi anomalia riscontrata in questa fase permette un tempestivo intervento
sul sistema.
