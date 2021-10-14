---
title: Uppsetning gilda fyrir kostnaðarfæribreytu
description: Þegar sett er upp eining heildarkostnaðar er hægt að skilgreina nokkur sett af algengum gildum sem verða í boði þegar ákveðnar gerðir af gildum kostnaðarfæribreyta eru valdar í öðrum hlutum forritsins. Í þessu efnisatriði er útskýrt hvernig á að setja upp þessi sett af gildum.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1bcce7af0a15add63f1d9c3b32563de0ab6698bd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577649"
---
# <a name="costing-parameter-values-setup"></a>Uppsetning gilda fyrir kostnaðarfæribreytu

[!include [banner](../../includes/banner.md)]

Þegar einingin **Heildarkostnaður** er sett upp er hægt að skilgreina ýmis sett af algengum gildum og tengdar stillingar fyrir hvert gildi. Þessi gildi verða þá tiltæk þegar valdar eru tilteknar gerðir af gildum kostnaðarfæribreyta í öðrum hlutum forritsins. Í þessu efnisatriði er útskýrt hvernig á að setja upp þessi sett af gildum.

## <a name="set-up-cost-type-codes"></a>Hvernig á að setja upp kóða kostnaðargerðar

Kóðar kostnaðargerðar ákvarða gerð kostnaðar sem myndast þegar vörurnar eru komnar inn í vöruhúsið eða heildarkostnað leiðar. Þó þeir auka yfirleitt virði varanna er einnig hægt að nota þá til að safna upp upphæðum í fjárhag. Fjárhagsleiðréttingar eru notaðar þegar kostnaði er safnað upp yfir tíma eða fyrir nokkrar ferðir í röð og jafnaður í einni færslu.

> [!NOTE]
> Ef taflan kostnaðargerðar er samnýtt á milli lögaðila þarf einnig að deila bókhaldslyklinum á milli lögaðila. Annars virkar bókunarfærslurnar ekki rétt.

Til að setja upp kóða kostnaðargerða skal fara í **Heildarkostnaður \> Kostnaðaruppsetning \> Kóðar kostnaðargerðar**. Hægt er að nota hnappana á aðgerðasvæðinu til að stofna nýja kostnaðargerðarkóða, breyta tiltækum kóðum eða eyða valinni kostnaðargerð.

Eftirfarandi tafla lýsir reitunum sem eru tiltækir fyrir hvern kóða kostnaðargerðar.

