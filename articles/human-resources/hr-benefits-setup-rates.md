---
title: Grunnstilla taxta
description: Verð í Microsoft Dynamics 365 Human Resources skilgreina hve mikið vinnuveitendur og starfsmenn leggja sitt af mörkum til fríðinda.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f846dcd0a15424ac681dd7e6a229d9da445a54e1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092408"
---
# <a name="configure-rates"></a>Grunnstilla taxta

[!include [banner](includes/preview-feature.md)]

Verð í Microsoft Dynamics 365 Human Resources skilgreina hve mikið vinnuveitendur og starfsmenn leggja sitt af mörkum til fríðinda. Gildið getur verið upphæð eða sveigjanleiki, allt eftir stillingum þínum.

Notaðu taxta til að ákvarða hversu mikið launþegar og vinnuveitendur greiða fyrir hverja bætur, út frá nokkrum þáttum. Tryggingarhlutfall er gildandi frá dagsetningunni, svo þú getur haldið sögulega skrá yfir verð. 

## <a name="set-up-rates"></a>Setja upp hlutföll

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hlutföll**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | Taxti | Einstakt nafn sem auðkennir fríðinahlutfallið. |
   | Lýsing | Lýsing á fríðindahlutfallinu. |
   | Virkt | Dagsetningin þar sem gengið er gildi. Núverandi kerfisdagsetning er sjálfgildið. 
   | Lok gildistíma | Lokadagur hlutfallsins. 12/31/2154 (sem táknar aldrei) er sjálfgildið. |
   | Nota lög | Lagið sem á að nota við útreikning á fríðindum. Stakt lag fyrir eins stigs fríðindahlutfall eða tvöfalt stig fyrir tveggja laga fríðindahlutfall. Dæmi um tvöfalt stig er flokkaupplýsingar byggðar á kyni og aldri. |
   | Greiðslutíðni | Greiðslutíðni sem ákvarðar hversu oft iðgjaldahlutfall er greitt til bótaaðila. Til dæmis, ef greiðslutíðni er mánaðarlega, þá er ávinningshlutfall mánaðarlega greiðslufjárhæðin. |
   | Reikniaðferð greiðslutíðni | Aðferðin við útreikning á tíðni launa tíðni: Venjuleg eða Árleg. |
   | Jöfnun greiðslutíðni | Aðferðin til að námunda hlutfallið: Stöðluð eða stytt. |
   | Upphæð starfsmanns fyrir þann sem reykir ekki | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Upphæð vinnuveitanda fyrir þann sem reykir ekki | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Upphæð starfsmanns fyrir reykingamann | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Upphæð vinnuveitanda fyrir reykingamann | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Upphæð stjórnunar | Stjórnsýslufjárhæð sem gjaldfærð er af þriðja aðila. Þetta er upphæðin sem vinnuveitandinn greiðir til þriðja aðila og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Sveigjanlegt útgjaldahlutfall | Fjöldi flex eykur fríðindakostnaðinn. Þetta á aðeins við um vexti sem eiga við áætlun um fríðindi sem er tengd flex-lánsfjáráætlunum. Ef þú notar stigavaxta er sveigjanlegur lánshlutfall skilgreint í Aðgerðum > Lagavextir. |
   | Breyta gildisdegi | Dagsetningin þegar breyting á fríðindataxta tekur gildi. Kerfið mun sjálfkrafa breyta fríðindataxtanum og uppfæra allar fríðindaáætlanir sem fylgja þessu taxta, svo framarlega sem þú keyrir vinnslu taxtauppfærsluskipta. Þú ættir ekki að stilla þessa dagsetningu nema þú viljir að kerfið uppfæri sjálfkrafa bætur áætlana starfsmanna út frá þessu gengi. Þetta er venjulega frátekið við sjálfvirka vinnslu á framtíðarbreytingum. Gildistaka breytingartímabilsins verður að vera innan gildistaxta og gildistíma fríðinda. |
   | Breytingu á hlutfalli lokið | Gátreiturinn frá taxtabreytingum lokið verður sjálfkrafa valinn þegar breytingum á taxta bótagreiðslna hefur verið lokið með frávinnslu breytinga á taxta. |

