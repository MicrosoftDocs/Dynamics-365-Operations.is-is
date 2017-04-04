---
title: "Rekja þóknanir í POS með söluflokka"
description: "Er algengur háttur smásölu til að rekja sölu með því að tengja sem unnið er með viðskiptavin er — með aðstoð, selja upp krosssölu og vinnur með færsluna."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Rekja þóknanir í POS með söluflokka

Er algengur háttur smásölu til að rekja sölu með því að tengja sem unnið er með viðskiptavin er — með aðstoð, selja upp krosssölu og vinnur með færsluna.

Rekja sölu eftir sölufulltrúi er mæling tengir selja hæfni er við sölu eftir gjaldkeri mæling hraða og skilvirkni. Vsk sem er rakin eftir sölufulltrúi eru einnig oft notuð til að reikna þóknanir eða öðrum hvatningargreiðslur.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Skilgreining starfsmanns verður sölufulltrúi í Sölustaðar
Þegar starfsmaður er bætt við sölu, verða þær hæfur fyrir þóknun og hægt er að auðkenna sem sölufulltrúi í kerfinu. Starfsmaðurinn sem er ekki í söluflokkur er ekki hæfur fyrir þóknun og ekki talin upp sem sölufulltrúi á sölustað. forritið. POS, í lista yfir sölufulltrúa er fenginn úr öllum söluflokka sem innihalda a.m.k. einn starfsmann sem er úthlutað á verslunina. Listinn birtist í POS sem samsetning Kenni og Heiti Vsk (Kenni: Heiti). Sjálfgefinn flokk sölu er hægt að úthluta til að styðja aðstæður þar sem það retailer velur sölufulltrúa á Sölustað línum sjálfvirkt stillt á starfsmenn. Notendur geta valið úr sölupöntun flokkinn sem starfsmaðurinn er meðlimur.

## <a name="functionality-profile-settings"></a>Virkni forstillingar
Nokkrir af aðgerðum forstillingar fyrir verslun sem munu ákvarða flæði og ferli í POS sem snerta sölufulltrúa.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Ef þessi valkostur er gerður virkur POS útfyllist sjálfkrafa færslulínur með gildandi gjaldkeri söluflokkur sjálfgefið. Ef gjaldkeri hefur ekki söluflokkur sjálfgefna tilgreint, ekki að stilla gildi. Notandi gæti enn setja handvirkt söluflokka með POS hnitaneti hnappinum hnappinn.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | Þessi valkostur hefur þrjú möguleg gildi: ** Nei **-Ef þessi valkostur er valinn notandi ekki beðinn um að velja söluflokka. Gildi gæti enn stillt með því að nota í gjaldkeri sjálfgefinn Vsk flokk eða handvirkt með því að nota á Sölustað hnappinn hnappinn hnitanetinu. **Upphaf færslu** - Ef þessi valkostur er valinn og annað hvort í **Sjálfgefin til að gjaldkeri** valkosturinn er ekki virk eða gildandi gjaldkeri hefur ekki sjálfgefna söluflokkur og notandinn verður beðinn um að velja söluflokka við upphaf hverrar færslu. Velja söluflokkur úr þessari kvaðning sjálfgefinn allar línur síðari við valinn flokk. Notandi gæti enn setja handvirkt söluflokka með POS hnitaneti hnappinum hnappinn. **Fyrir hverja línu** - Ef þessi valkostur er valinn og annað hvort í **Sjálfgefin til að gjaldkeri** valkosturinn er ekki virk eða gildandi gjaldkeri hefur ekki sjálfgefna söluflokkur og notandi er beðinn um að velja flokk á sölu eftir hverja línu er bætt við. Notandi gæti enn setja handvirkt Vsk-flokk með því að nota hnappur hnappinn hnappahnits Sölustaðar. |
| **Krefjast**                           | Þessi valkostur á einungis við þegar POS er skilgreindur til að biðja um sölufulltrúa. Ef virkjaður notandinn þarf að velja söluflokkur áður en haldið er áfram. Annars notandanum kvaðningu, en hægt hætta við og halda áfram án þess að vali. Eftir að línan er bætt við notanda með nægilegar heimildir samt að fjarlægja söluflokka úr línunni. "Krefst sölufulltrúi" ekki beitt í þessu tilfelli.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Birta upplýsingar sölufulltrúa Vsk á skjánum Sölustaður færslur
POS skjásins færslu og efni eru skilgreinanleg með því að nota á skjá útlit hönnuðar og úthlutuðum útlit afgreiðsluskjás á verslanir, afgreiðslukassar eða starfsmenn. Í **sölufulltrúi** svæðinu er hægt að bæta við flipanum Línur kvittunarrúðunni.  Þetta verður að birta Kenni í tilgreinda Vsk-flokk fyrir hverja línu á skjánum færslu.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Bæta við Sölu sölufulltrúa aðgerðir á Sölustað hnappinn hnitanet
POS gerir notendum kleift að skilgreina hnappahnit sem eru hafðar með í útlit afgreiðsluskjás til að veita aðgang að aðgerðir Sölustaðar. Hægt er að tengja eftirfarandi aðgerðir Sölustaðar í hnappahnitum sem snerta biðlaraþjónustu Vsk.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aðgerð**                             | **Description**                                                                                                                                                                                                                                                                              |
| Stilla sölufulltrúa í línu          | Þessi aðgerð POS birtir lista yfir hæf Vsk-flokkar (Kenni: Heiti) fyrir verslunina. Velja Vsk-flokk af listanum verður gildið sett í gildandi færslulínu.                                                                                                            |
| Hreinsa sölufulltrúa í línu        | Þessi aðgerð POS fjarlægir gildandi flokk söluvirði úr gildandi færslulínu.                                                                                                                                                                                                  |
| Stilla sölufulltrúi í færslu   | Þessi aðgerð POS birtir lista yfir hæf Vsk-flokkar (Kenni: Heiti) fyrir verslunina. Velja Vsk-flokk af listanum mun stilla sjálfgildi í gildandi færslu. Öllum fyrirliggjandi línum án þess að úthluta söluflokkur verður stillt, ásamt öllum síðar bætt við línur. |
| Hreinsa sölufulltrúi í færslu | Þessi aðgerð POS fjarlægir gildandi Vsk flokk sjálfgildi úr gildandi færslu. Það ekki áhrif á þær línur sem þegar eru til í færslunni.                                                                                                                             |

## <a name="calculating-commissions"></a>Reikna út þóknun
Þóknun er reiknuð fyrir starfsmenn í söluflokka tilgreind við bókun uppgjörs eða bókun sölupöntunar. Upphæð þóknunar er ákvarðað samkvæmt þóknunarhluti starfsmanns, eins og skilgreint er í söluflokka og tengd þóknun stillingar útreikninga fyrir viðskiptavin og/eða afurðir í færslunni.


