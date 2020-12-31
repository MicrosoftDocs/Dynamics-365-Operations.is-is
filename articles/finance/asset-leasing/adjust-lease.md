---
title: Leiðrétta leigusamninga
description: Þetta efnisatriði útskýrir hvernig á að leiðrétta leigusamning. Leiðrétting gæti verið nauðsynleg ef leiguskilmálum er breytt, leigan framlengd eða aðrar aðstæður breytast.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444593"
---
# <a name="adjust-leases"></a>Leiðrétta leigusamninga

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að leiðrétta leigusamning. Leiðrétting gæti verið nauðsynleg ef leiguskilmálum er breytt, leigan framlengd eða aðrar aðstæður breytast. Eignarleiga uppfyllir leiðbeiningar sem efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16) kveður á um varðandi breytingar á leigusamningum. ASC 842-20-15-1 skilgreinir breytingar á leigusamningi sem allar breytingar á skilmálum samnings sem valda breytingu á umfangi, eða meðferð á leigusamningi. Málsgrein 39 í IFRS 16 segir að leigjandi þurfi að endurmeta leiguskuldbindingu þannig að hún endurspegli breytingar á leigugreiðslum.

Fyrir fyrirtæki sem fylgja ASC 842 eða IFRS 16 er leigusamningur endurmetinn aftur til að endurspegla breytingu á núvirði á lágmarksgreiðslum á leigu í framtíðinni (PVFMLP). Þegar PVFMLP-aukning er til staðar mun bókarfærslan sem er stofnuð vera debetfærsla afnotaréttar af eign og kreditfærsla leiguskuldbindingarinnar á milli nýja PVFMLP og eldri PVFMLP. Ef PVFMLP lækkar verður bókarfærslan debetfærsla leiguskuldbindingar og kreditfærsla afnotaréttar af eign fyrir mismuninum.

Ef leiðréttingin lækkar afnotarétt af eign 0 (núll) verður afgangurinn kreditfærður á bókunarlykil hagnaðar vegna breytinga á leigusamningi sem tilgreindur er á síðunni **Bókunarlyklar leigu**. Kerfisreikningar fyrir þessar færslur og aðrar leiðréttingarfærslur, svo sem breytingar á flokkun, ógreiddur stofnkostnaður, leiguhvatar, fyrirframgreiðslur og kostnaður sundurhlutunar sem hlýst af breytingum á leigusamningi.

Til að fá sérstaka leiðsögn varðandi leiðréttingarfærslur leigusamnings er mælt með því að skoða IFRS 16 og ASC 842.

Gerðu eftirfarandi til að breyta leigusamningi. Breyttu gögnin uppfæra leiguáætlun þegar keyrslu á ferli áætlunarinnar er lokið.

1. Opnaðu **Eignarleiga \> Leigusamningar \> Samantekt leigusamnings**.
2. Á síðunni **Samantekt leigusamnings** skaltu velja leigusamning til að leiðrétta og veldu síðan **Breyta leigusamningi**.
3. Á síðunni **Breyta leigusamningi** skaltu færa inn nýjar upplýsingar fyrir leiðréttan leigusamning.

    Taktu eftir því að síðan **Breyta leigusamningi** líkist síðunni **Bæta við leigusamningi**. Að auki, rétt eins og upphafsdagsetningin sem þú tilgreinir þegar leigusamningi er bætt við sker úr um hvenær leigusamningurinn hefst, sker svæðið **Breytingardagsetning** á síðunni **Breyta leigusamningi** úr um hvenær breytti leigusamningurinn hefst. Þessi dagsetning getur ekki verið eftir upphafsdagsetninguna í greiðsluáætlunarlínunum.

    > [!NOTE]
    > Svæðin **Atriði varðandi afnotarétt af eign** eiga við um breytinguna á leigusamningnum. Þegar enginn stofnkostnaður, leiguhvatar, fyrirframgreiðslur eða kostnaður sundurhluunar er tengdur við breyttan leigusamning skal skilja þessi svæði eftir auð. Upprunalegu upphæðirnar eiga ekki við um uppfærða leigusamninginn. Allur viðbótarkostnaður sem myndast þegar leigusamningnum er breytt ætti að færa inn á síðuna **Breyta leigusamningi**.
    > 
    > Leigusali veitir t.d. 1000 USD hvata til að samþykkja framlengingu á leigusamningi. Í þessu tilviki þegar þú breytir leigusamningnum til að gera ráð fyrir framlengingunni færir þú **1000** inn í svæðið **Leiguhvatar**. Ef engir hvatar eru tengdir við breytingar á leigusamningi skal hreinsa út öll gildi sem áður voru færð inn í þetta svæði. Sömu rökin eru notuð fyrir önnur atriði varðandi afnotarétt af eign.

    Greiðsluáætlunarlínur leiðrétta leigusamningsins ætti að stofna á væntanlegum grunni. Greiðsluáætlunarlínur sem eru stofnaðar á væntanlegan grunni geta ekki hafist áður en breytingar á leigusamningnum taka gildi.

    Eftirfarandi skref eru nánast hin sömu og upphafsskrefin við að viðurkenna leigusamning.

