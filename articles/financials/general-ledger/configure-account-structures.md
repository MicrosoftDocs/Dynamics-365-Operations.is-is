---
title: Skilgreina lykilskipulög
description: Þetta efnisatriði inniheldur upplýsingar um lykilskipulög og fjárhagsvíddir.
author: aprilolson
manager: AnnBe
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fbd4b34d09b4ba8e1d34234c8e32268bba18778
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617297"
---
# <a name="configure-account-structures"></a>Skilgreina lykilskipulög

[!include[banner](../includes/banner.md)]

Lykilskipulög notar aðallykil og fjárhagsvíddir til að búa til safn af reglum sem ákvarða röð og gildi sem notaðar eru þegar lykilnúmerið er slegið inn. Hægt er að setja upp ótakmarkaðan fjölda lykilskipulaga fyrir fyrirtækið. Lykilskipulögunum er úthlutað á fjárhagsuppsetningu fyrirtækisins svo hægt sé að deila þeim.

Þegar lykilskipulag er stofnað er hámarksfjöldi hluta 11. Ef þú þarft fleiri hluta en þetta skaltu meta vandlega uppsetningu þína og kröfur, þar sem það mun hafa áhrif á reynslu notanda. Íhugaðu hvort hægt sé að afleiða hluta í uppgefinni atburðarás með því að nota stigveldi í staðinn við gagnaskráningu eða með því að nota notandaskilgreint svæði. Til dæmis, ef þú vilt tilkynna um staðsetningu, en þú getur fundið staðsetningu eftir deild eða kostnaðarstað, þá þarft þú ekki staðsetningu sem fjárhagsvídd. Ef þú ákveður að 11 hlutar séu nauðsynlegar eftir að hafa lagt mat á það getur þú bætt við fleiri hlutum með ítarlegum reglum.

Lykilskipulög krefjast aðallykils. Aðallykillinn þarf ekki að vera fyrsti hlutinn í skipulaginu, en hann gefur til kynna hvaða lykilskipulag er verið að nota við skráningu lykilnúmers. Út af þessu getur gildi aðallykils aðeins verið fyrir hendi í einu skipulagi sem er úthlutað til fjárhags þannig að þau skarast ekki. Eftir að lykilskipulagið er auðkennt er listinn yfir leyfileg gildi síaður til að leiðbeina notandanum með því að velja aðeins gild víddargildi, sem dregur úr möguleika á rangri bókarfærslu.

> [!NOTE] 
> Ef þú ætlar að fjárhagsáætlun á móti fjárhagsvídd verður það að vera hluti af lykilskipulagi. Fjárhagsáætlanagerð nýtir ekki ítarlegar reglur enn sem komið er.

## <a name="example"></a>Dæmi
Til að sýna bestu starfsvenjur við uppsetningu lykilskipulags skulum við gera ráð fyrir því að fyrirtæki vill fylgjast með efnahagslyklum sínum (100000..399999) á fjárhagsvíddarstigi lykil- og viðskiptaeiningar. Fyrir tekju- og kostnaðarlykla (400000..999999), þeir rekja viðskiptaeiningu, deild og kostnaðarstað fjárhagsvídda. Ef sala á sér stað vilja þeir líka rekja viðskiptavin. Með því að nota þessa atburðarás er mælt með að hafa tvö lykilskipulög úthlutuð á fjárhag fyrirtækisins - einn fyrir efnahagslykla og einn fyrir rekstrarlykla. Til að hámarka notendaupplifun og villuleit ætti viðskiptavinurinn að vera ítarleg regla sem aðeins er notaðu þegar sölulykill er notaður.

**Skipulag efnahagslykils**

|Aðallykill          | Viðskiptaeining    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Skipulag rekstrarreiknings**

|Aðallykill          | Viðskiptaeining    |Deild          | Kostnaðarstaður    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | *;” “|*;” “|*;” “|*;” “|

**Ítarleg regla til að bæta við viðskiptavini**

Skilyrði: Þar sem aðallykill er á milli 400000 og 499999, þá skal bæta við viðskiptavini. Ekki er hægt að skilja eftir autt.

|Viðskiptavinur         |
|-----------------|
|* |

Í þessu einfaldaða dæmi eru öll gildi og eyður leyfðar svo að * og „.“ eru notaðar.

## <a name="segments-and-allowed-values"></a>Hlutar og leyfð gildi
Kaflarnir **Hlutar** og **Upplýsingar um leyfð gildi** veita eins konar hnitanet til að slá inn reglurnar sem verður fylgt eftir í villuleit við bókun. Þú getur slegið beint í reiti hnitanetsins, flutt það inn frá Excel eða notað kaflann **Upplýsingar um leyfð gildi** til að leiðbeina þér í gegnum það.

