---
title: "Uppfærsla staðalkostnaðar fyrir nýja framleidda vöru"
description: "Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði fyrir nýja framleidda vöru."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 84b9f91f49e988244b98aeb7a6a6344548d6a8c0
ms.lasthandoff: 03/31/2017


---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Uppfærsla staðalkostnaðar fyrir nýja framleidda vöru

[!include[banner](../includes/banner.md)]


Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði fyrir nýja framleidda vöru. 

Eftirfarandi leiðbeiningar gera ráð fyrir að notuð sé tveggja útgáfu nálgunin til að uppfæra staðlaðan kostnað. Í þessari nálgun inniheldur ein kostnaðarútgáfa upphaflega skilgreindan staðlaðan kostnað fyrir fryst tímabil og seinni kostnaðarútgáfan inniheldur stigvaxandi uppfærslur sem eiga við nýju framleiddu vörurnar. Stigvaxandi uppfærslur eru færðar inn sem kostnaðarfærslur innan seinni kostnaðarútgáfunnar og að lokum gerðar virkar. Tveggja útgáfu nálgunin krefst þess að skilgreind sé önnur kostnaðarútgáfa. Hér eru leiðbeiningar fyrir skilgreiningu þessarar kostnaðarútgáfu:

-   Notið kostnaðargerðina **Staðlaður kostnaður**.
-   Gefið kostnaðarútgáfunni marktækt kenni sem skýrir innihaldið, til dæmis **2016-UPPFÆRSLUR**.
-   Í svæðisflokknum **Leyfa verðtegundir** gangið úr skugga um að **Kostnaðarverð** sé stillt á **Já**.
-   Leyfið að kostnaðarskýrslur séu færðar inn fyrir öll svæði (það er að segja, skiljið reitinn **Svæði:** eftir autt). Ef svæði er fært inn, er aðeins hægt að færa kostnaðarfærslur inn fyrir það svæði.
-   Notið varaúrræðið **Virkt**.

Ef bæta á við nýjum framleiðsluvörum í gegnum fryst tímabil, skal fylgja eftirfarandi skrefum.

1.  Notið skjámyndina **Uppsetning kostnaðarútgáfu**til að leyfa skráningu á kostnaðarfærslum inn í seinni kostnaðarútgáfuna sem inniheldur stigvaxandi uppfærslur. Komið í veg fyrir virkjun biðkostnaðar, þar sem virkjun er leyfð eftir að kostnaður í bið hefur verið algerlega og nákvæmlega skilgreindur. Tilgreinið auða upphafsdagsetningu sem reglu í kostnaðarútgáfunni og færið svo lokadaginn inn þegar hver kostnaðarfærsla er færð inn. Upphafsdagsetningin ætti að vera áður en nýju vörurnar verða keyptar inn eða framleiddar.
2.  Notið skjámyndina **Vöruverð** til að færa inn kostnaðarfærslur fyrir nýjar innkeyptar vörur. Fyrir hverja kostnaðarfærslu skal færa inn kostnaðarútgáfuna sem inniheldur stigvaxandi uppfærslur og nota upphafsdagsetningu sem kemur á undan væntanlegri framleiðsludagsetningu fyrir nýjar framleiddar vörur.
3.  Reiknið út kostnað nýframleiddra vara með því að nota skjámyndina **Útreikningur**. Opnið síðuna **Útreikningur** frá síðunni **Viðhald kostnaðarútgáfu** og veljið síðan kostnaðarútgáfuna sem inniheldur stigvaxandi uppfærslur. Notið valskilyrðin til að tilgreina nýframleidda vöru og alla framleidda íhluti hennar. Einnig gæti verið nauðsynlegt að tilgreina allar yfirvörur innan margstiga framleiðslubyggingar sem innihalda nýframleiddu vörurnar sem íhluti. Færið inn upphafsdagsetningu fyrir uppskriftarútreikninginn sem samsvarar byrjun framleiðslu fyrir nýframleiddu vörurnar. Upphafsdagsetningin ætti að vera innan gildisdagsetninga fyrir uppskriftarútgáfu og leiðarútgáfu vörunnar. **Athugið:**Týnd kostnaðarfærsla getur táknað nýja framleidda vöru. Uppskriftarútreikningar geta takmarkast við vörur með týndum kostnaði.
4.  Gangið úr skugga um að reiknaður kostnaður fyrir nýjar framleiddar vörur sé fullunninn og nákvæmur. Notið síðuna **Fullvinna** til að fara yfir reiknaðan kostnað hverrar vörukostnaðarfærslu og til að skoða viðvaranir úr athugasemdakladda. Einnig er hægt að nota síðuna **Útreikningur** til að fara yfir reiknaðan kostnað.
5.  Notið síðuna **Uppsetning kostnaðarútgáfu** til að breyta lokunarflaggiu til að heimila virkjun á biðkostnaðarfærslum í seinni kostnaðarútgáfunni.
6.  Notið síðuna **Virkja verð** (sem er opnuð úr síðunni **Viðhald kostnaðarútgáfu**) til að virkja allar biðkostnaðarfærslur í seinni kostnaðarútgáfunni. Einnig er hægt að virkja kostnaðarfærslur í bið fyrir stakar vörur með því að smella á hnappinn **Virkja** á síðunni **Vöruverð**.
7.  Notið síðuna **Uppsetning kostnaðarútgáfu**til þess að breyta lokunarflöggum í síðari kostnaðarútgáfunni og koma í veg fyrir frekara gagnaviðhald. Lokunarreglurnar hindra færslu nýs kostnaðar í bið og virkjun kostnaðar í bið.