| Svæði | lýsing |
|---|---|
| Kostnaðargerðarkóði | Færa inn heiti fyrir kóða kostnaðargerðar. |
| lýsing | Færa inn lýsingu á kóða kostnaðargerðar. |
| Nota flutningstaxta | Stillið þennan valkost á *Já* ef gengi ferðar (stundum vísað í sem stjórnunargengi) verður að vera notað til að reikna út gildi fyrir þennan kostnað. Í þessu tilviki verður flutningstaxtinn notaður í staðinn fyrir hefðbundið sjálfgefið stundargengi til að skipta reikningum erlendra gjaldmiðla. |
| Skýrslugerðarflokkur | Í þessum reit kemur fram skýrslugerðarflokkur fyrir kostnaðargerðina. Hægt er að prenta skýrslur annaðhvort út frá skýrsluflokkum eða eftir kostnaðargerð. |
| Debet gerð | Veljið hvort kostnaðargerðin eigi að debetfæra vöruna, fjárhagslykilinn eða lánardrottin. |
| Debet bókun | Ef reiturinn **Debetgerð** er stilltur á *Fjárhagslykil* skal velja bókunarlýsinguna. |
| Debetreikningur | Ef reiturinn **Debetgerð** er stilltur á *Fjárhagslykil* skal velja fjárhagslykilinn sem á að nota. |
| Kredit gerð | Veljið hvort þessi kostnaðargerð eigi að kreditfæra vöruna, fjárhagslykilinn eða lánardrottinn. |
| Kredit bókun | Ef reiturinn **Kreditgerð** er stilltur á *Fjárhagslykil* skal velja bókunarlýsinguna. |
| Kreditreikningur | Ef reiturinn **Kreditgerð** er stilltur á *Fjárhagslykil* skal velja fjárhagslykilinn sem á að nota. |
| Millireikningur | Veljið millireikninginn fyrir kostnaðargerðina. Mælt er með því að tilgreindur sé sérstakur millireikningur fyrir hverja kostnaðargerð til að aðstoða við afstemmingu. |
| Bókunargerð staðlaðs kostnaðar | Ef staðlur kostnaður er notaður skal velja bókunarlýsinguna. |
| Fráviksreikningur staðalkostnaðar | <p>Ef staðlað kostnaðarverð er notað verður lykillinn sem tilgreindur er hér notaður til að bóka öll frávik. Þessi lykill notar sundurliðun heildarkostnaðar á síðunni **Vöruverð**. Þessi sundurliðun er búin til með því að nota reglubundna uppfærslu á verðum.</p><p>Til dæmis er staðlaður kostnaður vöru $15,00, FOB er $13,00 og farmurinn er $2,00. Þegar tekið er við reikningi fyrir birgðirnar, er varan móttekin á $15,00, en það er staðlað verðfrávik upp á $2,00 fyrir vöruna vegna þess að raunverulegt FOB er $13,00. Þetta frávik er bókað á lykli staðlaðs verðfráviks sem er settur upp í bókunarreglu vörunnar. Þar sem áætlaður farmur er $2,00 er ekkert frávik þegar birgðareikningur er bókaður. Þegar reikningur fyrir farminn er móttekin er farmurinn hins vegar $2,50 á einingu. Þess vegna er $0,50 frávik bókað á tilgreindan kostnað. |
| Hlaupandi meðaltal fráviksreiknings | <p>Ef kostnaður hlaupandi meðaltals er notað verður lykillinn sem tilgreindur er hér notaður til að bóka öll frávik.</p><p>Til dæmis er áætlaður farmur $2,00. Þegar reikningur fyrir farminn er móttekin er farmurinn hins vegar $2,50 á einingu. Því verður að bóka $0,50 frávik.</p><p>Þegar valkosturinn **Bóka leiðréttingar sem frávik** er stilltur á *Já* á síðunni **Færibreytur heildarkostnaðar** verða öll frávik á milli áætlaðs og raunverulegs sendingarkostnaðar bókuð á frávikslykil hlaupandi meðaltals sem er tilgreindur hér. Þegar valkosturinn **Bóka leiðréttingar sem frávik** er stilltur á *Nei* verður venjuleg virkni notuð og frávikið verður sett annaðhvort á birgðir eða frávikslykil hlaupandi meðaltals sem er tilgreint hér, en það fer eftir lagerbirgðum.</p> |
| Gjaldauppsöfnunarlykill | Veljið lykilinn sem er notaður til að safna upp fyrir kostnaðarmati þegar innkaupareikningurinn er bókaður. Þessi reitur er aðeins notaður þegar valkosturinn **Nota gjaldauppsöfnunarlykil kostnaðargerðar** er stilltur á *Já* í flýtiflipanum **Kostnaðarútreikningur** í flipanum **Almennt** á síðunni **Færibreytur heildarkostnaðar**. |
| Gjaldalykill | Veljið lykilinn sem er notaður til að sækja flutningskostnað á innleið sem hefur verið reikningsfærður af birgi. Upphæðin er bókuð sem debet. Mótlykillinn er frávikslykill birgða. Þessi valkostur er aðeins notaður þegar valkosturinn **Bóka á gjaldalykil í fjárhag** er stilltur á *Já* á síðunni **Færibreytur viðskiptaskulda**. |
| Fráviksreikningur | Lykillinn sem verður notaður til að jafna uppsafnaðan kostnað þegar innkaupareikningurinn er bókaður. Þessi reitur er aðeins notaður þegar valkosturinn **Nota gjaldauppsöfnunarlykil kostnaðargerðar** er stilltur á *Já* í flýtiflipanum **Kostnaðarútreikningur** í flipanum **Almennt** á síðunni **Færibreytur heildarkostnaðar**. |

## <a name="vendor-cost-type-groups"></a>Flokkar kostnaðargerða lánardrottins

Kostnaðargerðarflokkar lánardrottins hjálpa til við að finna út gjöld *sjálfvirks kostnaðar* og leggja þau á ferð. Lánardrottnar sem hafa svipaðan innflutningskostnað eru tengdir saman. Til dæmis greiða lánardrottnar frá vaxandi mörkuðum sömu prósentu innkaupagjalds fyrir sömu tegund afurðar sem er keypt af rótgrónum markaði.

Hægt er að vinna með kostnaðargerðarflokka með því að fara í **Heildarkostnaður \> Kostnaðaruppsetning \> Kostnaðargerðarflokkar lánardrottins**. Síðan **Kostnaðargerðarflokkar lánardrottins** býður upp á hnitanet sem sýnir lista yfir alla núgildandi kostnaðargerðarflokka lánardrottins. Hægt er að nota hnappana í aðgerðarúðunni til að bæta við, fjarlægja og breyta línum í töflunni.

