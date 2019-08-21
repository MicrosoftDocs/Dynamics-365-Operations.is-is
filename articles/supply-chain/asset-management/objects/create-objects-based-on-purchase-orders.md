---
title: Stofna eignir byggt á innkaupapöntunum
description: Þetta efni útskýrir hvernig þú getur búið til lista yfir eignaliði sem hægt er að nota sem grunn til að búa til eignir fyrir viðhaldsverk í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 536795ac8ac164a6cc16e9ba22b0aa7bf30ddfd8
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783363"
---
# <a name="create-assets-based-on-purchase-orders"></a>Stofna eignir byggt á innkaupapöntunum

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þetta efni útskýrir hvernig þú getur búið til lista yfir eignaliði sem hægt er að nota sem grunn til að búa til eignir fyrir viðhaldsverk í eignastýringu. Miðað við eignaratriðin geturðu skoðað lista yfir innkaupapöntunarlínurnar sem eru búnar til á þeim hlutum. Tilgangurinn með þessari virkni er að búa til eign í eignastýringu auðveldlega út frá innkaupapöntun.

Í fyrsta lagi setur þú upp hlutina sem á að nota til að búa til eignir frá innkaupapöntun í **Eignir**. Eftir að þú hefur stofnað innkaupapöntunarlínu býrðu til eignirnar í **Eignir í bið**. Það er hægt að ákveða á hvaða stigi innkaupapöntunar eignin ætti að vera stofnuð.


## <a name="select-asset-items"></a>Velja eignaliði

1. Smelltu á **Eignastýring** > **Uppsetning** > **Eignir** > **Hlutir**.
2. Smelltu á **Nýtt** til að stofna eignalið.
3. Veldu vöru í reitnum **Vörunúmer**. Þegar þú ferð úr þessum reit er nafn vörunnar sjálfkrafa sett inn í reitinn **Vöruheiti**.
4. Á flýtiflipanum **Almennt** velurðuu eignategund fyrir vöruna.
5. Veldu eignaframleiðanda og gerð fyrir vöruna.
6. Vista vöruna


## <a name="create-assets-from-pending-assets"></a>Búðu til eignir úr eignum í bið

1. Smelltu á **Eignastýring** > **Sameiginlegt** > **Eignir** > **Eignir í bið**.
2. Þú munt sjá uppfærðan lista yfir innkaupapantanir út frá vörunum sem voru valdar í **Eignir**.
3. Þú getur síað stöðu innkaupapantana til að velja í hvaða líftímastöðu eignin ætti að vera búin til. Til dæmis gætirðu aðeins viljað búa til eignir þegar vörukvittun hefur verið bókuð í innkaupapöntun.
4. Veldu tengilinn **Tilvísunarnúmer** á innkaupapöntunarlínu til að skoða ítarlegar upplýsingar um vöruna.
5. Ef þú vilt breyta hvaða víddir birtast á flýtiflipanum **Birgðavíddir** smellirðu á **Sýna víddir** og velur valkosti þína.
6. Ef þú vilt búa til eign byggða á innkaupapöntunarlínu skaltu velja gátreitinn í dálkinum **Merkja** fyrir þá línu á listasíðunni og smella á **Stofna eignir**. Skilaboð verða birt þar sem upplýsingar um eignaauðkenni eru tilkynntar.
7. Veldu eignina í listanum **Allar eignir** og smelltu á hnappinn **Breyta** til að bæta meiri upplýsingum við eignina.
8. Í **Eignir í bið**, ef þú vilt eyða línu af því að þú vilt ekki búa til eign skaltu velja gátreitinn í dálkinum **Merkja** fyrir þá línu og smella á **Fleygja eignum í bið**. Skilaboð verða birt þar sem upplýsingar um eignaauðkenni eru tilkynntar. Þú ert ekki að eyða innkaupapöntuninni eða sölupöntuninni, heldur skránni sem þú gætir hafa stofna eign frá í **Eignastýring**.

>[!NOTE]
>Allar vöruvíddir (stærð, litur, stillingar osfrv.) eru sjálfkrafa færðir yfir í eignareigindirnar. Rakningarvíddir (raðnúmer) eru geymdar beint á eigninni þegar eignin er stofnuð.


## <a name="find-pending-assets"></a>Finndu eignir í bið

Þú getur keyrt **Fjöldi eigna í bið** til að athuga hvort eignir séu í bið. Til dæmis er hægt að nota þessa aðgerð til að fá tilkynningu í hvert skipti sem eign í bið er tilbúin til að búa til sem eign.

1. Smelltu á **Eignastýring** > **Reglubundið** > **Eignir** > **Fjöldi eigna í bið**.
2. Smelltu á **Í lagi** til að keyra starfið og uppfæra listann í **Eignir í bið**.
3. Þú getur sett þetta starf upp til að keyra sem runuvinnslu, til dæmis einu sinni á dag.

**Varúð:** Ef gögnum er breytt í innkaupapöntun *eftir* að þú hefur búið til eign byggða á vörunni sem hún tilheyrir munu þessar breytingar ekki koma fram á eigninni.
