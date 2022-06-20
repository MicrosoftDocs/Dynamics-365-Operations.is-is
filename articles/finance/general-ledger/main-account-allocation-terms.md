---
title: Úthlutunarskilmálar
description: Þessi grein veitir upplýsingar um notkun úthlutunarskilmála á aðalreikningi.
author: rachel-profitt
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: twheeloc
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d62c0cc79c9d61e0ebb1c2c62a345ad47412d0d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859828"
---
# <a name="allocation-terms"></a>Úthlutunarskilmálar

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um notkun úthlutunarskilmála á aðalreikningi. Úthlutunarskilmálar eru notaðir til að dreifa upphæðum á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.

Hvert úthlutunarskilmáli sem er búinn til á aðallykli skilgreinir hlutfallsprósentu fylgiskjals sem á að úthluta úr aðallykli með einn uppruna og samsetningu fjárhagsvídda. Að auki er áfangastaður aðallykils og fjárhagsvíddir skilgreindar þar sem upphæðinni verður úthlutað. 

Þegar fjárhagsvídd uppruna er skilgreind fyrir úthlutunina, er hægt að velja hvort hver vídd sé sértæk eða ósértæk. Sértæk gefur til kynna að fjárhagsvídd fyrir upprunafærslu þurfi að samsvara valinni vídd. Þegar ósértækt er valið, gefur það til kynna að eitthvert gildi fjárhagsvíddarinnar geti stuðlað að samsvörun.

Þegar áfangastaður fjárhagslykils er skilgreindur fyrir úthlutunarskilmála, þarf að tilgreina aðallykilinn sem upphæðinni er úthlutað á. Hægt er að nota sama aðallykilinn þar sem upprunafærslan er bókuð á eða annan aðallykil. Ef sami aðallykillinn er notaður birtist viðvörun þegar verið er að vista færsluna. Auk þess að tilgreina aðallykilinn þarf einnig að tilgreina víddir áfangastaðar. Fyrir hverja vídd er hægt að tilgreina hvort eigi að halda upprunalegu fjárhagsvíddargildi eða breyta því. Ef „nei“ er valið, þarf að velja nýtt gildi fyrir fjárhagsvíddina. Ef valið er „já“ eru engar viðbótarupplýsingar tilgreindar og kerfið viðheldur upprunalegu fjárhagsvíddunum þegar bókað er.

Engin takmörk eru á fjölda úthlutunarskilmála sem hægt er að bæta við aðallykil; hins vegar getur samanlögð prósenta úthlutunar fyrir úthlutunarskilmála ekki farið yfir 100. Hægt er að stofna úthlutanir fyrir minna en 100 prósent ef hluti upprunalegrar fylgiskjalsupphæðar á að vera áfram í fjárhagsvíddum upprunans. Hægt er að bæta úthlutunarskilmálum við aðallykil sem hnekkingu lögaðila. Ef verið er að nota samnýttan bókhaldslykil, verða úthlutunarskilmálar að vera skilgreindir fyrir hvern lögaðila. Til að fá aðgang að hnappnum **Úthlutunarskilmálar**, þarf fyrst að velja gátreitinn **Úthlutun** í hnekkingu lögaðila.

## <a name="allocation-term-example"></a>Dæmi um úthlutunarskilmála
Búið er að skilgreina kostnaðarstað fyrir fyrirtækið sem kallast FYRIRTÆKI sem er tölusett 000. Þegar reikningar eru bókaðir fyrir rekstrarkostnað, eru þeir kóðaðir fyrir kostnaðarstaðinn FYRIRTÆKI. Fyrirtækið hefur skilgreint reglu sem segir að allan rekstrarkostnað eigi að úthluta eftir prósentuhlutfalli til hvers kostnaðarstaðs fyrir sig. Aðrar fjárhagsvíddir fyrir deild og fyrirtækiseiningu haldast óbreyttar.

