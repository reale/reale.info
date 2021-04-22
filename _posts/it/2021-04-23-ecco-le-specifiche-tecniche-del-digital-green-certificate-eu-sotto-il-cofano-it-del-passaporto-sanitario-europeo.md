---
title: Ecco le specifiche tecniche del Digital Green Certificate EU: sotto il cofano IT del "passaporto sanitario" europeo 
description: "Le specifiche uscite a fine aprile, constano di diverse parti, sono state elaborate nell’ambito dell’iniziativa eHealth, la rete istituita dalla Direttiva 2011/24/EU. Ecco tutti i dettagli."
lang: it
ref: ecco-le-specifiche-tecniche-del-digital-green-certificate-eu-sotto-il-cofano-it-del-passaporto-sanitario-europeo
categories: [publications, articles]
tags: []
featured_image: /assets/images/2021-04-23-ecco-le-specifiche-tecniche-del-digital-green-certificate-eu-sotto-il-cofano-it-del-passaporto-sanitario-europeo.jpg
publication: Agenda Digitale
canonical: https://www.agendadigitale.eu/sanita/ecco-le-specifiche-tecniche-del-digital-green-certificate-eu-sotto-il-cofano-it-del-passaporto-sanitario-europeo/
archive: http://web.archive.org/web/*/https://www.agendadigitale.eu/sanita/ecco-le-specifiche-tecniche-del-digital-green-certificate-eu-sotto-il-cofano-it-del-passaporto-sanitario-europeo/
---

