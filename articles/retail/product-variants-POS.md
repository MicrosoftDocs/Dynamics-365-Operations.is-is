---
title: Uppfletting birgða á sölustað (POS)
description: Þetta efnisatriði lýsir þeim valkostum sem eru í boði til að skoða birgðaupplýsingar á sölustað (POS).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: cd2dc460c9e862503ebbf1942dcf998d67829d86
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "314418"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Uppfletting birgða á sölustað (POS)

[!include [banner](includes/banner.md)]

Uppfletting birgða á sölustað (POS) hjálpar smásölum að ná gæðarekstri í rauntíma og fá innsýn með því að tengja verslanir, POS og bakvinnslu. Þessi virkni veitir nákvæmt yfirlit í rauntíma yfir birgðastöðu afurða yfir verslanir og dreifingarmiðstöðvar. Hún hjálpar einnig smásölum að keyra aukna hagkvæmni og sparnað með því að betrumbæta birgðaáætlanagerð í rauntíma.

Nákvæmt yfirlit í rauntíma yfir birgðir yfir fyrirtæki hjálpar starfsfólki verslunar að veita tímanlega, betri þjónustu við viðskiptavini. Augnablikið sem skiptir mestu máli er augnablikið þegar viðskiptavinurinn er tilbúinn til að taka ákvörðun um kaup. Mikilvægt er að gjaldkeri í verslun hafi birgðaupplýsingar í rauntíma innan seilingar svo þeir geti lofað með nákvæmni afhendingu afurðar.

Hægt er að opna síðuna **Uppfletting birgða** frá vinnusvæðinu **Retail Modern POS** eða vinnusvæðinu **Retail POS í skýi**.

![Reitur uppflettingar á birgðum á heimasíðu POS](media/POSHomepage.png)

Á síðunni **Uppfletting birgða** er hægt að nota talnalyklaborð til að slá inn afurðarnúmer. Þá er hægt að skoða magn á lager fyrir margar verslanir og vöruhús.

![Uppflettingarsíða á stöðluðum birgðum](media/InventoryLookUp.png)

**Frátekið** og **Pantað** magn er einnig sýnt fyrir hverja staðsetningu.

- **Frátekið** - Þetta magn á við gildið **Efnislega frátekið** frá bakvinnslu fyrir tilgreint afurðarnúmer á staðsetningunni.
- **Pantað** - Þetta magn á við gildið **Pantað samtals** frá bakvinnslu fyrir tilgreint afurðarnúmer á staðsetningunni.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Staðsetningar þar sem upplýsingar um birgðaframboð eru sýndar fyrir

Listinn yfir staðsetningar inniheldur tvær tegundir eininga:

- **Smásöluverslanir** - Listinn sýnir verslanir sem eru skilgreindar með því að nota flokk verslanastaðsetjara fyrir núverandi verslun í höfuðstöðvum Retail.
- **Dreifingarmiðstöðvar** - Hægt er að skilgreina ýmis konar dreifingarmiðstöðvar (t.d. vöruhús) í Microsoft Dynamics 365 for Retail. Hins vegar sýnir listinn upplýsingar um birgðaframboð aðeins fyrir dreifingarmiðstöðvar af sjálfgefnu gerðinni **Staðall**.

    > [!NOTE]
    > Upplýsingar um birgðaframboð eru ekki sýndar fyrir vöruhús af gerðunum **Í flutningi**, **Biðgeymsla** og **Vörur á leið** fyrir POS.

Á síðunni **Uppfletting birgða** er hægt að skoða biðgeymslur ATP-afhendingarspár fyrir hverja verslun, til viðbótar við núverandi magn á lager, frátekið magn og pantað magn. Veldu verslunina til að skoða ATP-upplýsingar fyrir og veldu síðan **Sýna tiltækileika verslunar**.

