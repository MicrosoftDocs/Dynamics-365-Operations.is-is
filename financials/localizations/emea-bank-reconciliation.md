---
title: "Yfirlit yfir bankayfirlit og greiðsluafstemmingu fyrir Evrópusambandið"
description: "Þetta efnisatriði gefur yfirlit yfir eiginleika sem þú getur notað til að stemma af greiðsluupplýsingar frá bönkum með sniðum sem eru notuð í Evrópulöndum."
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

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Yfirlit yfir bankayfirlit og greiðsluafstemmingu fyrir Evrópusambandið

[!include[banner](../includes/banner.md)]


Þetta efnisatriði gefur yfirlit yfir eiginleika sem þú getur notað til að stemma af greiðsluupplýsingar frá bönkum með sniðum sem eru notuð í Evrópulöndum.

Í Microsoft Dynamics 365 for Operations er hægt að flytja inn færslur úr bönkum og stemma þær af við fyrirliggjandi færslur. Í Evrópu er hægt að gera þetta við eftirfarandi aðstæður:

-   Flytja inn bankayfirlit
-   Flytja inn greiðslur.
-   Flytja inn skilaskrár.

## <a name="bank-statements"></a>Bankayfirlit
*Bankayfirlit* eða *reikningsyfirlit* er samantekt á fjárhagsfærslum sem átt hafa sér stað á tilteknu tímabili á bankareikningi í eigu fyrirtækis hjá fjármálastofnun. Hægt er að flytja inn bankayfirlit í Dynamics 365 for Operations. Mikilvægt er að stemma innfluttar færslur af við fyrirliggjandi færslur auk þess að staðfesta upphafs- og lokastöðu bankareikninganna. Eftirfarandi listi inniheldur studd evrópsk snið.

-   Evrópsk skráarsnið fyrir ítarlega bankaafstemmingu. Frekari upplýsingar eru í [Ítarlegt bankaafstemmingaryfirlit](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 skráarsnið skilaboða með bankayfirliti
-   CODA-skráarsnið fyrir bankayfirlit. Frekari upplýsingar eru í [CODA-bankayfirlit](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Innflutnings- og skilaboð greiðslna viðskiptavina og lánardrottna
Auk bankayfirlita geta bankar einnig sent sérstök skilaboð með upplýsingar um greiðslur viðskiptavina og lánardrottna sem hægt er að flytja inn í Dynamics 365 for Operations og stemma af við færslur viðskiptavina og lánardrottna. Þegar fyrirtæki þarf að fá upplýsingar um mótteknar greiðslur frá viðskiptavini frá bankanum er hægt að nota innflutningssniðin. Fyrir fyrirtæki sem nota beingreiðslur og kreditfærslur er hægt að móttaka skilaboðin til að uppfæra stöðu greiðslna sem voru fluttar út áður. Munurinn á innflutningssniðum og skilasniðum er að skil eru helst notuð til að uppfæra greiðslubókarlínur sem þegar hafa verið stofnaðar (hægt er að stofna þær þegar beingreiðslum eða kreditfærslum er komið á) í stað þess að stofna nýjar línur. Sum flóknari innflutningssnið geta einnig innihaldið skil. Eftirfarandi dæmi sýnir þessi skipting á að fara fram.

##### <a name="import-formats"></a>Innflutningssnið

-   ISO 20022 camt.054 skilaboð með tilkynningu frá banka
-   [Nets-innflutningssnið](emea-nor-nets-import-format.md) - Flókinn eiginleiki fyrir norsk greiðslusnið
-   Innflutningur ESR-greiðslna viðskiptavinar
-   Innflutningsgreiðslusnið fyrir Svíþjóð - BankGirot Max og BankGirot OCR-snið

##### <a name="return-formats"></a>Skilasnið

-   ISO 20022 pain.002 skýrsla um greiðslustöðu
-   (DNK) BetalingsserviceBasis-returformat – Skilasnið fyrir útflutningssnið viðskiptavinarins Betalingsservice
-   [Innflutningsgreiðslusnið fyrir Svíþjóð](emea-swe-payment-formats-import.md) - Bankgirot Autogiro skilar
-   (SWE) BankGirot skil – Skilasnið fyrir greiðslur lánardrottna, sem samsvarar Bankgirot-útflutningssniðinu