Sono disponibili da poche ore le [specifiche tecniche](https://ec.europa.eu/health/ehealth/covid-19_en) del [Digital Green Certificate EU,](https://www.agendadigitale.eu/sicurezza/privacy/digital-green-certificate-attenti-ai-nostri-diritti-ecco-i-punti-sensibili/) il "passaporto sanitario" che dovrebbe consentire la ripresa degli spostamenti all'interno dell'Unione Europea.

Le specifiche, che constano di diverse parti, sono state elaborate nell'ambito dell'iniziativa eHealth, la rete istituita dalla Direttiva 2011/24/EU, a cui aderiscono su base volontaria i soggetti pubblici degli Stati Membri che si occupano di sanità digitale.

L'architettura digitale del DGC
-------------------------------

L'architettura del DGC poggia su tre elementi informativi fondamentali:

1.  un dataset minimo contenente le informazioni essenziali ai fini del certificato
2.  un identificativo globalmente univoco
3.  un trust framework (descritto più avanti)

Dal punto di vista del processo, l'iter del certificato (user story) prevede a sua volta tre fasi distinte:

1.  la raccolta e la registrazione in un sistema informativo sanitario dei dati sugli eventi sanitari di interesse da parte di soggetti autorizzati
2.  il rilascio del certificato
3.  la presentazione del certificato a un verificatore (es. guardia di frontiera o operatore sanitario) per la sua verifica

La complessità inerente alla gestione di tre condizioni caratterizzate da dinamiche diverse (vaccinazione, convalescenza, tampone) ha richiesto uno sforzo ulteriore in termini di design aperto e modulare, in grado non soltanto di garantire il rispetto dei requisiti "di business" ma anche la possibilità di future estensioni.

Le specifiche a loro volta constano di diversi documenti, articolati come segue

1.  meccanismi per il riconoscimento reciproco e l'interoperabilità dei certificati di vaccinazione, test e convalescenza ([formati e trust management](https://ec.europa.eu/health/sites/health/files/ehealth/docs/digital-green-certificates_v1_en.pdf), [gateway](https://ec.europa.eu/health/sites/health/files/ehealth/docs/digital-green-certificates_v2_en.pdf), [codici QR](https://ec.europa.eu/health/sites/health/files/ehealth/docs/digital-green-certificates_v3_en.pdf), [applicazioni](https://ec.europa.eu/health/sites/health/files/ehealth/docs/digital-green-certificates_v4_en.pdf))
2.  [tracciati record e schema JSON](https://ec.europa.eu/health/sites/health/files/ehealth/docs/digital-green-certificates_dt-specifications_en.pdf)
3.  implementazione di riferimento, disponibile su [GitHub](https://github.com/eu-digital-green-certificates).

Interoperabilità semantica
--------------------------

Il livello di interoperabilità semantica è cruciale per garantire che i dati sanitari trattati dal DGC siano rappresentati in maniera uniforme e machine-readable in tutti gli Stati Membri. Inoltre, un'adeguata progettazione a questo livello permette di prevedere future estensioni (che potrebbero essere necessarie, ad esempio, per gestire eventuali varianti del virus).

Le specifiche referenziano esplicitamente [SNOMED CT](https://www.snomed.org/snomed-ct/five-step-briefing), standard de facto nell'ambito della rappresentazione formale della terminologia medica.

Trust framework
---------------

Il trust framework rappresenta la chiave di volta delle specifiche, sia dal punto di vista tecnico che da quello della governance, perché è l'elemento che abilita il mutuo riconoscimento delle credenziali crittografiche tra *issuer* (l'autorità sanitaria che emette il certificato), *verifier* (il soggetto che lo verifica) e *holder* (l'interessato). La Commissione Europea ha palesemente dedicato un'attenzione particolare al framework, dettagliando i seguenti principi chiave su cui esso si fonda:

-   Interoperabilità crossborder: le implementazioni nazionali, entro i confini dell'Unione Europea, di certificati conformi alle specifiche del framework devono essere interoperabili (ovviamente, altrimenti si vanificherebbe il senso stesso della costruzione di un'architettura comune). Di più, le implementazioni nazionali non dovrebbero impedire l'interoperabilità con gli schemi internazionali in corso di sviluppo dall'OMS e da ICAO.
-   Privacy by design e by default: il trust framework è progettato per proteggere i dati dei soggetti coinvolti e in primis dell'interessato, attraverso il rispetto dei principi sanciti dal GDPR (minimizzazione e limitazione delle finalità del trattamento).
-   Sicurezza by design e by default: in particolare, il framework prevede mezzi atti ad impedire il cross-referencing dei dati trattati, pur specificando che ulteriori misure di prevenzione potranno essere discusse e incorporate nel framework nel corso di iterazioni successive dello stesso.
-   Semplicità d'uso e inclusività: in particolare, al fine di non discriminare utenti che non dispongano di device o competenze digitali, il framework prevede l'utilizzo di un ampio spettro di media, incluso il cartaceo (il codice QR può essere generato ed esibito su carta).
-   Flessibilità di implementazione: il framework è agnostico rispetto alla scelta della tecnologia, che è lasciata agli Stati Membri (ad esempio, non esclusa la possibilità di usare tecnologie a registri distribuiti o blockchain), purché ovviamente siano rispettati livelli di servizio comuni. Per quanto riguarda l'Italia, questo punto consentirà l'estensione al framework EU del passaporto sanitario nazionale il cui sviluppo, secondo quanto risulta, è affidato a Sogei.
-   Modularità e scalabilità: l'importanza di un'architettura scalabile, in grado di adattarsi a picchi di carico improvvisi senza che il livello di servizio ne sia danneggiato, è evidente. La modularità, dal canto suo, assicura che il framework sia predisposto per scenari e casi d'uso più ampi di quelli strettamente sanitari. Quest'ultimo è un punto critico, perché le specifiche prevedono esplicitamente un'estensione ad attività di tipo ricreativo, pur riconoscendo che le decisioni sul piano etico-politico in merito a tali estensioni esulano dagli scopi di una documentazione tecnica.
-   Standard e formati aperti: il trust framework è basato su standard aperti (nella misura in cui ciò è possibile) non soltanto per questioni di interoperabilità ma anche perché questo aspetto, in sinergia con un modello di governance aperta e con la disponibilità di un'implementazione open source, è considerato cruciale per costruire un rapporto di fiducia con gli utenti.

Gateway
-------

L'architettura prevede un gateway centrale, al quale i sistemi di backend degli Stati Membri, o meglio dei rispettivi servizi sanitari, potranno "agganciarsi" attraverso un meccanismo di sottoscrizione a web service. Ciascun sistema nazionale deve superare un processo di onboarding, simile a quello adottato da framework paneuropei come [PEPPOL](http://peppol.eu/), con relativo scambio di certificati (i certificati delle autorità sanitarie nazionali vengono inclusi in un'apposita white list, la DGCG Trust List), e dovrà prevedere a sua volta dei servizi (REST) di revoca e di callback.

Val la pena osservare che l'implementazione di riferimento [si ispira esplicitamente](https://github.com/eu-digital-green-certificates/dgc-gateway/commit/54bd521a3090b58439b66ec7d2cb07ac251513d8) allo [EFGS](https://github.com/eu-federation-gateway-service/efgs-federation-gateway), o EU Federation Gateway Service, che era stato sviluppato nel 2020 per permettere l'interoperabilità tra i sistemi di contact tracing degli Stati Membri. Nonostante preveda l'esistenza di un gateway centrale, dalla cui presenza dipende il funzionamento di tutto l'insieme, però, l'architettura proposta dalla Commissione Europea mantiene un certo grado di decentralizzazione in quanto i certificati sono gestiti direttamente dalle autorità sanitarie degli Stati Membri. In questo senso, il gateway rappresenta un soggetto certificatore di ultima istanza, una Certification Authority nel senso tradizionale in crittografia. Nulla impedisce agli Stati Membri di adottare, al loro interno, architetture più decentralizzate, purché sia assicurato il colloquio con il gateway.

L'implementazione di riferimento
--------------------------------

Come accennato, le specifiche tecniche sono accompagnate da un'implementazione di riferimento, disponibile con licenza open source su GitHub. Nel momento in cui scriviamo, tale implementazione consta di ben 15 componenti, distribuiti come segue:

1.  DGC gateway
2.  Emissione (issuance) di un DGC: servizio di backend e web app
3.  Verifica di un DGC: servizio di backend, web app, mobile app (iOS e Android)
4.  Wallet digitale (iOS e Android)
5.  Moduli core (iOS e Android)
6.  Librerie e classi Java comuni
7.  Validatore Swift del JSON Schema
8.  Codici QR di test
9.  Informazioni e documentazione per l'onboarding delle autorità sanitarie (repository ad oggi vuoto)

Il codice, ad una prima analisi, risulta tuttora in fase di sviluppo (i 15 repository non hanno tutti lo stesso grado di maturità) ma è già parzialmente utilizzabile, e in ogni caso può rappresentare un buon punto di partenza per gli Stati Membri che vorranno dotarsi della propria implementazione nazionale. La gestione del gateway, invece, di cui il codice sorgente è comunque disponibile, resta esclusivamente in capo alla Commissione Europea.

Conclusioni
-----------

Le specifiche delineano la governance e dirimono le questioni tecniche di un istituto, quello del passaporto sanitario, che naturalmente non si esaurisce sul piano dell'innovazione e della trasformazione digitale, ma investe soprattutto il piano dei diritti e del rapporto tra soggetto pubblico e cittadino. Non rientra negli scopi di questo articolo affrontare la questione da questo punto di vista più ampio, ma è comunque opportuno ribadire due punto: primo, che il soluzionismo tecnologico non può aprire le porte a discriminazioni ulteriori nell'accesso a spazi e servizi pubblici, discriminazioni che sarebbero poi anche conseguenza della gestione della campagna vaccinale; secondo, che è cruciale non ripetere gli errori fatti con il contact tracing, sia in termini di comunicazione con i cittadini che di governance del sistema sanitario.

«Un'iniziativa così ambiziosa necessiterà di una regia coordinata anche per quel che riguarda le iniziative di comunicazione che dovranno mettere in luce con la massima chiarezza tutti i vantaggi legati all'adozione di questo sistema in termini di sicurezza e privacy», commenta Flavia Gamberale, giornalista ed esperta di comunicazione dei servizi digitali.
