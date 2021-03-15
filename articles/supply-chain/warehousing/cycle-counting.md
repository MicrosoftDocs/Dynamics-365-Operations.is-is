---
title: Regluleg talning
description: Þessi grein lýsir hvernig nota má reglulega talningu með vöruhúsalausn sem er tiltæk í vöruhúsakerfi. Þessi grein á ekki við um vöruhúsalausn sem er tiltæk í birgðastjórnun.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca5ae06a2a6cbe410fadf464bc49071122d0342b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973811"
---
# <a name="cycle-counting"></a>Regluleg talning

[!include [banner](../includes/banner.md)]

Þessi grein lýsir hvernig nota má reglulega talningu með vöruhúsalausn sem er tiltæk í vöruhúsakerfi. Þessi grein á ekki við um vöruhúsalausn sem er tiltæk í birgðastjórnun.

Reglulega talningu er vöruhúsið ferli sem hægt er að nota til að endurskoða vörur á lager. Hægt er að lýsa reglulegri talningu í þremur áföngum:

1.  **Stofna reglulega talningu vinnu** ─ Reglulega talningu vinna er stofnuð sjálfkrafa samkvæmt færibreytum þröskuld fyrir vörur eða með því að nota við áætlun um reglulega talningu. Einnig er hægt að stofna reglulega talningu vinnu handvirkt með því að nota færibreytur vöru eða vöruhúss á síðunni **Vinna reglulegrar talningar eftir vörum** eða á síðunni **Vinna reglulegrar talningar eftir staðsetningu**.
2.  **Ferli reglulegrar talningar** ─ Eftir að hafa stofnað vinnu reglulegrar talningar er framkvæmd vinna reglulegrar talningar með því að telja vörur á staðsetningu vöruhúss og færa inn niðurstöðu í Dynamics 365 Supply Chain Management með fartæki. Að öðrum kosti er hægt að telja vörur í vöruhús án þess að stofna reglulega talningu á vinnu. Þetta ferli kallast *finna reglulega talningu*.
3.  **Leysa mismun í talningargildi** - Eftir reglulega talningu, munu allar vörur sem hafa mismunandi talningargildi hafa stöðuna **Bíður yfirferðar** í skjámyndinni **Allt**. Hægt er að leysa úr þessum mismun á síðunni **Vinna reglulegrar talningar bíður yfirferðar**.