Kaflinn **Upplýsingar um leyfð gildi** leiðbeinir þér í gegnum það að búa til skilyrði með því að nota **Virknitákn** eins og byrjar með, er á milli, inniheldur og margt fleira.

[![Leyfa gildi](./media/account.png)](./media/account.png) 

Leyfð gildi verða sjálfgefin á færslusíðu fyrir færslubók eða dreifingu á fjárhagsupphæð þegar ekki er hægt að velja nein önnur gildi samkvæmt uppsetningu lykilskipulags.

Hér er dæmi um **Skipulag rekstrarreiknings**.

|Aðallykill          | Viðskiptaeining    |Deild          | Kostnaðarstaður    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Þegar færslubók er færð inn og við val á lykli í rekstrarbilinu, mun val á viðskiptaeiningu „002“ leiða til þess að gildin 022 og 014 verði sjálfgefin fyrir stjórnun lykils. Þessi hegðun mun einnig eiga sér stað fyrir síðu dreifingar á fjárhagsupphæð. 

## <a name="more-than-7-criteria-needed"></a>Fleiri en 7 skilyrði þarf

Ef þú hefur fleiri en 7 skilyrði sem þarf, getur þú haldið áfram að bæta þeim við í næstu línu. Þú munt taka eftir því þegar að þú vinnur í hlutanum **Upplýsingar um leyfð gildi** að skilyrðið **+bæta við nýju** er ekki lengur virkt eftir að sjöunda skilyrðið er slegið inn. Þetta stafar af mörgum þáttum eins og: 
 - Dálkbreidd 
 - Hvernig gögnin eru geymd 
 - Frammistaða á stýringunni **Upplýsingar um leyfð gildi**
 - Notandahæfi  
 
Til að halda áfram að bæta við fleiri skilyrðum skaltu smella á **Afrita í hlutanum** og **Hluti leyfðra gilda**. Þetta mun afrita skilyrðið í nýja línu. Þú getur þá skrifað yfir eða breytt kaflanum **Upplýsingar um leyfð gildi**.

## <a name="best-practices"></a>Bestu venjur
Þegar þú setur upp lykilskipulögin þín eru nokkrar bestu venjur sem þú getur fylgt eftir. Hins vegar er þetta aðeins leiðsögn svo að heildræn umræða um fyrirtæki þitt, vaxtaráætlun og viðhaldsáætlun ætti að teljast hluti af þeirri umfjöllun.

- Hafðu aðallykil fyrstan eða eins nálægt yfirborði lykilskipulagsins og mögulegt er þannig að notendur fái bestu leiðsögn sem þeir geta við lykilfærslu.

- Nota lykilskipulög aftur eins mikið og mögulegt er til að draga úr viðhaldi þvert yfir lögaðila þína.

- Fyrir afbrigði þvert yfir lögaðila skaltu íhuga að nota ítarlegar reglur þannig að hægt sé að nota lykilskipulög aftur.

- Þegar þú skilgreinir leyfð gildi skaltu nota svið og algildi eins mikið og mögulegt er. Þetta leyfir þér ekki aðeins að vaxa og breytast án viðhalds, en kerfið gengur einnig betur með þessari skilgreiningu.

- Ekki bara setja stjörnu fyrir hvern hluta í lykilskipulaginu og síðan eingöngu að treysta á ítarlegu reglurnar. Þetta getur verið erfitt að stjórna og leiðir oft til notandavillna á meðan á viðhaldi stendur sem getur gert það að verkum að kerfið getur ekki bókað.

## <a name="account-structure-activation"></a>Virkjun lykilskipulags
Þegar þú ert ánægð(ur) með nýju uppsetninguna eða breytingu á lykilskipulagi, verður þú að virkja það. Ef lykilskipulagi er úthlutað á fjárhag, getur þessi virkjun verið ferli sem tekur langan tíma að keyra, þar sem allar óbókaðar færslur í kerfinu verða að vera samstilltar við nýja skipulagið. Bókaðar færslur verða ekki fyrir áhrifum af völdum breytinga á lykilskipulag.

Nánari upplýsingar er að finna í [Skipuleggðu bókhaldslykilinn þinn](plan-chart-of-accounts.md), [Fjárhagsvíddir](financial-dimensions.md) og [Sláðu inn lykil og víddarsamsetningum (hlutuð færslustýring)](enter-account-dimension-combinations-segmented-entry-control.md).
