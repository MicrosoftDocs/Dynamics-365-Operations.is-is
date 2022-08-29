---
title: Reikningur vegna viðhalds á eignum viðskiptavinar
description: Þessi grein útskýrir hvernig á að búa til, vinna úr og innheimta viðhaldsvinnu sem er unnin á eignum sem viðskiptavinir þínir eiga.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c0d067ec4f2110b1c146ef0229b90e309578eaa7
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335076"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Reikningur vegna viðhalds á eignum viðskiptavinar

[!include [banner](../../includes/banner.md)]

Eiginleikinn *Innheimta verkbeiðni* gerir kleift að stofna, vinna úr og rukka fyrir viðhaldsvinnu sem gerð er á eignum sem viðskiptavinir eiga. Þessi eiginleiki gerir notendum kleift að framkvæma eftirfarandi verkefni:

- Tengja viðskiptavini við eignirnar sem þeir eiga.
- Velja viðskiptavin og skoða eignirnar sem viðskiptavinur á þegar verkbeiðni er stofnuð.
- Setja upp yfirverk fyrir hvern viðskiptavin.
- Skrá vinnustundir, vörur, kostnað og gjöld á móti verkbeiðni og stofna síðan reikningstillögu fyrir viðskiptavininn síðar.

Að auki býður eiginleikinn upp á eftirfarandi virkni:

- Verksamningurinn úr yfirverki viðskiptavinar er sjálfkrafa afritaður í viðeigandi verkbeiðni verks.
- Eignastýring getur nú notað verkfærslugerðina *þóknun* á bæði spár verkbeiðnir og færslubækur verkbeiðni.

## <a name="turn-on-the-customer-billing-feature"></a>Kveikja á reikningseiginleika viðskiptavinar

Áður en þú getur notað þennan eiginleika verður að kveikja á honum fyrir kerfið þitt. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Verkefnastjórnun og bókhald*
- **Heiti eiginleika:** *Innheimta verkbeiðni*

## <a name="example-scenario"></a>Dæmi

Til að fá upplýsingar um hvernig þessi eiginleiki virkar skal fylgja eftirfarandi aðstæðum.

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../../fin-ops-core/fin-ops/get-started/demo-data.md) er sett upp. Nauðsynlegt er að velja **USMF**-lögaðila áður en byrjað er.

Einnig er hægt að nota þessar aðstæður sem leiðsögn um notkun á eiginleikanum þegar unnið er í framleiðslukerfi. Í slíku tilfelli þarf hinsvegar að skipta út eigin gildum og einhverjar nauðsynlegar færslugerðir gæti vantað sem stöðluðu sýnigögnin bjóða upp á.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>Skref 1: Stofna nýjan verksamning fyrir viðskiptavininn

1. Opnaðu **Verkefnastjórnun og bókhald \> Verk \> Verksamningar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Nýr verksamningur**:

    - **Heiti:** *Pelican Wholesales*
    - **Gerð fjármögnunar:** *Viðskiptavinur*
    - **Uppruni fjármögnunar:** *US-013* (*Pelican Wholesales*)

1. Veljið **Í lagi**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>Skref 2: Búa til nýtt yfirverk fyrir viðskiptavininn

Yfirverkið sem er stofnað hér verður notað þegar verkbeiðnir fyrir viðskiptavininn eru stofnaðar.

1. Opnaðu **Verkefnastjórnun og bókhald \> Verk \> Öll verk**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Nýtt verkefni**:

    - **Gerð verks:** *Tími og efni*
    - **Heiti verks:** *Pelican Wholesales work orders*
    - **Verkflokkur:** *TM*
    - **Verksamningskenni:** *Pelican-Sales* (samningurinn sem var stofnaður fyrr)
    - **Upphafsdagsetning:** Veldu daginn í dag.

1. Velja **Stofna verk**.
1. Nýja verkið er opnað. Skráið niður gildið **Verkkenni**. Nauðsynlegt er að færa það inn síðar.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>Skref 3: stofna nýja gerð verkbeiðni í Eignastýring

1. Farið í **Eignastýring \> Uppsetning \> Verkbeiðni \> Gerðir verkbeiðna**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Nýrri færslu er bætt við listann. Stillið eftirfarandi gildi fyrir hana:

    - **Gerð verkbeiðni:** *Þjónusta*
    - **Heiti:** *Verkbeiðnir þjónustu*
    - **Líftímastaða verkbeiðni:** *Venjuleg*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>Skref 4: Tengja viðskiptavinalykil við yfirverk

Nú verður að tengja viðskiptavinalykilinn við yfirverkið í verkuppsetningu eignastýringar.

