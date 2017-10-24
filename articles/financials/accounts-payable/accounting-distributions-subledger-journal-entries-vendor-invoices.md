---
title: "Dreifing á fjárhagsupphæð og færslur færslubókar undirfjárhags fyrir reikningur lánardrottins"
description: "Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig kostnaður, skatta eða gjöld verður að teknir með á reikningi lánardrottins. Hvert upphæð sem verður að vera teknir með þegar reikningur lánardrottins er skráð mun hafa eina eða fleiri dreifingar á fjárhagsupphæð."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f8169c32dc47c1635f6d3d00852d14d677678868
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a>Dreifing á fjárhagsupphæð og færslur færslubókar undirfjárhags fyrir reikningur lánardrottins

[!include[banner](../includes/banner.md)]


Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig kostnaður, skatta eða gjöld verður að teknir með á reikningi lánardrottins. Hvert upphæð sem verður að vera teknir með þegar reikningur lánardrottins er skráð mun hafa eina eða fleiri dreifingar á fjárhagsupphæð. 

<a name="accounting-distributions"></a>Dreifing á fjárhagsupphæðum 
-------------------------

Hægt er að nota eftirfarandi hnappanna í   síðunni reikningur lánardrottins til að skoða og mögulega breyta, dreifingar á fjárhagsupphæð síða fyrir hverja upphæð á reikningi lánardrottins.
-   **Dreifa fjárhæðir** - Skoða og breyta þeim dreifing á fjárhagsupphæð fyrir einstakar línur og allar  undirlínur, svo sem skatta eða gjöld. Einnig er hægt að skoða og breyta dreifingar á fjárhagsupphæð fyrir línu undirstig beint í frá síðunni VSK-færsla eða síðunni Gjaldfærslur.
    -   Breyta upphæðum í haus lánardrottnareiknings, svo sem gjöldum eða sléttuðum gjaldeyrisupphæðum.
    -   Breyta línuupphæðum lánardrottnareikninga.
-   **Skoða dreifingu** - Skoða dreifingu á fjárhagsupphæð fyrir allar línur skjals. Ekki er hægt að breyta dreifingu fjárhagsupphæða í þessu yfirliti.
    -   Skoða hausupplýsingar og línuupphæðir.

Ef lánardrottinsreikningnum vísar til innkaupapöntunar, er hægt að skipta og breyta dreifingar á fjárhagsupphæð fyrir línur sem innihalda vörur sem ekki eru í birgðum. Ef reikningslínu lánardrottinsins tilvísun til innkaupapöntunarlínu, er einnig hægt að eyða fjárhagsupphæð. Ekki er hægt að skipta eða eyða línum fyrir gjöld, skatt, og línuafslætti. Hægt er að breyta fjárhagslyklinum, en ekki er hægt að breyta upphæðum eða prósentum.
> [!NOTE]                                                                                                                                 
> Ef yfirlínu inniheldur vöru sem er ekki í birgðum og fjárhagsupphæð skipt, undirstig verður að skipta línunni sjálfkrafa til að jafna fjárhagsvíddir yfirlínu. Dreifingar á fjárhagsupphæð fyrir línu undirstig getur ekki auk skipta eða eytt, en eftir uppsetningu á undirstig línu, gæti verið hægt að breyta fjárhagslykil fyrir fjárhagsupphæð undirstig línu.