Eftirfarandi mynd sýnir hvernig á að framkvæma reglulega talningu. ![Vinnsluflæði fyrir reglulega talningu](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Skilyrði fyrir reglulega talningu
Eftirfarandi tafla sýnir skilyrði sem verða að vera til staðar áður en byrjað er á reglulegri talningu.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skilyrði</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vara</td>
<td>Varan verður að vera virkur fyrir vöruhúsakerfisferli.</td>
</tr>
<tr class="even">
<td>Vöruhús</td>
<td>Vöruhús verður að vera virkur fyrir vöruhúsakerfisferli. Til að virkja vöruhús fyrir vöruhúsakerfisferli, skal velja vöruhús í skjámyndinni <strong>Vöruhús</strong> og velja síðan valkostinn <strong>Nota vöruhúsakerfisferli</strong>. Þar að auki, ef óskað er að virkja starfsmenn til tilfærslu bretta við reglulega talningu, á flýtiflipanum <strong>Vöruhúsakerfi</strong>, veljið valkostinn <strong>Leyfa tilfærslu bretta við reglulega talningu</strong>.</td>
</tr>
<tr class="odd">
<td>Vinnuhópar</td>
<td>Valfrjálst: Stofna vinnuhóp til að aðgreina vöruhúsavinnu, byggt á gerð vinnu (í þessu tilfelli, vinnu reglulegrar talningar).</td>
</tr>
<tr class="even">
<td>Staðsetningar</td>
<td>Virkja reglulega talningu fyrir staðsetningar. Í skjámyndinni <strong>Staðsetningarsnið</strong> velurðu valkostinn <strong>Leyfa reglulega talningu</strong> til að leyfa reglulega talningu fyrir vöruhúsið.</td>
</tr>
<tr class="odd">
<td>Færibreytur vöruhúsakerfis</td>
<td>Setja upp færibreytur fyrir reglulega talningu. Í skjámyndinni <strong>Færibreytur vöruhúsakerfis</strong> tilgreinirðu sjálfgefna gerð aðlögunarkóða, auðkenni vinnuklasa og vinnuforgang reglulegrar talningar.</td>
</tr>
<tr class="even">
<td>Fartæki</td>
<td><ul>
<li>Stofna valmyndaratriði fyrir eina af eftirfarandi aðferðum í skjámyndinni <strong>Valmyndaratriði fartækis</strong>:
<ul>
<li>Stýrt af staðfestum notanda reglulega talningu</li>
<li>Regluleg talning sem er stýrt af kerfi</li>
<li>Flokkun reglulegrar talningar</li>
<li>Regluleg stundartalning</li>
</ul>
</li>
<li>Setja upp valmynd fyrir fartæki.</li>
<li>Stofna reikning notanda og úthluta valmynd fartækis til notandakennis viðkomandi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tengd uppsetningarverk</td>
<td>Setja upp áætlun um reglulega talningu fyrir staðsetningu í vöruhúsinu.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Stofna reglulegu talninguna sjálfkrafa
Það eru tvær leiðir til að bóka endurtekna stofnun vinnu reglulegrar talningar: Setja upp reglulega talningarþröskulda eða setja upp áætlanir um reglulega talningu.

-   Þröskuldur reglulegrar talningar tilgreinir mörk magns eða prósentu birgðavara. Vinnu reglulegrar talningar er stofnuð sjálfkrafa þegar mörk þröskuldur er náð.
-   Áætlun um reglulega talningu er sett upp til að stofna vinnu reglulegrar talningar með reglulegu millibili gegnum runuvinnslu eða strax. Þegar regluleg talning er stofnuð inniheldur vinnulína talningar upplýsingar um staðsetningu sem á að telja. Birgðir á lager sem tengjast þessari staðsetningu eru ekki læstar og eru því tiltækar fyrir frátekningu og útleið vinnslu jafnvel þó að opin talningarvinna sé til staðar.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Stofna vinnu reglulegrar talningar á grundvelli þröskuld færibreytur fyrir vörur

Hægt er að stofna vinnu reglulegrar talningar þegar fjöldi vara fer niður fyrir tiltekið þröskuld gildi á ákveðinni staðsetningu. Til dæmis eru 60 vörur á staðsetningu þar sem reglulegur talningarþröskuldur er 40. Við sölupöntunarfærslu, eru 25 vörur teknar frá staðsetningu og settar inn í sviðsetningarstaðsetningu. Þar sem nýr fjöldi vörunnar, 35, er minna en magnþröskuldur er vinna reglulegrar talningar stofnuð sjálfkrafa fyrir staðsetningu.

### <a name="schedule-cycle-counting-work"></a>Áætla vinnu reglulegrar talningar

Hægt er að setja upp áætlun um reglulega talningu til að stofna vinnu reglulegrar talningar með reglulegu millibili eða strax. Með því að setja upp áætlanir um reglulega talningu er hægt að stýra vinnuhópi sem vinna reglulegrar talningar er stofnuð fyrir, hámarksfjölda reglulegrar talningar sem eru stofnaðar fyrir vörur á mismunandi stöðum og fjölda daga áður en staðsetning í vöruhúsi er talið aftur. Til dæmis er vara tiltæk í þremur staðsetningum í vöruhúsinu og hámarksfjöldi reglulegrar talningar er stillt á **2**. Í þessu tilfelli, þegar keyrð er áætlun um reglulega talningu eru tvær reglulegar talningarvinnur stofnaðar fyrir þær tvær staðsetningar þar sem varan er til staðar. Sem annað dæmi er fjöldi daga á milli reglulegrar talningar stilltur á **5**. Í þessu tilfelli er vinna reglulegrar talningar stofnuð á fimm daga fresti. Hins vegar ef unnið er úr vinnu reglulegrar talningar á degi 3 mun næsta reglulega talning stofnast fimm dögum eftir að síðasta reglulega talning var unnin, á degi 8.

## <a name="create-cycle-counting-work-manually"></a>Stofna vinnu reglulegrar talningar handvirkt
Til að stofna vinnu reglulegrar talningar handvirkt er hægt að nota síðurnar **Vinna reglulegrar talningar eftir vörum** eða **Vinna reglulegrar talningar eftir staðsetningu**. Hægt er að tilgreina hámarksfjölda reglulegrar talningar sem hægt er að stofna í hvert sinn. Til dæmis, ef vöruhússtjórinn tilgreinir gildið **5** er vinna reglulegrar talningar stofnuð fyrir fimm staðsetningar jafnvel þó að varan er til staðar í 10 mismunandi stöðum. Einnig er hægt að velja vinnuhópskenni til að úthluta þeim vinnukennum reglulegrar talningar sem eru stofnuð til. Þegar vinnuhópskenni er unnið fyrir reglulega talningu, er vinnukenni reglulegrar talningar sem úthlutað er þessum vinnuhópi unnið eins og hópur.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Framkvæma reglulegar talningar með fartæki
Það eru nokkrar aðferðir við reglulega talningu þegar Supply Chain Management er notað á fartæki:

-   **Stýrt af notanda** ─ starfsmaðurinn getur tilgreint Vinnukenni reglulegrar talningar sem er í stöðunni **Opið**.
-   **Stýrt af kerfi** - Supply Chain Management úthlutar starfsmanni auðkenni reglulegrar talningar.
-   **Flokkun reglulegrar talningar** ─ starfsmaðurinn getur flokkað saman vinnukenni reglulegrar talningar sem tengjast tiltekinni staðsetningu, svæði eða vinnuhóp.
-   **Regluleg stundartalning** ─ Starfsmaður getur talið vörur á vöruhúsi hvenær sem er án þess að skapa regluleg talningarvinnu. Til að framkvæma reglulega stundartalningu á staðsetningu, færir starfsmaðurinn inn staðsetningarauðkenni.

Eftirfarandi ferli er dæmi um hvernig hægt er að framkvæma reglulega stundartalningu með fartæki. Leiðbeiningar sem starfsmaðurinn sér á tækinu eru breytilegar, eftir uppsetningu valmyndaratriða fyrir reglulega stundartalningu.

1.  Á farsíma, velja valmyndaratriði til að keyra vinnslu reglulegrar stundatalningar.
2.  Skráið staðsetninguna þar sem á að framkvæma reglulega stundartalningu.
3.  Skrá og staðfesta vörunúmer og talið magn vörunnar. **Athugið:** Vinna reglulegrar talningar er uppfærð í annað hvort **Bíður yfirferðar**, eða **Lokað** á síðunni **Allt**, eftir þeim færibreytum sem eru settar upp í skjámyndinni **Starfsmaður**.
4.  Valfrjálst: Endurtaka þrep 3 fyrir þær vörur sem eru eftir á staðsetningunni og staðfesta að það eru engar frekari vörur tiltækar fyrir talningu.

## <a name="resolve-cycle-counting-differences"></a>Leysa úr mismun á reglulegri talningu.
Mismunur reglulegrar talningar kemur upp við eftirtaldar aðstæður ef valkosturinn **Er umsjónarmaður reglulegrar talningar** er stilltur á **Nei** fyrir vinnunotendakenni:

-   Talið gildi er ekki innan fráviksmarkanna sem eru tilgreind í skjámyndunum **Mörk Hámarkshlutfalls** eða **Mörk Hámarksmagns** á síðunni **Notendur**. Til dæmis, er magn á lager í staðsetningu 50 og fráviksmörk fyrir vinnunotanda er 10. Ef vinnu notandinn færir inn gildi sem er ekki á milli 40 og 60, munur á sér stað.
-   Talið gildi er frábrugðið magni á lager og það eru engin fráviksmörk sett.

Hægt er að leiðrétta mismun talningargilda og samþykkja talið gildið á síðunni **Regluleg talning bíður yfirferðar**. Endurskoðuð magntalning vörunnar getur verið staðfest á síðunni **Lagerstaða eftir staðsetningu**. Talið gildi er hafnað ef ekki er hægt að samþykkja mismun.

## <a name="additional-resources"></a>Frekari upplýsingar
[Uppsetning fartækja fyrir vöruhúsavinnu](configure-mobile-devices-warehouse.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]