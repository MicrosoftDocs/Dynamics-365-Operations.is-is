---
title: "Yfirlit yfir afstemming bankayfirlits og greiðsla banka fyrir ESB"
description: "Þetta efnisatriði gefur yfirlit yfir aðgerðir sem hægt er að nota til að stemma af greiðsluupplýsingar úr banka í snið sem notuð eru með Evrópskra landa."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267994
ms.assetid: 2bfb8ecc-e850-43cb-9a96-deb11716a391
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 22d93d7b3618d4f5931c6a7e39d681173734b0b9
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Yfirlit yfir afstemming bankayfirlits og greiðsla banka fyrir ESB

Þetta efnisatriði gefur yfirlit yfir aðgerðir sem hægt er að nota til að stemma af greiðsluupplýsingar úr banka í snið sem notuð eru með Evrópskra landa.

Í Microsoft Dynamics 365 fyrir Aðgerðir, hægt að flytja inn færslur af bönkum og jafna þessar færslur á móti fyrirliggjandi færslur. Í Evrópu er hægt að gera það fyrir eftirfarandi aðstæður:

-   Flytja inn bankayfirlit
-   Flytja inn greiðslur.
-   Flytja inn skrár vegna skila.

## <a name="bank-statements"></a>Bankayfirlit
A *bankayfirlit* eða *lykill uppgjör* er yfirlit yfir fjárhagslegar færslur sem hafa orðið yfir tiltekið tímabil á bankareikning geymdur af fyrirtæki með í fjármálastofnun. Í Dynamics 365 aðgerða hægt er að flytja inn bankayfirlit. Mikilvægt er að jafna innfluttar færslur við fyrirliggjandi færslur sem staðfesta opnunarfærslur- og lokadagsetningu stöðu bankareikninga. Eftirfarandi listi inniheldur studd Evrópska snið.

-   Ítarleg afstemming Evrópska skrársnið. Nánari upplýsingar, sjá [Ítarlegt yfirlit yfir afstemming banka](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 skilaboð skrá sniði bankayfirlits
-   CODA skrá sniði bankayfirlits. Nánari upplýsingar, sjá [coda-bankayfirlit](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Flytja inn- og skila skilaboð greiðslur viðskiptavinar og lánardrottins
Auk bankayfirliti, bönkum veita ákveðnum skilaboð sem innihalda upplýsingar um greiðslur viðskiptavina og lánardrottna, sem geta flutt inn í Dynamics 365 aðgerða og afstemmd með færslur viðskiptavina og lánardrottna. Þegar fyrirtæki þarf að fá upplýsingar um innleið viðskiptavinafærslur greiðslur frá bankanum, hægt að nota sniðin innflutning. Fyrir fyrirtæki sem nota beina debet og kredit flutning fyrir svör er hægt að taka til að uppfæra stöðu greiðslna sem áður voru fluttar út. Mismunur innflutningssniði og skila snið er sem skilar eru ætlaðar eru til að uppfæra þegar stofnað færslubókarlínur lánardrottinsgreiðslu (geta stofnað þegar beina debet eða kredit flutning var hafin) í stað þess að stofna nýjar línur. Sumar flókið innflutningssniði getur einnig innihaldið skilaaðstæðum. Eftirfarandi dæmi sýnir hvernig á að innleiða þessa skiptingu.

##### <a name="import-formats"></a>Innflutningssnið

-   Tilkynning ISO 20022 camt.054 banka
-   [Innflutningssnið nets](emea-nor-nets-import-format.md) -Flóknar eiginleiki fyrir Norsk greiðslusnið
-   Flytja ESR greiðslur viðskiptavina
-   Flytja inn greiðslusnið fyrir Svíþjóð - BankGirot Max og BankGirot OCR-snið

##### <a name="return-formats"></a>Skila snið

-   ISO skýrslu um stöðu 20022 pain.002
-   (DNK) BetalingsserviceBasis-returformat – skilasniðinu útflutningssniðið Betalingsservice viðskiptavinar
-   [Flytja inn greiðslusnið fyrir Svíþjóð](emea-swe-payment-formats-import.md) -Bankgirot Autogiro skilar
-   (SWE) BankGirot skila-sniði sem samsvarar útflutningssniði Bankgirot lánardrottnagreiðslur skila

