---
title: Hvernig set ég upp afstemmingu fjárhagsvídda?
description: Þessi grein lýsir valkostum til að setja upp og nota eiginleikann Jöfnun fjárhagsvíddar.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: dd859629b0eb9f14fa4907699613382f3897d21d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878013"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Hvernig set ég upp afstemmingu fjárhagsvídda?

[!include [banner](../includes/banner.md)]

Þessi grein lýsir valkostum til að setja upp og nota eiginleikann Jöfnun fjárhagsvíddar.

## <a name="symptom"></a>Einkenni

Valkostirnir eru tveir til að setja upp jöfnunarfjárhagsvíddir. Fyrsti valkosturinn er að nota reitinn **Jöfnunarfjárhagsvídd** á uppsetningarsíðunni **Fjárhagur** (**Fjárhagur \> Uppsetning fjárhags \> Fjárhagur**). Annar valkosturinn er að nota reitinn **Fara fram á að víddin sé jöfnuð** á síðunni **Fjárhagsvíddir** (**Fjárhagur \> Víddir \> Fjárhagsvíddir**). Þessi grein útskýrir muninn á þessum tveimur valkostum.

## <a name="resolution"></a>Upplausn

Stofnanir/fyrirtæki nota yfirleitt jöfnunarvíddir til að búa til efnahagsreikning sem er jafnaður við fjárhagsvíddarstigið. Með því að virkja annan hvorn eiginleikann er ekki hægt að jafna birtar, ójafnaðar víddir. Fyrst þarf að slá inn stillifærslur handvirkt til að jafna efnahagsreikninginn áður en annar hvor eiginleikinn er virkjaður.

Valkostirnir tveir útiloka hvorn annan. Valkosturinn sem stofnunin notar ætti að vera byggður á viðskiptakröfum þínum. Við heyrum oft af viðskiptavinum sem skilgreina jöfnunarvíddina bæði í fjárhagsuppsetningu og uppsetningu fjárhagsvíddar og ljúka síðan við einhverja eða allar viðbótaruppsetningar sem krafist er. Þeir geta þó enn ekki birt vegna ójafnvægis á fjárhagsvíddarstigi.

Eftirfarandi hlutar lýsa valkostunum tveimur og útskýra hvernig á að setja þá upp.

### <a name="ledger--balancing-financial-dimension"></a>Fjárhagur – Jöfnunarfjárhagsvídd

Jöfnunarvíddin á uppsetningarsíðunni **Fjárhagur** er notuð til að virkja millieiningabókhald. Fylgdu þessum skrefum til að kveikja á virkni.

1. Ákveða hvaða fjárhagsvídd verður jöfnunarvíddin.

    - Þessi virkni gerir þér kleift að velja aðeins eina fjárhagsvídd sem jöfnunarvídd.
    - Ekki velja enn víddina á uppsetningarsíðunni **Fjárhagur**.
    - Gakktu úr skugga um að efnahagsreikningur þinn sé þegar jafnaður fyrir valda fjárhagsvídd.

2. Uppfæra lykilskipulagið fyrir fjárhagsvídd jöfnunar.

    - Jöfnunarfjárhagsvíddin verður að vera með í öllu lykilskipulagi sem tengist fjárhagnum.
    - Fjárhagsvíddin má ekki leyfa auða reiti í lykilskipulaginu. Þessi takmörkun tryggir að allar bókhaldsfærslur sem eru færðar í bókhaldið innihaldi fjárhagsvíddargildi. Tóm vídd er ekki gild þegar jöfnunarvíddir eru notaðar.

3. Á síðunni **Lyklar fyrir sjálfvirkar færslur** (**Fjárhagur \> Uppsetning bókunar \> Lyklar fyrir sjálfvirkar færslur**), skal skilgreina aðallykla fyrir debet og kredit.
4. Á uppsetningarsíðu **Fjárhagur** (**Fjárhagur \> Fjárhagsuppsetning \> Fjárhagur**), í reitnum **Jöfnunarfjárhagsvídd** skal velja fjárhagsvídd fyrir jöfnun.

Ef valin fjárhagsvídd er ekki jöfnuð eftir að færslur eru færðar inn og birtar mun kerfið sjálfkrafa bæta við debet- eða kreditkortafærslum sem þarf til að jafna bókhaldsfærslu við bókun. Debet- og kreditfjárhagslyklarnir fyrir færslu milli eininga eru sýndir á birtu fylgiskjali í fjárhag. Þeir verða hins vegar ekki birtir í færslubókum eða upprunaskjölum sem bókhaldsfærslurnar voru bókaðar fyrir.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Fjárhagsvídd – Fara fram á að víddin sé jöfnuð

