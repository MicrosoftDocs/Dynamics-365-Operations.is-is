---
title: Skilgreina afslætti sem tengjast tilteknum rásum
description: Smásala stilla oft inn mismunandi afslætti á mismunandi rásum. Í þessu efnisatriði eru skoðuð hugtök sem nauðsynlegt er að þekkja til að stofna afslátt fyrir tiltekna rás.
author: scott-tucker
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 14b6f8f4a7d344111718fad94418bc3dbb5c9b1e113c0fd613350c49a2511d4f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759312"
---
# <a name="define-channel-specific-discounts"></a>Skilgreining afslátta fyrir tiltekna rás

[!include [banner](includes/banner.md)]

Í þessu efnisatriði eru skoðuð hugtök sem nauðsynlegt er að þekkja til að stofna afslátt fyrir tiltekna rás.

## <a name="channel-specific-discounts"></a>Afslættir sem tengjast tilteknum rásum

Smásalar bjóða oft mismunandi afslætti á mismunandi rásum. Þetta getur verið gert til að ná til staðbundinna markaðsaðstæðna eða takast á við smásala í samkeppni.

Commerce notar verðflokka til að skilgreina rásarafslætti fyrir smásölu og viðskipti. Hægt er að úthluta verðflokkum við eitt eða fleiri af eftirfarandi einingar: rásir vörulista, tengsl og vildarkerfi. Þessi skrá fjallað um rásir, en sömu hugtök eiga við vörulistaafslætti, tengslaafslætti og vildarkortaafslætti.

## <a name="price-groups"></a>Verðflokkar

[![Verðflokkar.](./media/price-groups-1024x608.png)](./media/price-groups.png)

Skýringarmyndin að ofan sýnir tengslin á milli aðila sem geta verið á færslum (rásar, vörulista, sambands, viðskiptavinur, vildarkort) og mismunandi afsláttargerðir sem má stilla. Allar færslur eiga sér stað í rás, svo tryggt er að rás verði til staðar á færslu. Eftirstandandi einingar eru valkvæðar. Á öllum síðum aðalgagna er tengill við tengdar verðflokkasíðu þar sem hægt er að skoða og bæta við verðflokkar eftir þörfum. Verðflokkur er notuð til að tengjast fjórar tegundir eininga við afslætti, verðleiðréttingar og viðskiptasamninga. Ráðlagt er að undirbúa aðferð um það hvernig þú nefnir verðflokkana þína til að hafa þá skipulagða. Einn valkostur væri að nota bókstaf eða númersforskeyti eða viðskeyti til að greina milli mismunandi gerðum. Til dæmis 1-xxxxx fyrir verðflokka rásar og 2-xxxxx fyrir verðflokka vörulista. Til eru fjórar fyrirspurnarsíður sem áherslu leggja á hverja netverslunareiningu sem geta verið með afslætti tengda við sig.

- **Verðflokkar rásar** – Þessi síða sýnir lista yfir rásir og afslætti sem eru tengdar saman fyrir hvern verðflokk.
- **Verðflokkar vörulista** – Þessi síða sýnir lista yfir vörulista og afslætti sem eru tengdar saman fyrir hvern verðflokk.
- **Verðflokkar vildarkerfis** – Þessi síða sýnir lista yfir vildarkerfi og afslætti sem eru tengdar saman fyrir hvern verðflokk.
- **Verðflokkar tengsla** – Þessi síða sýnir lista yfir tengsl og afslætti sem eru tengdar saman fyrir hvern verðflokk.

## <a name="example-channel-discount-set-up"></a>Uppsetning afsláttar fyrir dæmarás

Eftirfarandi dæmi sýnir verkefnunum sem felast í að setja upp afslátt rásar.

1. Í þessu dæmi ertu með rás sem kallast **Houston**, og það er verið að stofna nýjan afslátt kallaðan **Aftur í skólann**.
2. Þar sem stjórnunarstefna verðs og afsláttar inniheldur möguleika á afslætti fyrir rás, er alltaf stofnaður verðflokk bundnum við rás þegar rás er stofnuð.
3. Verðflokkurinn er **Houston-PG** og er úthlutað á **Houston** rás.
4. Eftir að Búið er að stofna nýja **aftur í skólann** afsláttur, þarf að smella á **Verðflokkar** efst í **Afsláttur** síðu. **Afsláttarverðflokka** síðan opnast. Smellið því næst á **Nýtt** og velja **Houston -PG** verðflokk.
5. Nú hægt að virkja afsláttinn og færa hann í rás.

## <a name="additional-resources"></a>Frekari upplýsingar

[Verðleiðréttingar og afslættir](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]