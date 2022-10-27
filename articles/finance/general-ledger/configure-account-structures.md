---
title: Skilgreina lykilskipulög
description: Þessi grein veitir upplýsingar um reikningsuppbyggingu og fjárhagsvíddir.
author: aprilolson
ms.date: 10/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3fbdd6e2cac61c358848a21e1126bea900e86b2
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713944"
---
# <a name="configure-account-structures"></a>Skilgreina lykilskipulög

[!include[banner](../includes/banner.md)]

Lykilskipulög notar aðallykil og fjárhagsvíddir til að búa til safn af reglum sem ákvarða röð og gildi sem notaðar eru þegar lykilnúmerið er slegið inn. Hægt er að setja upp ótakmarkaðan fjölda lykilskipulaga fyrir fyrirtækið. Reikningsskipulaginu er úthlutað til fjárhagsuppsetningar fyrirtækis, svo hægt sé að deila þeim.

Þegar lykilskipulag er stofnað er hámarksfjöldi hluta 11. Ef þú þarft fleiri en 11 hluta skaltu meta uppsetningu þína og kröfur vandlega, þar sem það mun hafa áhrif á notendaupplifunina. Íhugaðu hvort hægt sé að afleiða hluta í uppgefinni atburðarás með því að nota stigveldi í staðinn við gagnaskráningu eða með því að nota notandaskilgreint svæði. Til dæmis, ef þú vilt tilkynna um staðsetningu, en þú getur fundið staðsetningu eftir deild eða kostnaðarstað, þarftu ekki staðsetningu sem fjárhagsvídd. Ef þú ákveður að 11 hlutar séu nauðsynlegar eftir að hafa lagt mat á það getur þú bætt við fleiri hlutum með ítarlegum reglum.

Lykilskipulög krefjast aðallykils. Aðalreikningurinn þarf ekki að vera fyrsti hluti skipulagsins, en hann auðkennir hvaða reikningsskipulag er notað við innslátt reikningsnúmersins. Vegna þessa getur aðalreikningsgildi aðeins verið til í einni uppbyggingu sem úthlutað er fjárhagsbókinni svo þau skarist ekki. Eftir að lykilskipulagið er auðkennt er listinn yfir leyfileg gildi síaður til að leiðbeina notandanum með því að velja aðeins gild víddargildi, sem dregur úr möguleika á rangri bókarfærslu.

> [!NOTE] 
> Ef þú ætlar að fjárhagsáætlun á móti fjárhagsvídd verður það að vera hluti af lykilskipulagi. Fjárhagsáætlanagerð nýtir ekki ítarlegar reglur enn sem komið er.

## <a name="example"></a>Dæmi
Til að sýna bestu starfsvenjur við uppsetningu lykilskipulags skulum við gera ráð fyrir því að fyrirtæki vill fylgjast með efnahagslyklum sínum (100000..399999) á fjárhagsvíddarstigi lykil- og viðskiptaeiningar. Fyrir tekju- og kostnaðarlykla (400000..999999), þeir rekja viðskiptaeiningu, deild og kostnaðarstað fjárhagsvídda. Ef sala á sér stað vilja þeir líka rekja viðskiptavin. Með því að nota þessa atburðarás væri mælt með því að hafa tvær reikningsuppbyggingar úthlutaðar á fjárhagsbók fyrirtækisins - einn fyrir efnahagsreikninga og einn fyrir rekstrarreikninga. Til að hámarka notendaupplifun og villuleit ætti viðskiptavinurinn að vera ítarleg regla sem aðeins er notaðu þegar sölulykill er notaður.

**Skipulag efnahagslykils**

|Aðallykill          | Viðskiptaeining    |
|----------------------|-----------|
|100000..399999 | *;"&nbsp; "|

**Skipulag rekstrarreiknings**

|Aðallykill          | Viðskiptaeining    |Deild          | Kostnaðarstaður    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;"&nbsp; "| \*;"&nbsp; "| \*;"&nbsp; "| \*;"&nbsp; "|

**Ítarleg regla til að bæta við viðskiptavini**

Skilyrði: Þar sem aðallykill er á milli 400000 og 499999, þá skal bæta við viðskiptavini. Það má ekki skilja það eftir autt.

|Viðskiptamaður         |
|-----------------|
|\* |

Í þessu einfaldaða dæmi eru öll gildi og auð leyfð\* og "&nbsp; " eru notuð.

## <a name="segments-and-allowed-values"></a>Hlutar og leyfð gildi
Kaflarnir **Hlutar** og **Upplýsingar um leyfð gildi** veita eins konar hnitanet til að slá inn reglurnar sem verður fylgt eftir í villuleit við bókun. Þú getur slegið beint í reiti hnitanetsins, flutt það inn frá Excel eða notað kaflann **Upplýsingar um leyfð gildi** til að leiðbeina þér í gegnum það.

Kaflinn **Upplýsingar um leyfð gildi** leiðbeinir þér í gegnum það að búa til skilyrði með því að nota **Virknitákn** eins og byrjar með, er á milli, inniheldur og margt fleira.