1. Farið í **Eignastýring \> Uppsetning \> Verkbeiðnir \> Uppsetning verks**.
1. Í flipanum **Yfirverk** skal velja **Bæta við** til að bæta við línu.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Viðskiptavinalykill:** *US-013* (*Pelican Wholesales*)
    - **Kenni verks:** Færið inn verkkennið sem skrifað var niður hér á undan.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>Skref 5: Tengið verkflokkinn og gerðina við verk verkbeiðninnar

Þú ættir enn að vera á síðunni **Uppsetning verks** (**Eignastýring \> Uppsetning \> Verkbeiðnir \> Uppsetning verks**).

1. Í flipanum **Verkflokkur** skal velja **Bæta við** til að bæta við línu.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Gerð verkbeiðni:** *Þjónusta* (verkbeiðnigerðin sem stofnuð var hér á undan)
    - **Verkflokkur:** *TM*

> [!NOTE]
> Verksamningur fyrir verk verkbeiðni er alltaf fenginn frá yfirverkinu.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>Skref 6: Tengja eign við kenni viðskiptavinar

1. Opnið **Eignastýring \> Eignir \> Virkar eignir**.
1. Í reitinn **Sía** skal slá inn *VE-102* og velja að sía eftir **Eign**.
1. Veljið eignina til að opna stillingar hennar.
1. Í flipanum **Viðskiptavinur** skal stilla **Viðskiptavinareikningur** reitinn á *US-013* (*Pelican Wholesales*).

    Reiturinn **Heiti** uppfærist sjálfkrafa í *Pelican Wholesales*.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>Skref 7: Stofna nýja verkbeiðni fyrir eignina

1. Opnið **Eignastýring \> Verkbeiðnir \> Virkar verkbeiðnir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláðu inn eftirfarandi gildi í svarglugganum **Búa til verkbeiðni**:

    - **Gerð verkbeiðni:** *Þjónusta*
    - **Lýsing:** *Viðgerð á vöruflutningabíl*
    - **Viðskiptavinalykill:** *US-013* (*Pelican Wholesales*)
    - **Eign:** *VE-102*

        > [!NOTE]
        > Uppfletting sýnir aðeins eignir sem eru tengdar við valinn viðskiptavinalykil.

    - **Gerð viðhaldsverks:** *Viðgerð*
    - **Starfsgrein:** *Bifvélavirki*
    - **Þjónustustig:** *4*

1. Veljið **Í lagi**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>Skref 8: Yfirfara verkbeiðni og hefja vinnu á henni

Í þessum hluta verður unnið í verkbeiðninni sem stofnuð var í fyrri hlutanum.

1. Fylgið eftirfarandi skrefum til að staðfesta að foreldrahlutverkið sé *Pelican wholesales verkbeiðni*:

    1. Í hlutanum **Viðhaldsverk verkbeiðni** skal velja línu.
    1. Í flýtiflipanum **Upplýsingar um línu** skal skoða gildið **Verkkenni**. Það ætti að vera númer tengt með bandstriki á forminu *\<Parent-Project-ID\>-\<Project-ID\>*. Gildið er tengill.
    1. Veljið tengil verkkennis til að opna síðu þar sem hægt er að skoða yfirverkið og verkheiti.

1. Á aðgerðasvæðinu, í flipanum **Verkbeiðni**, í flokknum **Líftímastaða**, skal velja **Uppfæra stöðu verkbeiðni**.
1. Í svarglugganum **Uppfæra stöðu verkbeiðni**, í dálkinum **Velja**, skal velja gátreitinn fyrir línuna þar sem reiturinn **Líftímastaða** er stilltur á *Í vinnslu*.
1. Veljið **Í lagi**.
1. Í svarglugganum **Líftímastaða: InProgress** skal velja **Í lagi**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>Skref 9: Bóka vinnustundirnar sem fóru í verkbeiðnina og stofna nýja reikningstillögu

Í þessum hluta verður haldið áfram að vinna í verkbeiðninni sem unnin var í fyrri hlutanum.

1. Á aðgerðasvæðinu, í flipanum **Verkbeiðni**, í flokknum **Verk**, skal velja **Færslubækur**.

    Síðan **Færslubækur verkbeiðni** birtist. Hér er hægt að skrá tímann sem var eytt í verkbeiðni.

1. Í flýtiflipanum **Vinnustundir** skal velja **Bæta við línu**.
1. Stillið reitinn **Klukkustundir** á *4* á nýju línunni.
1. Á aðgerðasvæðinu skal velja **Bóka færslubækur**.
1. Lokið síðunni **Færslubækur verkbeiðni** til að fara aftur í verkbeiðnina.
1. Á aðgerðasvæðinu, í flipanum **Reikningsfærsla**, skal velja **Ný reikningstillaga**.
1. Í svarglugganum **Stofna reikningstillögu**, í hlutanum **Verkfærslur**, skal velja gátreitinn **Velja** fyrir hverja línu sem á að reikningsfæra.
1. Veljið **Í lagi** til að loka svarglugganum og skoða nýju reikningstillöguna.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]