4. Veldu **Stofna áætlanir** til að mynda leiðrétta greiðsluáætlun. Þú færð skilaboð sem tilgreinir að greiðsluáætlun hafi verið stofnuð fyrir leigusamninginn.

    > [!IMPORTANT]
    > Áður en hægt er að velja **Stofna áætlanir** skal ganga úr skugga um að breytingadagsetningin og greiðsluáætlunarlínur séu réttar. Gangið einnig úr skugga um að allur stofnkostnaður, leiguhvatar, fyrirframgreiðslur eða kostnaður sundurhlutunar samsvari aðeins kostnaði sem hlýst af leiðréttingunni.

5. Til að skoða nýstofnaða greiðsluáætlun skal velja **Bækur** og opna síðuna **Greiðsluáætlun**.
6. Á síðunni **Greiðsluáætlun** er hægt að breyta leiðréttum greiðsluupphæðum áður en greiðsluáætlun er staðfest. Til að staðfesta áætlunina skal velja **Staðfesta áætlun**.

    Þegar greiðsluáætlun er staðfest er búið að stofna nýjar afskriftir eigna og nýjar áætlanir um leiguskuldbindingar.

7. Til að skoða nýju afskriftaráætlun leiguskuldbindingar sem er mynduð úr nýja innslættinum skal loka síðunni **Greiðsluáætlun** og opna síðan síðuna **Afskriftaráætlun leiguskuldbindingar**.
8. Til að skoða nýmyndaða afskriftaráætlun eigna skal opna síðuna **Afskriftaráætlun eigna** á síðunni **Upplýsingar um bók**.
9. Til að mynda leiðréttingarbókarfærslu skal velja **Aðgerð \> Leiðrétting leigusamnings**. Þú færð skilaboð sem segir til um að leiðréttingabókarfærsla hafi verið stofnuð. 
10. Til að skoða bókarfærsluna skal velja **Færslubækur \> Færslubók eignarleigu**.
11. Til að bóka bókarfærsluna skal velja línuna og velja síðan **Bóka**.

## <a name="view-lease-versions"></a>Skoða útgáfur leigusamnings

Ef leigusamningi hefur verið breytt er hægt að skoða mismunandi útgáfur af honum. Einnig er hægt að skoða eldri áætlanir og eldri upplýsingar um leigusamning.

1. Á síðunni **Samantekt leigusamnings** skal velja leigusamning og velja síðan á aðgerðasvæðinu **Útgáfuferill leigusamnings**.

    Þegar breytingar hafa verið gerðar á völdum leigusamningi birtast ólíkar útgáfur af samningnum á síðunni **Útgáfuferill leigusamnings**. Upprunalegi leigusamningurinn er merktur með **1** og útgáfurnar þar á eftir með hækkandi númeraröð.

    Fyrir valda útgáfu leigusamnings er hægt að skoða fjárhagsvíddirnar, frekari upplýsingar um samninginn, staðsetningu og greiðsluáætlunarlínur.

2. Til að skoða eldri áætlanir skal opna breyttan leigusamning á síðunni **Samantekt leigusamnings** velja viðeigandi bók og velja síðan **Útgáfuferill bókar** á aðgerðasvæðinu.
3. Á síðunni **Bókaútgáfa** skal velja æskilega útgáfu og æskilega áætlun til skoðunar.