Eftirfarandi tafla lýsir reitum sem eru tiltækir í hverri línu í töflunni.

| Svæði | lýsing |
|---|---|
| Flokkar kostnaðargerða lánardrottins | Færið inn einkvæmt heiti fyrir kostnaðargerðarflokk lánardrottins (t.d. *Rótgrónir markaðir*). |
| lýsing | Færið inn lýsingu á hópnum fyrir kostnaðargerð lánardrottins. Þessi lýsing getur gefið upplýsingar um stigið eða gerð gjaldsins sem tengist lánardrottnaflokki. |

## <a name="item-cost-type-groups"></a>Flokkar kostnaðargerðar fyrir vörur

Kostnaðargerðarflokkar vöru hjálpa til við að finna út gjöld *sjálfvirks kostnaðar* og leggja þau á ferð. Svipaðar vörur eru tengdar saman. Til dæmis geta allar vörur sem eru með 5 prósenta toll tilheyrt tilteknum flokki kostnaðargerða.

Hægt er að vinna með kostnaðargerðarflokka vöru með því að fara í **Heildarkostnaður \> Kostnaðaruppsetning \> Kostnaðargerðarflokkar vöru**. Síðan **Kostnaðargerðarflokkar vöru** býður upp á hnitanet sem sýnir lista yfir alla núgildandi kostnaðargerðarflokka vöru. Hægt er að nota hnappana í aðgerðarúðunni til að bæta við, fjarlægja og breyta línum í töflunni.

Eftirfarandi tafla lýsir reitum sem eru tiltækir í hverri línu í töflunni.

| Svæði | lýsing |
|---|---|
| Flokkar kostnaðargerðar fyrir vörur | Færið inn einkvæmt heiti fyrir kostnaðargerðar vöru (svo sem *Tollur 5%*). |
| lýsing | Færið inn lýsingu á kostnaðargerðarflokki vöru. Þessi lýsing getur gefið upplýsingar um stigið eða gerð gjaldsins sem tengist vöruflokknum. |

> [!NOTE]
> Kostnaðargerð vörunnar er tengd við vöruna í gegnum reitinn **Kostnaðargerðarflokkur** í flýtiflipanum **Innkaup** á vörusíðunni **Útgefin afurð**.

## <a name="transfer-order-cost-type-groups"></a>Flokkar kostnaðargerðar flutningspöntunar

Kostnaðargerðarflokkar flutningspöntunar hjálpa til við að finna út gjöld *sjálfvirks kostnaðar*. Svipaðar vörur eru tengdar saman. Til dæmis geta allar vörur sem eru með 7 prósenta toll tilheyrt tilteknum flokki kostnaðargerða.

Hægt er að vinna með kostnaðargerðarflokka flutningspöntunar með því að fara í **Heildarkostnaður \> Kostnaðaruppsetning \> Kostnaðargerðarflokkar flutningspöntunar**. Síðan **Kostnaðargerðarflokkar flutningspöntunar** býður upp á hnitanet sem sýnir lista yfir alla núgildandi kostnaðargerðarflokka flutningspöntunar. Hægt er að nota hnappana í aðgerðarúðunni til að bæta við, fjarlægja og breyta línum í töflunni.

Eftirfarandi tafla lýsir stillingum sem eru tiltækir í hverri línu í töflunni.

| Svæði | lýsing |
|---|---|
| Flokkar kostnaðargerðar flutningspöntunar | Færið inn einkvæmt heiti fyrir kostnaðargerð flutningspöntunar vöru (svo sem *Tollur 7%*). |
| lýsing | Færið inn lýsingu á kostnaðargerðarflokki flutningspöntunar. Þessi lýsing getur gefið upplýsingar um stigið eða gerð gjaldsins sem tengist flokki kostnaðargerðar flutningspöntunar. |

> [!NOTE]
> Kostnaðargerð flutningspöntunar er tengd við vöruna í gegnum reitinn **Kostnaðargerðarflokkur flutningspöntunar** í flýtiflipanum **Innkaup** á vörusíðunni **Útgefin afurð**.

## <a name="cost-templates"></a>Kostnaðarsniðmát

Kostnaðarsniðmát er notað til að stilla sjálfgildi fyrir stillingar sem notendur sem eru að fá kostnaðarmatið vita hugsanlega ekki um. Kostnaðarsniðmát geta dregið úr flækjum í matsferlinu með því lágmarka valkostina sem notendur verða að velja til að fá nákvæmt mat.

