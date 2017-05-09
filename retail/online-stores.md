---
title: Yfirlit netverslunar
description: "Þessi grein gefur upplýsingar um netverslanir í smásölu og hvernig setja skal þær upp í Microsoft Dynamics 365 for Operations."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 40fbf8b4fdfed32dd67013b6b21cc2c8ee3d31e6
ms.lasthandoff: 03/31/2017


---

# <a name="online-store-overview"></a>Yfirlit netverslunar

[!include[banner](includes/banner.md)]


Þessi grein gefur upplýsingar um netverslanir í smásölu og hvernig setja skal þær upp í Microsoft Dynamics 365 for Operations.

Smásölu og viðskipti í Dynamics 365 for Operations styður mörg smásölurása. Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir). Netverslun gefur smásölum viðveru á netinu svo að viðskipavinir þeirra geti keypt afurðir úr netverslun þeirra til viðbótar við smásöluverslanir þeirra. Ef Viðskiptamenn kaupa afurðir úr netverslun geta þeir fengið þær sendar til sín eða sótt þær í staðbundna verslun. Þú stofnar netverslun í Dynamics 365 for Operations-biðlara. Þessi netverslun er síðan birt til netverslunar þriðja aðila sem er samþætt við Dynamics 365 for Operations. Netverslun þriðja aðila gegnir hlutverki búðarglugga (UI) fyrir netverslunina og veitt val um stjórnkerfi viðskiptavinar (CMS) og UI getu. Nokkrar samþættingar af þessari gerð eru tiltækar fyrir Dynamics 365 for Operations. Eiginleikar sem eru tilgreindar fyrir netverslunina stýrir atferli netverslunarinnar. Til dæmis skilgreina tegundastigveldi yfirlitsflokks Dynamics 365 for Operations og úthluta því á netverslun. Þegar netverslun er birt fyrir netverslun þriðja aðila, er tegundastigveldi yfirlitsflokks birt í netútgáfu verslunarinnar. Kaupendur nota síðan tegundastigveldi yfirlitsflokks til að fletta upp netverslunina og til að leita að afurðum. Til að stofna netverslun, verður að setja upp íhluti sem á að leyfa færslur sem vinna á fyrir verslunina. Til dæmis, þarf að bæta úrvali, nota eigindir og setja upp greiðsluhætti og sendingarmáta. Einnig er hægt að tilgreina verð, kynningartilboð, afslætti, viðskiptasamninga og sendingu greiðsluskilmála sem eiga við netverslun. Eftir að netverslunin hefur verið birt á netverslun þriðja aðila er hægt að stofna smásöluvörulista fyrir netverslunina. Afurðir í vörulistanum verða afurðaskráningar í netversluninni. Þegar sá sem verslar kaupir afurðir úr netverslun, eru tiltækar birgðir uppfærð og samstillt í á biðlaranum. Einnig eru sölupantanir myndaðar fyrir innkaup og send til biðlara fyrir pöntunarupplýsingum og vinnslu.

## <a name="set-up-an-online-store"></a>Uppsetning netverslunar
Til að setja upp netverslun, Það verður að ljúka eftirfarandi verkum:

1.  Stofna netverslun.
2.  Bæti netversluninni við viðeigandi stigveldi fyrirtækis
3.  Bæta við vöruúrval sem hafa með afurð sem eru í boði í netverslun.
4.  Úthluta eða stofna verðflokka fyrir netverslun.
5.  Setja upp afhendingarmátum sem eru í boði fyrir netversluninni.
6.  Úthluta greiðslumáta sem er viðurkenndir af netverslun.
7.  Ef shoppers til að panta afurðir á netinu og síðan taka þær í staðbundna verslun, úthluta verslun slóðarflokki netverslun.
8.  Úthluta eigindum fyrir rásir, afurðir og sölupantanir til netverslun. Eigindi rásar eiga við alla netverslun, afurðareigindum eiga við afurðir sem eru í boði í netversluninni og eigindum sölupöntunar eiga við sölupantanir sem eru myndaðar úr netverslun.
9.  Varpa eigindum til að skilgreina eiginleika sem ákvarða hvernig þessar eigindir haga sér á netverslun. Til dæmis er hægt að skilgreina eigindir eins og þörf er á eða sem leitanlegar.
10. Birta netverslun til að búa til uppbyggingu verslunar að eigin vali fyrir netverslun þriðja aðila. **Mikilvægt** Áður en hægt er að birta netverslun í , þarf að setja upp dreifingarstað fyrir hana.

## <a name="retail-channel-navigation-hierarchies"></a>Yfirlitsstigveldi smásölurásar
Áður en hægt er að stofna netverslun þarf að skilgreina yfirlitsstigveldi smásölurásar sem á að nota fyrir hana. Yfirlitsstigveldi smásölurásar táknar tegundastigveldi sem birtist í netversluninni eftir verslun er birt. Þegar þú birtir vörulista smásölu á netverslun, eru afurðirnar í vörulista varpaðar á flokka í yfirlitsstigveldi smásölurásar. Stigveldið er notuð af þeim sem versla til að fletta í netversluninni.

## <a name="organization-hierarchies"></a>Stigveldi fyrirtækis
stigveldi fyrirtækis er Notað fyrir uppbyggingu smásölurása. Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri. Þegar settar eru upp netverslanir er hægt að bæta þeim við stigveldi fyrirtækis. Verslanir samnýta gögn sem er notað fyrir úrval áfyllingar og skýrslugerð. Þegar stofnað er stigveldi fyrirtækis, er málefni úthlutað til þess. Málefni gefur til kynna hvernig stigveldi er notað í uppbyggingu business. Hægt er að stofna eitt stigveldi fyrirtækis fyrir verslunaraðgerðir þínar og nota það stigveldi úrval, áfyllingar og skýrslugerð. Einnig er hægt að stofna sérstakt stigveldi fyrirtækis fyrir hvern tilgang. Einnig er hægt að stofna mörg stigveldi sem hafa sama tilgangi og úthluta aðskilinni rás til hvers og eins. Ef ætlunin er að birta vörulista smásölu á netverslun, ætti að lágmarki að bæta netverslanir við stigveldi fyrirtækis fyrir úrval. Afurðir í vörulista eru valdar úr úrvali afurða sem eru úthlutað til netverslana. Þegar vörulistinn er birtur ber birtingu ferli gildisdagsetninga fyrir úrval sem tengdur er við netverslun með afurðir sem eru í vörulista til að ákvarða hvaða vörur skulu vera tiltækar í netversluninni.




