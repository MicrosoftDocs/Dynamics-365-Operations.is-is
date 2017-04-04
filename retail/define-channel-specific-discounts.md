---
title: "Skilgreina afslætti sem tengjast tilteknum rásum"
description: "Smásala stilla oft inn mismunandi afslætti á mismunandi rásum. Í þessu efnisatriði eru skoðuð hugtök sem nauðsynlegt er að þekkja til að stofna afslátt fyrir tiltekna rás."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Skilgreina afslætti sem tengjast tilteknum rásum

Smásala stilla oft inn mismunandi afslætti á mismunandi rásum. Í þessu efnisatriði eru skoðuð hugtök sem nauðsynlegt er að þekkja til að stofna afslátt fyrir tiltekna rás. 

<a name="channel-specific-discounts"></a>Afslættir sem tengjast tilteknum rásum
--------------------------

Smásala bjóða oft mismunandi afslætti á mismunandi rásum. Þetta er getur gert aðsetur markaðinn staðbundið skilyrði eða við competing smásala.

Notar verðflokka til að skilgreina rás afslætti fyrir smásölu og commerce í Microsoft Dynamics 365 fyrir Aðgerðir. Hægt er að úthluta verðflokkum við eitt eða fleiri af eftirfarandi einingar: rásir vörulista, tengsl og vildarkerfi. Þessi skrá fjallað um rásir, en sömu hugtök eiga við vörulistaafslætti, tengslaafslætti og vildarkortaafslætti.

## <a name="price-groups"></a>Verðflokkar
\[myndatexta = "viðhengi\_256084" jafna = "alignnone" breidd = "640"\][![Verð flokka](./media/price-groups-1024x608.png)](./media/price-groups.png) Verð flokka tengla fyrir Retail\[/myndatexti\]

Á skýringarmyndinni ofan sýnir tengslin á milli mismunandi gerðir afslátt sem hægt er að skilgreina og einingar sem hugsanlega á færslu (rásar, vörulista, sambands, viðskiptavinur, vildarkort). Allar færslur eiga sér stað í rás, svo sem leiðin er tryggt kalli til að vera til staðar í færslu. Eftirstandandi einingar eru valkvæðar. Á öllum síðum aðalgagna er tengill við tengdar verðflokkasíðu þar sem hægt er að skoða og bæta við verðflokkar eftir þörfum. Verðflokkur er notuð til að tengjast fjórar tegundir einingar afslætti verðleiðréttingar og viðskiptasamninga. Ráðlagt að áætla stjórnunarstefnu fyrir hvernig verður nafn þitt verðflokka til að geyma þau sérstaklega. Einn valkostur væri að nota í bókstaf eða númer forskeyti eða viðskeyti til að greina milli mismunandi gerðum. Til dæmis 1-xxxxx verðflokkar rásar og 2-xxxxx verðflokka vörulista. Til eru fjórar fyrirspurnarsíður sem áherslu leggja á hverja smásölueiningu sem geta verið með afslætti tengda við sig.

-   **Verðflokkar rásar í smásölu ** - Þessi síða sýnir lista yfir rásir og afslætti sem eru tengdar saman fyrir hvern verðflokk.
-   **Verðflokkar vörulista** - Þessi síða sýnir lista yfir vörulista og afslætti sem eru tengdar saman fyrir hvern verðflokk.
-   **Verðflokkar vildarkerfis** - Þessi síða sýnir lista yfir vildarkerfi og afslætti sem eru tengdar saman fyrir hvern verðflokk.
-   **Verðflokkar tengsla ** - Þessi síða sýnir lista yfir tengst og afslætti sem eru tengdar saman fyrir hvern verðflokk.

## <a name="example-channel-discount-set-up"></a>Uppsetning afsláttar fyrir dæmarás
Eftirfarandi dæmi sýnir verkefnunum sem felast í að setja upp afslátt rásar.

1.  Í þessu dæmi ertu með rás sem kallast **Houston**, og það er verið að stofna nýjan afslátt kallaðan **Aftur í skólann.**
2.  Þar sem stjórnunarstefna verðs og afsláttar inniheldur möguleika á afslætti fyrir rás, er alltaf stofnaður verðflokk bundnum við rás þegar rás er stofnuð.
3.  Verðflokkurinn er **Houston-PG** og er úthlutað á **Houston** rás.
4.  Eftir að Búið er að stofna nýja **aftur í skólann** afsláttur, þarf að smella á **Verðflokkar** efst í **Afsláttur** síðu. **Afsláttarverðflokka** síðan opnast. Smellið því næst á **Nýtt** og velja **Houston -PG** verðflokk.
5.  Nú hægt að virkja afsláttinn og færa hann í rás.

 

<a name="see-also"></a>Sjá einnig
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