4. Veldu til að fylgjast með og viðhalda breytingum á uppbótarhlutfalli **Aðgerðir** og veldu síðan **Viðhalda útgáfum**.

5. Veljið **Vista**. 

## <a name="set-up-tier-rates"></a>Setja upp taxta fyrir lög

Þú getur notað stighlutfall í taxtauppsetningunni ef hlutfallið er mismunandi eftir ýmsum þáttum. Til dæmis gætirðu stillt stigahlutfall til að segja að ef aldur þinn er allt að 34,99 þá er upphæðin sem ekki reykir 2. Ef aldur þinn er allt að 39,99, þá er upphæðin sem ekki reykir 3.

Þú getur líka notað tvöfalt lag. Ef þú velur **Tvöfalt lag** fyrir gildið **Nota lög** á **Uppsetningu taxta** formi, þú getur skilgreint verð byggt á tveimur víddum. Til dæmis gætirðu stillt kerfi með tveimur lögum til að segja að ef þú ert karlkyns og aldur þinn er allt að 34,99 þá er upphæðin sem ekki reykir 2. Ef þú ert karlkyns og aldur þinn er allt að 39,99, þá er upphæðin sem ekki reykir 3. Ef þú ert kvenkyns og aldur þinn er allt að 34,99, þá er upphæðin sem ekki reykir 1.8. Ef þú ert kvenkyns og aldur þinn er allt að 39,99, þá er upphæðin sem ekki reykir 2.8.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hlutföll**.

2. Veldu eitt eða fleiri verð af listanum, veldu **Aðgerðir** og veldu síðan **Taxtar fyrir lög**.

3. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- | 
   | Lýsing | Gildið fyrir lýsingarreitinn verður beitt út frá lýsingunni í skrárhraðaprósentunni. Þetta hjálpar þér að bera kennsl á hvaða hlutfall skipulag stig stig eru tengd við. |
   | Kóði lags | Veldu kóða fyrir lög. Kóðar fyrir lög eru skilgreindir í gluggnaum Kóðar fyrir lög. Kerfið birtir sjálfkrafa lýsingu á kóða fyrir lög í töflunni til vinstri. |
   | Gerð þreps | Tilgreinir hvaða reit ætti að nota sem valviðmið fyrir útreikningsferli kóða fyrir lög. Dæmi:</br></br><ul><li>Ef aldur er notaður mun kerfið nota fæðingardegi starfsmanns í útreikningsferli bótahlutfallsins.</li><li>Ef laun eru notuð mun kerfið nota árleg hlunnindi starfsmanns í útreikningsferli bótahlutfallsins.</li><li>Ef starfstegund er notuð mun kerfið nota núverandi virka stöðuupplýsingar starfsmannsins til að ákvarða tegund gerðar eftir starfssetningu sem tengd er stöðunni.</li></ul></br></br>Flokkaupplýsingarnar eru Aldur, Laun, Líkamleg, Kyn, Stöðugildi, Störf, starfssvið og Stig. | 
   | Stig | Gildið sem á að nota með tegundinni við útreikning á fríðindataxta. Dæmi:</br></br><ul><li>Ef flokkaupplýsingar eru Aldur, þá væri þetta aldursgildið.</li><li>Ef flokkaupplýsingar eru Laun, þá væri þetta launaupphæðin.</li><li> Ef flokkaupplýsingar eru Starfsgerð, þá væri þetta starfsgerðin.</li></ul></br></br>Með flokkun aldurs eða launa notar kerfið hækkandi nálgun við val á stigahlutfalli, sem þýðir að gildi í stigsviðinu er neðri mörk stigsins. Með flokkaupplýsingar af starfsgerð notar kerfið nákvæma samsvörunaraðferð við val á stigi. |
   | Reiknigerð | Tilgreinir hvernig á að nota upphæðina í reitnum útreikningsfjárhæðar og hvaða stærðfræðiútreikning á að framkvæma ef þörf krefur. Ef útreikningsgerðin er flöt upphæð notar kerfið upphæðarsviðina eins og er. Ef útreikningsgerðin er á hverja $ upphæð af launum eða umfjöllun notar kerfið útreikningsupphæðina og útreikningsstefnuna í stærðfræðiútreikningi sínum.</br></br>Ef útreikningartegundin er á hverja $ upphæð launa notar kerfið eftirfarandi stærðfræðijöfnur:</br></br>Árleg bótagreiðsla deilt með Útreikningsupphæð (ávöl upp eða niður) sinnum upphæðir fyrir reykingamann eða ekki reykingarmann fyrir starfsmann eða vinnuveitanda.</br></br>Ef útreikningartegundin er á hverja $ upphæð tryggingar notar kerfið eftirfarandi stærðfræðijöfnur:</br></br>Tryggingarupphæð deilt með Útreikningsupphæð (ávöl upp eða niður) sinnum upphæðir fyrir reykingamann eða ekki reykingarmann fyrir starfsmann eða vinnuveitanda.</br></br>Í báðum útreikningum er útreikningsstefnan notuð til að ákvarða hvort fara skuli niður árleg hlunnindi eða tryggingarupphæð deilt með útreikningsupphæð upp eða niður. |
   | Reikningsupphæð | Upphæðin sem á að nota við útreikningsferli fríðinda. Þessi upphæð verður deilir í stærðfræðiútreikning á stighlutfalli. |
   | Stefna útreiknings | Stefnan (hækka eða lækka) sem reiknuð niðurstöðuupphæð ætti að vera námunduð við. Kerfið styður þrjár útreikningsleiðbeiningar: Autt (nákvæm aðferð), Hækka og Lækka.</br></br><ul><li>Ef það er autt mun kerfið nota nákvæma útreikning á launum / umfjöllunarfjárhæð deilt með útreikningsupphæðinni. Ef þetta gildi hefur brot, þá mun kerfið nota þetta við útreikning.</li><li>Ef Hækkun eykur kerfið stærðfræðiútreikning á launa / umfjöllunarfjárhæð deilt með útreikningsupphæðinni á næsta heiltölu, sem þýðir að 12,25 myndi hækka í 13.</li><li>Ef Lækkun lækkar kerfið stærðfræðiútreikning á launa / umfjöllunarfjárhæð deilt með útreikningsupphæðinni á núverandi heiltölu, sem þýðir að 12,25 myndi lækka í 12.</li></ul> |
   | Upphæð starfsmanns fyrir þann sem reykir ekki | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Upphæð vinnuveitanda fyrir þann sem reykir ekki | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Upphæð starfsmanns fyrir reykingamann | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Upphæð vinnuveitanda fyrir reykingamann | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Upphæð stjórnunar | Stjórnsýslufjárhæð sem gjaldfærð er af þriðja aðila. Þetta er upphæðin sem vinnuveitandinn greiðir til þriðja aðila og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | Hlutfall sveigjanlegra útgjalda fyrir þann sem reykir ekki | Fjöldi flex eykur ávinningskostnaðinn, miðað við útreikninginn sem er skilgreindur fyrir stig stig fyrir ekki reykingarfólk. Til dæmis, ef útreikningartegundin er 'Á $ fjárhæð umfjöllunar', þá er útreikningsupphæðin 10.000, og sveigjanleiki sem ekki reykir er 6, þá þýðir það að ef starfsmaður sem reykir ekki reykingar velur $10,000 af umfjöllun mun það kosta 6 beygja einingar. Ef þeir velja $20,000 af umfjöllun kostar það 12 flex einingar, og svo framvegis. |
   | Hlutfall reykingamanns fyrir sveigjanleg útgjöld | Fjöldi flex eykur ávinningskostnaðinn, miðað við útreikninginn sem er skilgreindur fyrir stig stig fyrir reykingarfólk. |

5. Veljið **Vista**. 
