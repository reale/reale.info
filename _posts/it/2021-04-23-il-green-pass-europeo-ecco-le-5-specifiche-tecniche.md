---
title: "Il green pass europeo, ecco le 5 specifiche tecniche"
description: "Ecco le specifiche tecniche del Digital Green Pass, il passaporto sanitario per gli spostamenti tra Paesi Ue. Ma non bastano le tecnicalità per gestire il pass europeo in tutti gli Stati membri."
lang: it
ref: il-green-pass-europeo-ecco-le-5-specifiche-tecniche
categories: [publications, articles]
tags: []
featured_image: /assets/images/2021-04-23-il-green-pass-europeo-ecco-le-5-specifiche-tecniche.jpg
publication: Key4biz
canonical: https://www.key4biz.it/il-green-pass-europeo-ecco-le-5-specifiche-tecniche/357164/
archive: http://web.archive.org/web/*/https://www.key4biz.it/il-green-pass-europeo-ecco-le-5-specifiche-tecniche/357164/
---

La Commissione Europea [ha reso pubbliche](https://ec.europa.eu/health/ehealth/covid-19_en) le specifiche tecniche del Digital Green [Pass](https://www.key4biz.it/breton-spera-nel-green-pass-dal-15-giugno-cosa-prevede-esattamente-il-regolamento-ue-per-viaggiare-test-per-i-bimbi/352726/), il "passaporto sanitario" su cui la stessa Commissione e gli Stati Membri avevano raggiunto un [accordo](https://ec.europa.eu/commission/presscorner/detail/en/ip_21_1181) lo scorso 17 marzo sul piano dei principi fondamentali (non-discriminazione, tutela della privacy, interoperabilità). Le specifiche sono accompagnate da un'implementazione di riferimento di tutti i componenti della piattaforma digitale, già disponibile come software open source su [GitHub](https://github.com/eu-digital-green-certificates).

Le 3 condizioni per mostrare la "prova digitale"
------------------------------------------------

Va anzitutto ricordato che per Digital Green Pass intendiamo una "prova digitale" riferita a tre diverse condizioni:

1.  essersi vaccinati
2.  essere guariti dal virus
3.  aver eseguito un tampone con esito negativo.

Green pass europeo, le 5 specifiche tecniche
--------------------------------------------

La complessità inerente alla gestione di tre condizioni caratterizzate da dinamiche e tempistiche così diverse tra loro ha richiesto naturalmente uno sforzo di design aperto e flessibile, che dal punto di vista della governance tecnologica e dell'architettura informativa si traduce in alcuni elementi fondamentali:

1.  un livello di [interoperabilità semantica](https://ec.europa.eu/health/sites/health/files/ehealth/docs/vaccination-proof_interoperability-guidelines_en.pdf) garantito dall'adozione di [SNOMED CT](https://www.snomed.org/snomed-ct/five-step-briefing), il gold standard per la rappresentazione formale e machine-readable, della terminologia medica, e che consentirà anche eventuali future estensioni rese necessarie da varianti del virus
2.  un [trust framework](https://ec.europa.eu/health/sites/health/files/ehealth/docs/trust-framework_interoperability_certificates_en.pdf) al quale tutti i soggetti partecipanti si conformeranno per garantire lo scambio di credenziali necessarie per verificare i certificati, a sua volta basato su tre elementi: holder (il titolare del Pass), issuer (l'autorità sanitaria che lo rilascia) e verifier (l'autorità o il soggetto che verifica il Pass, ad esempio in aeroporto o in hotel)
3.  un [gateway centrale](https://ec.europa.eu/health/sites/health/files/ehealth/docs/digital-green-certificates_v2_en.pdf), gestito dalla Commissione Europea, al quale potranno "agganciarsi" i sistemi di backend degli Stati Membri
4.  la distribuzione delle chiavi crittografiche in ciascun Stato membro potrà avvenire secondo tecnologie definite autonomamente dallo stesso Paese.
5.  le autorità sanitarie nazionali/regionali (gli issuer) dovranno superare un processo di onboarding per accreditarsi presso il gateway

Non bastano le specifiche tecniche per gestire il pass europeo
--------------------------------------------------------------

Le questioni di governance e architetturali sembrano dunque definite per intero dalle specifiche EU. Resta però l'urgenza di chiarire, stante che ovviamente la gestione del Digital Green Pass non si esaurisce certo sul piano tecnologico, quali misure gli Stati membri decideranno di mettere in atto per evitare che lo strumento digitale si trasformi in una fonte di discriminazioni (come [accaduto ad esempio in Israele](https://www.editorialedomani.it/politica/mondo/come-la-nuova-vita-normale-di-israele-campione-di-vaccini-gtu13dmm)) o peggio in una nuova débâcle.

Implementazione open source
---------------------------

La disponibilità delle nuove specifiche tecniche EU interseca la vicenda del Green Pass italiano, su cui [stanno emergendo nuovi elementi](https://www.key4biz.it/il-green-pass-funzionera-cosi-qr-code-sui-certificati-da-inviare-ai-cittadini-via-email-con-immuni-e-app-io/357124/). La piattaforma italiana sarà sviluppata e gestita da **Sogei**, che dovrà naturalmente impegnarsi alla realizzazione di un'architettura compatibile con le specifiche EU. In questo senso, la disponibilità dell'implementazione open source di riferimento pubblicata dalla Commissione Europea può rappresentare un ottimo punto di partenza per fare economia di scala tra gli Stati Membri ed evitare tortuosità, dispersioni di energie e la necessità di affidarsi alle piattaforme commerciali come già accaduto per il contact tracing.
