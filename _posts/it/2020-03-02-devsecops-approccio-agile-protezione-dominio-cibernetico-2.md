---
title: "DevSecOps: l’approccio agile alla protezione del dominio cibernetico – Parte 2"
lang: it
ref: ofcs-devsecops-2
categories: [publications, articles]
tags: []
featured_image: /assets/images/2020-03-02-devsecops-approccio-agile-protezione-dominio-cibernetico-2.jpg
coauthors: [ "D. Maniscalco" ]
publication: OFCS.Report
canonical: https://ofcs.report/cyber/devsecops-dalla-cybersecurity-al-dominio-cibernetico-2/
archive: http://web.archive.org/web/*/https://ofcs.report/cyber/devsecops-dalla-cybersecurity-al-dominio-cibernetico-2/
---

Security come codice. Il paradigma tradizionale considera ortogonali software e infrastruttura, intendendo quest’ultima come ambiente di supporto all’esecuzione del software stesso. Tuttavia, la convergenza di diversi processi di evoluzione tecnologica, di metodologica e operativa e di management ha eroso nel corso degli ultimi anni il confine tra i due mondi. Sul piano tecnologico, ad esempio, l’avvento del cloud, di tecniche di virtualizzazione e containerizzazione, di software-defined networking e software-defined storage ha consentito di svincolare le decisioni architetturali dal piano puramente fisico; sul piano delle metodologie, l’Agile nelle sue tante declinazioni e l’evoluzione nella gestione di servizi e operations (si pensi a come è cambiato nel tempo ad esempio il modello ITIL) ha introdotto l’approccio iterativo e il feedback “circolare” tra produzione, implementazione, progettazione. Sul piano del management, l’esigenza di rispondere con efficienza e tempismo alle sollecitazioni esterne ed interne e l’avvento di modelli organizzativi più snelli ha favorito la rottura dei silos tradizionali.

Il tema di fondo del nuovo paradigma è la circolazione più ampia e più diffusa delle informazioni tra chi progetta un asset digitale, chi ne cura la continuità operativa e chi lo inserisce all’interno di un modello di business: in tal modo, viene innestato nel ciclo di vita di un asset un flusso continuo di evoluzione, integrazione e validazione che è a sua volta iterativo, replicabile, automatizzabile e verificabile.

In questo quadro, il “layer” cybersecurity si inserisce in modo naturale.

Nel 2012, Gartner introduce il paradigma DevSecOps (in origine “DevOpsSec”) nel report [_DevOpsSec: Creating the Agile Triangle_](https://www.gartner.com/en/documents/1896617/devopssec-creating-the-agile-triangle), ravvisando la necessità per i professionisti di information security di essere attivamente coinvolti nelle iniziative DevOps e di rimanere fedeli allo spirito di DevOps, facendone propri la filosofia e gli strumenti, e nello stesso stesso tempo per la comunità DevOps di introdurre nei propri flussi informativi e organizzativi la preoccupazione per la sicurezza.

DevSecOps non è altro che un modo per incorporare fin dal principio, nella progettazione, implementazione ed operazione degli asset digitali, tre idee di fondo:

* iteratività
* responsabilità condivisa
* integrazione e trasversalità dei processi.

Un successivo [rapporto Gartner](https://cdn2.hubspot.net/hubfs/1958393/White_Papers/devsecops_how_to_seamlessly__315283.pdf) del 2016 raccomandava tra le altre cose agli architetti dell’information security di:

* abbracciare un modello di sicurezza incentrato sulle persone, consentendo agli sviluppatori di assumere una responsabilità personale (circolarità delle informazioni)
* richiedere alle piattaforme di information security di esporre tutte le funzionalità tramite API in vista di un’opportuna automatizzazione
* utilizzare pratiche e strumenti comprovati per il controllo delle versioni per tutto il software applicativo e, altrettanto importante, per tutti gli script, i modelli e i progetti utilizzati negli ambienti DevOps
* adottare un modello a “infrastruttura immutabile” in cui i sistemi di produzione sono bloccati e modificati esclusivamente tramite lo sviluppo.

È essenziale da questo punto di vista osservare che la cybersecurity non va intesa come un insieme di pratiche di basso livello, ma, come scrive Rebecca Cutrona in un [articolo](https://www.difesa.it/InformazioniDellaDifesa/periodico/Periodico_2019/Documents/Numero3/ID_03_2019_cybersecurity.pdf) apparso in *Informazioni Difesa*, come un insieme di teoria e prassi la cui “chiave principale è quella di una ricerca continua sui nuovi pericoli e sui diversi livelli di attori coinvolti in sinergia con una serie di investimenti orientati non solo verso tecnologie cost-effective, ma anche sicure”.