Í þessu dæmi verður nýr úthlutunarskilmáli stofnaður fyrir aðallykil rekstrarkostnaðar. Ein lína yrði stofnuð fyrir hvern kostnaðarstað með prósentunni sem á að úthluta. **Valskilyrðið** fyrir fjárhagsvíddir upprunans fyrir hverja línu yrði **Sértækt** fyrir **Kostnaðarstaðinn** og gildið yrði stillt á 000: FYRIRTÆKI. Fyrir deild og fyrirtækiseiningu yrði **Valskilyrðið** að **Ótilgreint**.

Í flýtiflipanum **Fjárhagslykill áfangastaðar**, verður aðallykillinn sami rekstrarkostnaðarlykillinn og **Geyma fjárhagsvíddir uppruna** verður stillt á **Já** fyrir **Fyrirtækiseiningu** og **Deild**. **Geyma fjárhagsvíddir uppruna** verður stillt á **Nei** fyrir **Kostnaðarstað**, og gildið sem er valið verður hver viðkomandi kostnaðarstaður sem verið er að úthluta á. Ef úthluta þarf á þrjá kostnaðarstaði, verða þrjár færslur úthlutunarskilmála búnar til. Eini munurinn milli hvers úthlutunarskilmála fyrir sig er kostnaðarstaðurinn sem er tilgreindur á fjárhagslykli áfangastaðar.

## <a name="create-an-allocation-term-on-a-main-account"></a>Stofna úthlutunarskilmála í aðallykli

1. Í **Yfirlitssvæðinu** skal fara í **Einingar > Fjárhagur > Bókhaldslykill > Lyklar > Aðallyklar**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í flýtiflipanum **Hnekkingar lögaðila** skal velja **Bæta við**.
4. Veljið **Fyrirtæki** og veljið síðan **Bæta við**.
5. Veljið gátreitinn **Úthlutun**.
6. Veljið **Úthlutunarskilmálar**.
7. Veljið **Breyta** til að breyta sjálfgefinni færslu, eða veljið **Ný** til að bæta við færslu.
8. Í reitinn **Prósent** skal færa inn prósentuna á fylgiskjalsfærslum sem ætlunin er að úthluta.
9. Í flýtiflipanum **Fjárhagsvídd uppruna**, í **Valskilyrði** fyrir hverja fjárhagsvídd, skal velja valkost.
    - Ef valið er **Tiltekið** skal velja fjárhagsvíddargildið í fellilistanum hægra megin.
    - Ef valið er **Ótiltekið** er engra frekari upplýsinga krafist fyrir fjárhagsvíddina.
10. Í flýtiflipanum **Fjárhagslykill áfangastaðar**, í reitnum **Til lykils**, skal velja aðallykilinn þar sem ætlunin er að úthluta prósentuhlutfalli fylgiskjalsfærslunnar.
11. Í **Geyma fjárhagsvíddir uppruna** fyrir hverja fjárhagsvídd, skal velja valkost.
    - Ef valið er **Nei**, skal velja fjárhagsvíddargildið í fellilistanum hægra megin þar sem ætlunin er að úthluta fylgiskjalsfærslunni á.
    - Ef valið er **Já**, þarf ekki frekari upplýsingar. Kerfið geymir gildið í upprunalega fylgiskjalinu þegar úthlutunin er bókuð.
12. Endurtakið skref 7-11 fyrir hverja viðbótarúthlutun. Samtala allra úthlutana er tilgreind í reitnum **Heildarprósenta**. Þessi upphæð má ekki vera hærri en 100.
13. Lokið öllum síðunum.

>[!NOTE] 
> Hægt er að nota hnappinn **Afrita** til að tvítaka valda úthlutun.

Þegar úthlutunarskilmáli er stofnaður fyrir aðallykil, bókar kerfið nýtt fylgiskjal sjálfkrafa þegar fylgiskjal er bókað sem samsvarar fjárhagsvíddum uppruna í úthlutunarskilmálunum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