Til að vinna með kostnaðarsniðmát skal fara í **Heildarkostnaður \> Kostnaðaruppsetning \> Kostnaðarsniðmát**. Á síðunni **kostnaðarsniðmát** sýnir listasvæðið vinstra megin öll kostnaðarsniðmát. Hægt er að nota hnappana í aðgerðarúðunni til að bæta við, fjarlægja og breyta sniðmátum.

Eftirfarandi tafla lýsir stillingunum sem eru tiltækar fyrir hvert sniðmát.

| Svæði | lýsing |
|---|---|
| Kostnaðarsniðmát | Færið inn einkvæmt heiti fyrir kostnaðarsniðmátið. Heitið lýsir venjulega stuðlinum eða kostnaðarmargfaldara fyrir sniðmátið. |
| lýsing | Færa inn lýsingu á kostnaðarsniðmátinu. |
| Flutningsfyrirtæki | Veljið lánardrottnalykil flutningsfyrirtækisins sem tengja á við kostnaðarsniðmátið. |
| Afhendingarmáti | Veljið afhendingarmáta sem kostnaðarsniðmátið á að nota þegar áætlaður kostnaður vöru er reiknaður. Þessi reitur hjálpar til við að ákvarða sjálfvirkan kostnað sem tengist vörum í kostnaðarmatinu. |
| Gámagerð | Veljið gerð gámategundar til að tengja við kostnaðarsniðmátið. Þessi reitur hjálpar til við að ákvarða sjálfvirkan kostnað sem tengist vörum í kostnaðarmatinu. |
| Tollmiðlari | Veljið tollmiðlara (lánardrottinn) til að tengja við kostnaðarsniðmátið. Þessi reitur hjálpar til við að ákvarða sjálfvirkan kostnað sem tengist kostnaðarmatinu. |
| Stuðull | Færið inn stuðul sem á að nota fyrir endanleg kostnaðarmat á vörum. Til að bæta til dæmis 10 prósentum við reiknaða kostnaðarmatið skal slá inn *1,10*. |

## <a name="volumetric-divisors"></a>Deilar rúmmálsmælinga

Deilar rúmmálsmælinga eru notaðir til að reikna út rúmmálsþyngdina. Hvert flutningafyrirtæki notar sýna eigin deila rúmmálsmælinga. Auk þess fara deilar fyrirtækisins yfirleitt eftir því hver flutningsmátinn er. Til dæmis eru flutningar loftleiðis og sjóleiðis oft og tíðum með mismunandi deila. Fyrirtæki getur einnig gert reglurnar flóknari, allt eftir því hvaðan sendingin kemur.

Til dæmis er pakki sem er sendur með flugvél 3 rúmmetrar (m³). Fyrirtækið rukkar eftir rúmmálsþyngd og notar deili rúmmálsmælingar upp á 6. Þessi deilir er margfaldaður með rúmmálinu til að finna út rúmmálsþyngdina. Þess vegna er rúmmálsþyngdin fyrir þetta dæmi 3 x 6 = 18 kílógrömm (kg).

Til að setja upp deili rúmmálsmælinga skal fara í **Heildarkostnaður \> Kostnaðaruppsetning \> Deilar rúmmálsmælinga**. Síðan **Deilar rúmmálsmælinga** sýnir hnitanet með lista yfir alla núgildandi deila rúmmálsmælinga. Hægt er að nota hnappana í aðgerðarúðunni til að bæta við, fjarlægja og breyta línum í töflunni.

Eftirfarandi tafla lýsir reitum sem eru tiltækir í hverri línu í töflunni.

| Svæði | lýsing |
|---|---|
| Flutningsfyrirtæki | Veljið lánardrottnalykil flutningsfyrirtækisins sem tengist rúmmálsdeili. |
| Kostnaðargerðarkóði | Veljið kóða kostnaðargerðar sem tengist deili rúmmálsmælingar. Notið þennan reit til að setja kostnaðargerðir inn í skýrslugerðarramma. Hægt er að prenta skýrslur annaðhvort út frá skýrsluflokkum eða eftir kostnaðargerð. |
| Frá höfn | Veljið „frá“ höfn sem deilir rúmmálsmælingar á við um. |
| Deilir rúmmálsmælingar | Færið inn gildi fyrir deili rúmmálsmælingar sem á við um línuna. Gildið sem fært er inn verður *margfaldað* með rúmmáli hvers pakka til að ákvarða rúmmálsþyngd pakkningarinnar. |
