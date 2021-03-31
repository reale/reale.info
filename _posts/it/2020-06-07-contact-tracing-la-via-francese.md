---
title: "Contact tracing: la “via francese”"
lang: it
ref: contact-tracing-la-via-francese
categories: [publications, articles]
tags: [france, italy, society, politics, covid 19]
featured_image: /assets/images/2020-06-05-immunizzarsi-o-indignarsi.jpg
publication: "Eventual Consistency"
canonical: https://medium.com/reale/contact-tracing-la-via-francese-f6e947c2413b
archive:
---

Sì, ho installato Immuni. Per dovere di cronaca ho installato anche StopCovid, la sua omologa francese. E sì, le due app possono convivere sullo stesso dispositivo (funzionando correttamente entrambe) perché si basano su due approcci completamente diversi.

Immuni usa le API Bluetooth Low Energy di Apple/Google. Attenzione alle parole, perché dietro o oltre l’argot c’è tutta la disparità di forza tra Stati e big tech. I due giganti del digitale hanno fatto in fretta a stringersi la mano, decidere che i propri “stack” BLE possono parlarsi tra loro e che quella della pandemia è un’occasione molto, molto ghiotta per fare sfoggio di social responsibility e nello stesso tempo insinuarsi ancora più profondamente nella vita della gente e negli equilibri geopolitici.

Perché guardate, non è che Google e Apple abbiano un piano segreto per usare Immuni o le sue omologhe presenti e future per spiarci, geolocalizzarci o fare incetta di “big data”. Non ne hanno bisogno. Il loro peso, la loro dominanza in un mondo che senza digitale semplicemente non sopravvive (la pandemia ce l’ha dimostrato abbastanza brutalmente) sono tali da costringere i decisori politici nelle forche caudine di una scelta obbligata. Chi possiede l’infrastruttura dell’infosfera, res extensa o res cogitans che sia, possiede il mondo: e oggi l’infrastruttura è distribuita come il contact tracing, sono i device che portiamo in tasca e i sistemi operativi e le piattaforme che li animano. Tutto questo mentre il linguaggio stesso viene edulcorato: si passa dal contact tracing, troppo invasivo, al più anodino, politically-correct exposure notification. Giusto per sottolineare che sì, per chi vende device e sistemi operativi le app dovrebbero essere tutte uguali ma alcune sono più uguali delle altre.

Dal canto opposto, la Francia. StopCovid rifiuta di adeguarsi a decisioni prese oltreoceano e ripiega su ROBERT, un protocollo open sviluppato da Inria e Fraunhofer. Paga però questo gesto di ribellione con una notevole inefficienza energetica: non potendo usare il BLE in background perché inaccessibile senza le API di cui sopra, StopCovid deve restare attiva e quindi si “beve” la batteria subito. Ora, se la sostenibilità digitale (l’impatto energetico di un asset digitale) francamente non mi pare prioritaria rispetto alla possibilità di salvare vite umane, tuttavia dal punto di vista della user experience l’impatto si sente eccome.

Ma c’è un aspetto più profondo e meno aggirabile: il virus non si ferma certo alle frontiere, quindi le soluzioni scelte dagli Stati devono essere interoperabili, altrimenti siamo punto e da capo e finiamo per dare ragione a Grecia e Austria che non ci vogliono in casa loro. E qui, delle due l’una: se tutti ci facciamo bastare il solco tracciato per noi da Apple/Google, allora l’interoperabilità ce l’abbiamo (quasi) gratis perché il cuore dell’app è sempre lo stesso: però così la dipendenza, il lock-in sulle due big tech passa dalla dimensione nazionale a quella europea. Se invece vogliamo far da soli, gli Stati devono cercare un accordo tra loro: fatica enorme e alea troppo grande. Ci toccherebbe tener chiuse le frontiere fino all’estate del 2021. StopCovid, paradossalmente, non essendo ristretta dai vincoli imposti agli Stati che come l’Italia scelgono la strada API BLE, funziona anche fuori dal territorio francese.

Quindi da un lato la “scelta” (chiamiamola così) italiana, “allineata” ma pragmatica. Dall’altra lo scatto d’orgoglio d’oltralpe, non so se più coraggioso o più velleitario, perché fuori dal “paradiso” delle piattaforme non si salva nessuno.