[![Leyfa gildi.](./media/account.png)](./media/account.png) 

Leyfð gildi verða sjálfgefin á færslusíðu fyrir færslubók eða dreifingu á fjárhagsupphæð þegar ekki er hægt að velja nein önnur gildi samkvæmt uppsetningu lykilskipulags.

Hér er dæmi um **Skipulag rekstrarreiknings**.

|Aðallykill          | Viðskiptaeining    |Deild          | Kostnaðarstaður    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Þegar færslubók er færð inn og við val á lykli í rekstrarbilinu, mun val á viðskiptaeiningu „002“ leiða til þess að gildin 022 og 014 verði sjálfgefin fyrir stjórnun lykils. Þessi hegðun mun einnig eiga sér stað fyrir síðu dreifingar á fjárhagsupphæð. 

## <a name="more-than-seven-criteria-needed"></a>Það þarf meira en sjö viðmið

Ef þú hefur fleiri en sjö viðmið sem þarf geturðu haldið áfram að bæta þeim við í næstu línu. Þú munt taka eftir því þegar þú vinnur í **Leyfðar upplýsingar um gildi** kafla sem **+Bæta við nýjum** skilyrði er ekki lengur virkt eftir að sjöunda viðmiðið er slegið inn. Þetta stafar af mörgum þáttum eins og: 
 - Dálkbreidd 
 - Hvernig gögnin eru geymd 
 - Frammistaða á stýringunni **Upplýsingar um leyfð gildi**
 - Notandahæfi  

> [!NOTE]
> Uppfærsla frá Microsoft Dynamics AX 2012 þar sem fleiri en sjö viðmið eru tilgreind er ekki stutt. Það verður að leiðrétta áður en þú lýkur uppfærslunni í fjármála- og rekstrarforrit. 

Til að halda áfram að bæta við fleiri skilyrðum skaltu smella á **Afrita í hlutanum** og **Hluti leyfðra gilda**. Þetta mun afrita skilyrðið í nýja línu. Þú getur þá skrifað yfir eða breytt kaflanum **Upplýsingar um leyfð gildi**.

## <a name="best-practices"></a>Bestu venjur
Þegar þú setur upp reikningsskipulag þitt eru nokkrar bestu starfsvenjur sem þú getur fylgt. Hins vegar er þetta aðeins leiðsögn svo að heildræn umræða um fyrirtæki þitt, vaxtaráætlun og viðhaldsáætlun ætti að teljast hluti af þeirri umfjöllun.

- Gerðu aðalreikninginn fyrst eða eins nálægt framhlið reikningsskipulagsins og mögulegt er, svo notendur fái bestu leiðsögn sem þeir geta við innslátt reiknings.
  
  - Staðfestu að allar lausnir frá þriðja aðila sem þú ætlar að nota styðji aðalreikning í fyrstu stöðu.

- Nota lykilskipulög aftur eins mikið og mögulegt er til að draga úr viðhaldi þvert yfir lögaðila þína.

- Fyrir afbrigði þvert yfir lögaðila skaltu íhuga að nota ítarlegar reglur þannig að hægt sé að nota lykilskipulög aftur.

- Þegar þú skilgreinir leyfð gildi skaltu nota svið og algildi eins mikið og mögulegt er. Þetta leyfir þér ekki aðeins að vaxa og breytast án viðhalds, en kerfið gengur einnig betur með þessari skilgreiningu.

- Ekki bara setja stjörnu fyrir hvern hluta í lykilskipulaginu og síðan eingöngu að treysta á ítarlegu reglurnar. Þetta getur verið erfitt að stjórna og leiðir oft til notandavillna á meðan á viðhaldi stendur sem getur gert það að verkum að kerfið getur ekki bókað.

## <a name="account-structure-activation"></a>Virkjun lykilskipulags
Þegar þú ert ánægður með nýju uppsetninguna þína eða breytingu á reikningsskipulagi verður þú að virkja hana. Ef lykilskipulagi er úthlutað á fjárhag, getur þessi virkjun verið ferli sem tekur langan tíma að keyra, þar sem allar óbókaðar færslur í kerfinu verða að vera samstilltar við nýja skipulagið. Bókaðar færslur verða ekki fyrir áhrifum af breytingum á reikningsskipulagi. Frá og með útgáfu útgáfu 10.0.31, nýr eiginleiki sem heitir **Frammistöðuaukning reikningsskipulagsvirkjunar** er fáanlegt í eiginleikastjórnun. Fyrir frekari upplýsingar um þennan nýja eiginleika fyrir virkjun reikningsskipulags, sjá [Frammistöðuaukning reikningsskipulagsvirkjunar](account-structure-improvement.md). 

Fyrir frekari upplýsingar, sjá [Skipuleggðu reikningsyfirlitið þitt](plan-chart-of-accounts.md),[Fjárhagsstærðir](financial-dimensions.md), og [Sláðu inn reiknings- og víddarsamsetningar (hlutbundin færslustýring)](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
