---
title: "Immuni? Timori sulla privacy infondati ma serve un approccio rigoroso alla sicurezza"
lang: it
ref: immuni-timori-sulla-privacy-infondati-ma-serve-un-approccio-rigoroso-alla-sicurezza
categories: [publications, articles]
tags: [covid 19, italy, politics, cybersecurity, privacy]
featured_image: /assets/images/2020-06-08-immuni-timori-sulla-privacy-infondati-ma-serve-un-approccio-rigoroso-alla-sicurezza.jpg
publication: "Eventual Consistency"
canonical: https://medium.com/reale/immuni-timori-sulla-privacy-infondati-ma-serve-un-approccio-rigoroso-alla-sicurezza-e19cd2e79072
archive:
---

Ai microfoni di [*Radio Cusano Campus*](https://www.tag24.it/) [ho raccontato](https://www.tag24.it/257090-reale-eutopian-app-immuni-sicura-paure-sulla-privacy-infondate/) le mie impressioni su Immuni: app e sistema di backend (quello che colloquia con il Servizio Sanitario Nazionale) sono fatti bene sia in termini di design che di implementazione, e l'attenzione alla privacy e alla sicurezza c'è indubbiamente stata. Dall'estero del resto ci seguono con grande attenzione non solo perché siamo stati quasi i primi in Europa a deployare un servizio completo di exposure notification, nonostante le API BLE di Google e Android su cui Immuni si appoggia fossero state rilasciate solo pochi giorni prima, ma anche perché il risveglio del dibattito pubblico che Immuni ha innescato fa in un certo senso da controcanto alla compressione di diritti che abbiamo subito durante il lockdown.

Impressioni, dicevo: ma in una questione che ha investito in pieno il dibattito sulla gestione della crisi da parte del governo e in ultima analisi sulla tenuta della democrazia (ed è forse una delle primissime volte che in Italia a fare da detonatore è una piattaforma digitale: ma vi dico che succederà sempre più spesso) accontentarsi delle proprie impressioni, fondate o meno, è pericoloso.

Perciò con [Eutopian](https://eutopian.eu/) qualche giorno fa abbiamo richiesto due cose imprescindibili per un servizio pubblico digitale veramente sicuro:

1.  un [formal threat model](https://github.com/immuni-app/immuni-documentation/issues/109), cioè un modello che descrive in modo rigoroso tutti i possibili attacchi informatici a una piattaforma o un servizio digitale e quindi ne mette in luce debolezze e vulnerabilità, invitando a correggerle
2.  una [responsible disclosure policy](https://github.com/immuni-app/immuni-documentation/issues/110), ossia un protocollo sicuro per la segnalazione di vulnerabilità scoperte da esperti indipendenti ed ethical hackers

Permettetemi una digressione. È fondamentale rivolgersi direttamente agli architetti del software e agli sviluppatori, ai tecnici insomma, interagendo con loro su piattaforme come GitHub che non soltanto rappresentano lo standard de facto globale per qualsiasi progetto open source ma che si avviano a diventare le nuove agorà. L'Italia purtroppo sconta, nell'approccio alle discipline STEM e in particolare all'ingegneria del software, il vecchio pregiudizio contro le "arti meccaniche", e molta parte del lavoro interdisciplinare che andrebbe fatto per affrontare con piena cognizione di causa la transizione digitale si scontra cono la resistenza degli "umanisti" a sporcarsi le mani, a dialogare con quello sviluppatore, mezzo guru mezzo homo sanza litterae, che essi disprezzano e temono nello stesso tempo.

Alla fine dell'intervista, non ho saputo rinunciare alla mia vena provocatoria: dico, in modo forse un po' trenchant, che l'app doveva essere un obbligo. Io che credo nello Stato liberale, e che so benissimo che anche il garante europeo della privacy (l'EDPB) si era già espresso negativamente (e tassativamente) a riguardo. Ma so anche molto bene che già nel 1965 Mancur Olson dimostra che l'azione collettiva quasi mai si volge al bene comune, e so che i free rider, quei soggetti che godono dei benefici di qualcosa lasciandone però ad altri i costi, saranno talmente numerosi da rendere di fatto inefficace il progetto Immuni, per la gioia delle pizie del no-trax. Eppure se Immuni o qualsiasi altra soluzione di exposure notification, in Italia e fuori, all'interno del più ampio processo 3T (Test Treat Track), servirà a salvare anche una sola vita umana, ne sarà ampiamente valsa la pena.