Þrátt fyrir að jöfnunarvíddin á síðunni **Fjárhagsvíddir** sé yfirleitt notuð af fyrirtækjum í opinbera geiranum er virknin ekki tengd neinum stillingarlykli í opinbera geiranum. Vegna þess að það er engin takmörkun í kerfinu getur þú notað þessa virkni jafnvel þótt stofnunin/fyrirtækið sé ekki opinber aðili.

Þessi virkni er yfirleitt notuð hjá viðskiptavinum opinberra aðila vegna þess að hún krefst þess að bókunarskilgreiningar séu notaðar til að jafna sjálfkrafa hverja færslu. Það notar ekki millieiningu debet- og kreditlykla sem eru skilgreindir á síðunni **Lyklar fyrir sjálfvirkar færslur** til að jafna bókhaldsfærslur sjálfkrafa. Ef bókhaldsfærsla er ekki jöfnuð á víddarstigi eftir að bókunarskilgreiningum er beitt verða færslurnar ekki birtar, jafnvel þótt debet- og kreditlyklar milli eininga séu skilgreindir.

Við heyrum oft af viðskiptavinum sem skilgreina jöfnunarvíddina bæði í fjárhagsuppsetningu og uppsetningu fjárhagsvíddar. Í þessu tilviki notar kerfið virkni fjárhagsvídda. Uppsetning fyrir jöfnunarvíddir á fjárhagsvíddarstigi hefur forgang meðan á bókun stendur. Bókun mistekst ef bókunarskilgreiningin skapar ekki jafnaða bókhaldsfærslu á fjárhagsvíddarstigi.

Fylgið þessum skrefum til að kveikja á notkun jöfnunarvíddar á fjárhagsvíddarstigi.

1. Ákveða hvaða fjárhagsvíddir verður jöfnunarvíddir.

    - Hægt er að velja fleiri en eina fjárhagsvídd sem jöfnunarvídd.
    - Ekki velja fjárhagsvíddir sem þarf til að jafna færslu á síðunni **Fjárhagsvíddir**.

2. Skilgreinið bókunarskilgreiningar fyrir hverja tegund færslubókar eða upprunaskjal sem stofnunin/fyrirtækið notar. Bókunarskilgreiningar nota fjárhagslykla úr óbókaðri færslubók eða upprunaskjali sem „skilyrði fyrir samsvörun“. Bókunarskilgreiningin skilar síðan „mynduðu færslunum“ sem verða að bókhaldsfærslunni. Ef bókunarskilgreiningin er sett upp á réttan hátt, inniheldur færslan sem mynduð er fjárhagslykla skilyrða fyrir samsvörun, auk viðbótarlykla til að jafna bókhaldsfærslu á víddarstigi. Frekari upplýsingar eru í [Bókunarskilgreiningar](posting-definitions.md). 
   
   Skilgreiningar á birtingu eru ekki studdar fyrir allar færslugerðir. Til dæmis er ekki hægt að skilgreina bókunarskilgreiningu fyrir færslur sem skráðar eru í gegnum fjárhag eða færslubók eigna. Ef ekki er hægt að skilgreina bókunarskilgreiningu fyrir færslubók eða upprunaskjal verður að jafna færsluna handvirkt við fjárhagsvíddargildið. Til dæmis, ef færsla í færslubók er gerð og deildarvíddin er jöfnunarvíddin verður þú að tryggja að hvert deildargildi sé jafnað.  Ef víddin er ekki jöfnuð fyrir hvert deildargildi mun fylgiskjalið ekki birtast fyrr en ójafnvægið hefur verið leiðrétt handvirkt með því að bæta debet- eða kredit millieiningar við fylgiskjalið. 

    > [!IMPORTANT]
    > Ef of margar færslur verða að vera handvirkar jafnaðar ætti **ekki** að nota virkni jöfnunarvíddar á síðunni **Fjárhagsvíddir**. Í staðinn skal nota virkni jöfnunarfjárhagsvíddar á uppsetningarsíðu **Fjárhagur**.

3. Eftir að bókunarskilgreiningar hafa verið skilgreindar er hægt að merkja fjárhagsvíddina sem þörf er á að jafna.

Þegar þú slærð inn og birtir færslur eru bókunarskilgreiningar kallaðar við bókun til að ákvarða færslur bókhalds. Ef fjárhagsvíddir eru jafnaðar á staðfesting sér stað eftir að bókhaldsfærslur hafa verið ákvarðaðar. Ef fjárhagsvíddirnar eru ekki jafnaðar verða færslan ekki bókuð og þú færð skilaboð þess efnis að debetfærslur séu ekki jafngildar kreditfærslum fyrir tiltekna vídd.