![ATP-magn](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>Opna yfirlit víddarbyggðs fylkið til að sýna öll afbrigði

Á síðunni **Afurðarupplýsingar** afurðarsniðmáts, eða á síðunni **Uppfletting birgða** skal velja **Skoða öll afbrigði** úr forritastikunni neðst á síðunni. Yfirlitið **Víddarbyggt fylki** fyrir upphaflegu ræsinguna frá þessum síðum sýnir upplýsingar um birgðaframboð fyrir öll afbrigði afurðar fyrir núverandi verslun.

> [!NOTE]
> Hnappurinn **Skoða öll afbrigði** er aðeins í boði fyrir afurðarsniðmát vöru sem hefur afurðarafbrigði. Það er ekki í boði fyrir sjálfstæðar afurðir eða sett.

![Hnappurinn skoða öll afbrigði á uppflettingarsíðu birgða](media/StandardToMatrix.png)

Veldu **Skoða öll afbrigði** á síðunni **Afurðarlýsingar** fyrir afurðarsniðmát, eða á síðunni **Uppfletting birgða**, án þess að velja staðsetningu, til að fara í yfirlitið **Víddarbyggt fylki** til að skoða upplýsingar um birgðaframboð fyrir öll afbrigði afurðar fyrir núverandi verslun.

![Yfirlit víddarbyggðs fylkis fyrir uppflettingarsíðu birgða](media/Matrix.png)

> [!NOTE]
> Í skýringarmyndinni hér að framan er birtingarröð víddanna í stafrófsröð vegna þess að birtingarröð vídda var ekki stillt fyrir valda afurð.

Í yfirlitinu **Víddarbyggt fylki** innihalda hólf afurðarafbrigða virði lagerbirgða í neðra hægra horninu. Eftirfarandi tafla útskýrir merkingu á hinum ýmsu virðum.

| Virði á lager                            | lýsing |
|------------------------------------------|-------------|
| Tölugildi sem er meira en 0 (núll) | Afbrigði hefur verið gefið út á valda staðsetningu og þú getur framkvæmt fleiri aðgerðir í hólfinu. (Þessum aðgerðum er lýst nánar síðar í þessu efnisatriði.) |
| **0** (núll)                             | Afbrigði hefur verið gefið út á valda staðsetningu en varan er ekki tiltæk á valdri staðsetningu. Hins vegar er hægt að framkvæma fleiri aðgerðir í hólfinu. (Þessum aðgerðum er lýst nánar síðar í þessu efnisatriði.) |
| **Á ekki við** eða óvirkt hólf              | Afbrigði hefur ekki verið gefið út á valda staðsetningu og þú getur ekki framkvæmt fleiri aðgerðir í hólfinu. |

Einnig er hægt að breyta snúningi á víddum með því að velja nýju víddina sem á að nota.

![Breyta snúningi](media/ChangePivot.png)

![Snúningi breytt](media/PivotChanged.png)

> [!NOTE]
> Í framangreindri skýringarmynd er birtingarröð víddanna fyrir valda afurð sérsniðin (ekki í stafrófsröð). Það byggist á birtingarröð víddar sem er stillt í bakvinnslu.

Auk þess í yfirlitinu **Víddarbyggt fylki** er hægt að framkvæma fleiri aðgerðir sem hjálpa til við að auka vinnuafköst starfsmanns verslunar. Hér eru nokkur dæmi:

- Breyttu staðsetningu verslunar til að fletta upp á birgðaframboði á öllum afurðarafbrigðum á öðrum staðsetningum. Þessar staðsetningar innihalda aðrar verslanir í flokki verslanastaðsetjara af sjálfgefnum gerðinni **Staðall**.
- Seldu stakt afurðarafbrigði til viðskiptavinar með því að nota reiðufé og afhentu, sótt í verslun eða sent á aðsetur.
- Gefðu viðskiptavininum ATP-upplýsingar fyrir stök afurðarafbrigði á tiltekinni staðsetningu.

![Viðbótaraðgerðir á breytilegum reitum](media/VariantActions.png)

> [!NOTE]
> Í skýringarmyndinni hér að framan er birtingarröð víddanna í stafrófsröð vegna þess að birtingarröð vídda var ekki stillt fyrir valda afurð.

Eftirfarandi tafla veitir frekari upplýsingar um viðbótaraðgerðir sem eru í boði.

| Aðgerð               | lýsing |
|----------------------|-------------|
| Selja núna             | Bæta völdu vöruafbrigði við færsluna og beindu notandanum á færsluskjáinn. (Þessi aðgerð er ekki í boði þegar valin staðsetning er dreifingarmiðstöð.) |
| Sækja í verslun     | Búðu til pöntun viðskiptavinar fyrir afurðarfbrigðið sem verður sótt á valda staðsetningu og beindu notandanum á færsluskjáinn. (Þessi aðgerð er ekki í boði þegar valin staðsetning er dreifingarmiðstöð.) |
| Senda afurð         | Búðu til pöntun viðskiptavinar fyrir afurðarfbrigðið sem verður sent á valda staðsetningu og beindu notandanum á færsluskjáinn. |
| Framboð         | Sýna ATP-upplýsingar fyrir valdar samsetningar afbrigða fyrir valda staðsetningu. |
| Sýna allar staðsetningar   | Skiptu yfir í staðlað uppflettingaryfirlit birgða og auðkenndu upplýsingar um birgðaframboð á vöruafbrigðinu yfir allar verslanir í flokki verslanastaðsetjara og einnig í dreifingarmiðstöðvum af gerðinni **Staðall/Sjálfgefið**. |
| Skoða upplýsingar um afurð | Beindu notandanum á síðuna **Afurðarupplýsingar** á tengdu afurðarsniðmáti. |