## <a name="distributing-amounts"></a>Dreifing upphæða
Þegar reikningur lánardrottins verður hverri upphæð dreift á eftirfarandi hátt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Gerð reikningslínu lánardrottins</th>
<th>Forgangsröð sem ákvarðar hvaðan aðallykill er birtur</th>
<th>Forgangsröð sem ákvarðar hvaða fjárhagsvídd sjálfgefna er birt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Afurð í birgðum</td>
<td><ol>
<li>Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna.</li>
<li>Svæði aðallykils þegar útgjöld Innkaupa fyrir afurð er valinn í Bókunarsíðu.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda á reikningi lánardrottins.</li>
</ol></td>
</tr>
<tr class="even">
<td>Innkaupategund eða afurð sem er ekki í birgðum</td>
<td><ol>
<li>Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínu lánardrottinsins vísar í innkaupapöntunarlínu.</li>
<li>Svæði aðallykils þegar útgjöld Innkaupa fyrir kostnaður er valinn í Bókunarsíðu.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda á reikningi lánardrottins.</li>
<li>Nota fjárhagsvíddargildi reikningslínu lánardrottins.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Eign</td>
<td><ol>
<li>Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínu lánardrottinsins vísar í innkaupapöntunarlínu.</li>
<li>Ef Kaup er valinn í svæðinu gerð Færslu í skjámyndinni reikningur Lánardrottins, er svæði aðallykils þegar Kaup eru valdar merktur í síðan bókunarregla eigna.</li>
<li>Ef leiðrétting kaupa er valinn í svæðinu gerð Færslu í skjámyndinni reikningur Lánardrottins, er svæði aðallykils þegar leiðrétting kaupa eru valdar merktur í síðan bókunarregla eigna.</li>
</ol></td>
<td><ol>
<li>Nota lykilsdreifingar fyrir innkaupapöntunarlínu, ef reikningslínan vísar í innkaupapöntunarlínu.</li>
<li>Nota fjárhagsvíddargildi reikningslínu lánardrottins.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</li>
</ol></td>
</tr>
<tr class="even">
<td>Verk sem eru skilgreind í reikningslínu lánardrottins</td>
<td><ol>
<li>Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</li>
<li>Ef Staða er valin í Bókunarkostnað - vörusvæði í síðunni verkflokkur, er svæðið aðallykill þegar Kostnaður er valinn í síðunni uppsetning fjárhagsbókunar.</li>
<li>Ef hagnaður og tap er valin í Bókunarkostnað - vörusvæði í síðunni verkflokkur, er svæðið aðallykill þegar kostnaður - afurð er valinn í síðunni uppsetning fjárhagsbókunar.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Línuafsláttur</td>
<td><ol>
<li>Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</li>
<li>Svæði aðallykils þegar afsláttur er valinn í Bókunarsíðu.</li>
<li>Ef aðallykill fyrir afslátt er ekki skilgreint í bókunarreglu, dreifing á fjárhagsupphæð heildarverðs á innkaupapöntunarlínunni.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna.</li>
<li>Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</li>
<li>Nota gildi fjárhagsvídda fyrir reikningslínu lánardrottins.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</li>
</ol></td>
</tr>
<tr class="even">
<td>Innkaup, gjald fært inn í verð og afsláttur flipi innkaupapöntunarlínunnar</td>
<td><ol>
<li>Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</li>
<li>Dreifing á fjárhagsupphæð útvíkkað verð á innkaupapöntunarlínunni.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Línugjald</td>
<td><ol>
<li>Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</li>
<li>Ef fjárhagslykillinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði debet Lykils í síðunni gjaldakóðar.</li>
<li>Ef afurð er valin í reitnum gerð debets í    skjámyndina gjaldakóðar, dreifing á fjárhagsupphæð fyrir heildarverð á innkaupapöntunarlínunni.</li>
<li>Ef viðskiptavinur/lánardrottinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði kredit Lykils í síðunni gjaldakóðar.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</li>
<li>Nota fjárhagsvíddargildi reikningslínu lánardrottins.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</li>
</ol></td>
</tr>
<tr class="even">
<td>Skattur, með eftirfarandi skilyrði:
<ul>
<li>valkosturinn beita BNA skattlagningarreglum er valinn á síðunni færibreytur fjárhags.</li>
</ul></td>
<td><ol>
<li>Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</li>
<li>Dreifing á fjárhagsupphæð heildarverð eða gjöldum.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</li>
<li>Nota fjárhagsvíddargildi reikningslínu lánardrottins.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Skattur, með eftirfarandi skilyrðum:
<ul>
<li>Valkosturinn beita BNA skattlagningarreglum er hreinsaður á síðunni færibreytur fjárhags.</li>
<li>svæðið neysluskattur fyrir VSK-flokkur er hreinsaður á síðunni vsk-flokka.</li>
</ul></td>
<td><ol>
<li>Ef skattupphæðin er endurkræf, svæðið VSK-kröfur í í síðunni fjárhagsbókunarflokkar.</li>
<li>Ef skattupphæðin er endurkræf, útvíkkað verð eða dreifing á fjárhagsupphæð fyrir gjald.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Nota fjárhagsvíddir úr útvíkkað verð eða dreifingar á fjárhagsupphæð fyrir gjald á reikningslínu lánardrottins.</li>
<li>Nota fjárhagsvíddargildi reikningslínu lánardrottins.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</li>
</ol></td>
</tr>
<tr class="even">
<td>Skattur, með eftirfarandi skilyrðum:
<ul>
<li>Valkosturinn beita BNA skattlagningarreglum er hreinsaður á síðunni færibreytur fjárhags.</li>
<li>neysluskattur svæði fyrir VSK-flokkur er valið í síðu VSK-flokkur.</li>
</ul></td>
<td><ol>
<li>Ef skattupphæðin er endurkræf, svæðið VSK-kröfur í í síðunni fjárhagsbókunarflokkar.</li>
<li>Ef skattupphæðin er ekki endurkræf, svæði útgjöld neysluskatts í síðunni fjárhagsbókunarflokkar.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Nota fjárhagsvíddir úr útvíkkað verð eða dreifingar á fjárhagsupphæð fyrir gjald á reikningslínu lánardrottins.</li>
<li>Nota fjárhagsvíddargildi reikningslínu lánardrottins.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Gjald hauss</td>
<td><ol>
<li>Ef fjárhagslykillinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði debet Lykils í síðunni gjaldakóðar.</li>
<li>Ef viðskiptavinur/lánardrottinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði kredit Lykils í síðunni gjaldakóðar.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</li>
<li>Nota sjálfgefin sniðmátsgildi fjárhagsvídda úr reikningshaus lánardrottins.</li>
<li>Nota fjárhagsvíddargildi reikningslínu lánardrottins.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</li>
</ol></td>
</tr>
<tr class="even">
<td>Haus afsláttur</td>
<td><ol>
<li>Svæði aðallykils fyrir bókunargerð fyrir afslátt reikningur lánardrottins í lyklar fyrir síðuna sjálfvirk færsla.</li>
</ol></td>
<td><ol>
<li>Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</li>
<li>Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</li>
<li>Nota fjárhagsvíddargildi reikningslínu lánardrottins.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</li>
</ol></td>
</tr>
</tbody>
</table>

 
<a name="distributing-taxes"></a>Dreifing skatta
------------------

