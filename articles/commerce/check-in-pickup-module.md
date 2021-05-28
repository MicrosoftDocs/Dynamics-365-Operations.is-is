---
title: Innskráning í afhendingareiningu
description: Þetta efnisatriði fjallar um innskráningu fyrir afhendingareiningu og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937592"
---
# <a name="check-in-for-pickup-module"></a>Innskráning í afhendingareiningu

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði fjallar um innskráningu fyrir afhendingareiningu og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.

Innskráning fyrir afhendingareiningu býður upp á staðfestingarsíðu fyrir viðskiptavini sem nota Dynamics 365 Commerce innskráningarmöguleika viðskiptavinar til að láta verslun vita um komu þeirra. Innskráning fyrir afhendingareiningu gerir einnig kleift að skilgreina snið sem safnar viðbótarupplýsingum frá viðskiptavinum til að auðvelda afhendingu á pöntun. Þessar upplýsingar innihalda bílastæðanúmer viðskiptavinar og tegund bifreiðar. 

## <a name="module-properties"></a>Eiginleikar einingar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Staðfestingartexti | Textastrengur | Efni fyrir fyrirsögnina sem birtist á staðfestingarsíðu innskráningar. |
| Sýna QR-kóða | **Satt** eða **Ósatt** | Þegar þessi eiginleiki er stilltur á **Satt** sýnir staðfestingarsíða innskráningar QR-kóða sem stendur fyrir kenni pöntunarstaðfestingar. |
| Fyrirsögn viðbótarupplýsinga | Textastrengur | Efni fyrir fyrirsögnina sem birtist þegar reitir viðbótarupplýsinga hafa verið skilgreindir. |
| Lyklar viðbótarupplýsinga | Par tilfangakennis/tilfangagildis | Hver lykill býr til innfærslureit og tengt merki sem er notað til að safna viðbótarupplýsingum frá viðskiptavinum. |
| Lyklar viðbótarupplýsinga \> tilfangakenni | Textastrengur | Hver upplýsingalykill býr til innfærslureit og tengt merki sem er notað til að safna viðbótarupplýsingum frá viðskiptavinum. Þessi eiginleiki tilgreinir lykil viðbótarupplýsinga. Í verkinu sem er búið til á sölustað er verðmæti þessarar eignar sýnt sem merkið í leiðbeiningareitnum. |
| Lyklar viðbótarupplýsinga \> tilfangagildi | Textastrengur | Merkið fyrir textareitinn í verkinu á sölustað. |
| Lyklar viðbótarupplýsinga \> áskilið | **Satt** eða **Ósatt** | Í þessari eign er tilgreint hvort viðskiptavinir þurfi að fylla út eyðublaðsreitinn áður en þeir geta haldið áfram. Þegar þessi eiginleiki er stilltur á **Satt** er stjarna sýnd við hliðina á skjámyndarmerkinu og núll-athugun er gerð til að koma í veg fyrir að viðskiptavinir haldi áfram ef ekkert gildi er slegið inn. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Bæta innskráningu fyrir afhendingareiningu við síðu

Bæta á innskráningu afhendingareiningar við nýju síðuna sem búin er til fyrir staðfestingu innskráningar. Sú síða mun vera upplifun staðfestingar á innskráningu fyrir viðskiptavini sem velja tengilinn **Ég er mætt(ur)** eða hnapp í tölvupóstinum. 

## <a name="configure-the-additional-information-form"></a>Skilgreina skjámynd viðbótarupplýsinga

Ef engir lyklar viðbótarupplýsinga eru skilgreindir sýnir einingin viðskiptavinum sjálfkrafa staðfestingarsíðu innskráningar. Þegar staðfesting innskráningar er sýnd, er verk stofnað á sölustað fyrir verslunina þar sem sækja á pöntunina.

Þegar einn eða fleiri lyklar viðbótarupplýsinga eru skilgreindir, eru viðskiptavinir fyrst beðnir að slá inn upplýsingar. Þegar þeir velja **Senda inn** fá þeir að sjá staðfestingu innskráningar og verk er stofnað á sölustað. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Virkja innskráningartilkynningar viðskiptavinar á sölustað (POS)](enable-customer-check-in.md)