Ekki er hægt að stofna dreifingu á fjárhagsupphæð fyrr en skattar hafa verið reiknaðir. Til að reikna virðisaukaskatt, verður að ljúka eitt af eftirtöldum verkefnum í síðunni reikningur lánardrottins.
-   Skoða samtölu reiknings.
-   Skoða VSK.
-   Skoða færslubók undirfjárhags.
-   Skoða dreifingar á fjárhagsupphæð fyrir reikning lánardrottins sem er lokið.
-   Setja reikningur lánardrottins í bið.
-   Bóka reikning lánardrottins.

## <a name="subledger-journals-for-vendor-invoices"></a>Færslubækur undirfjárhags fyrir reikninga lánardrottins
Áður en reikningur lánardrottins er bókaður, er hægt að skoða alla lykilfærslu reiknings, þar á meðal debet- og kreditsniði, til að staðfesta sem reikningurinn er bókuð á rétta lykla. Þetta yfirlit yfir alla lykilfærslu kallast færslubók undirfjárhags. 

Ef færsla í undirbók er röng þegar hún er forskoðuð áður en reikningur lánardrottins eru skráðar, er hægt að breyta færslu í undirbók. Þess í stað verður þú að breyta dreifingu á fjárhagsupphæð eða bókunarreglu. Fjárhagsupphæðum er notuð til að skilgreina einni hlið lykilfærslu, debet eða kredit. Mótfærslu lykilfærslu undirbókarlykils er stofnuð með því að nota bókunarreglur, eins og úr lykli lánardrottins eða skatts.






