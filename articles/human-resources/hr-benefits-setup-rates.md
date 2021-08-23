---
title: Grunnstilla taxta
description: Verð í Microsoft Dynamics 365 Human Resources skilgreina hve mikið vinnuveitendur og starfsmenn leggja sitt af mörkum til fríðinda.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: da006516f8b3a1d8eb0d4963187d01308f059619f95a52410391d9501aafbbc1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732706"
---
# <a name="configure-rates"></a>Grunnstilla taxta

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Taxtar skilgreina hversu mikið vinnuveitendur og starfsmenn leggja fram til fríðinda. Gildið getur annaðhvort verið upphæð eða sveigjanlegir inneignapunktar eftir því hver skilgreiningin er.

Notaðu taxta til að ákvarða hversu mikið launþegar og vinnuveitendur greiða fyrir hverja bætur, út frá nokkrum þáttum. Tryggingarhlutfall er gildandi frá dagsetningunni, svo þú getur haldið sögulega skrá yfir verð. 

## <a name="set-up-rates"></a>Setja upp hlutföll

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hlutföll**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Taxti** | Einstakt nafn sem auðkennir fríðinahlutfallið. |
   | **Lýsing** | Lýsing á fríðindahlutfallinu. |
   | **Virkt** | Dagsetningin þegar taxtinn tekur gildi. Núverandi kerfisdagsetning er sjálfgildið. Dagsetningin á að vera á eða á undan fríðindatímabilinu. Góð venja er að stilla dagsetninguna á dagsetningu fríðindaáætlunarinnar. |
   | **Lok gildistíma** | Lokadagur hlutfallsins. 12/31/2154 (sem táknar aldrei) er sjálfgildið. |
   | **Nota lög** |  Notaðu þennan reit ef þú ert með rök sem verður að nota til að ákvarða taxta. Ef til dæmis þarf að hækka taxtann samkvæmt aldri skal velja gildi hér. Veldu **Eitt lag** fyrir fríðindahlutfall með einföldu lagi eða **Tvöfalt lag** fyrir fríðindahlutfall með tvöföldu lagi. Dæmi um tvöfalt lag er lag sem byggir á kyni og aldri. Eftir að þú hefur valið gildi velur þú **Aðgerðir** og síðan **Hlutföll lags**. Ef þú ert með fastan taxta sem breytist ekki skal skilja þennan reit eftir auðan. |
   | **Greiðslutíðni** | Tilgreindu hversu oft á að greiða þjónustuaðila fríðinda taxta iðgjalds. Taxtinn sem er sleginn inn á síðuna sem er útskýrður síðar í þessu efnisatriði mun byggja á greiðslutíðninni sem er tilgreind hér. Ef þú til að mynda færir inn **Mánaðarlega** í þennan reit og færir inn starfsmannantaxta upp á **$100** er ályktað að fríðindin muni kosta starfsmanninn $100 á mánuði. Starfsmaður gæti þó fengið greitt tvisvar sinnum í mánuði samkvæmt greiðslutíðni fríðindanna sem er stillt í starfsmannsfærslunni. Í þessu tilviki, þegar starfsmaðurinn skráir sig inn í sjálfsafgreiðslu starfsmanns, mun upphæðin sem hann greiðir vera $50 vegna þess að taxtinn sem sjálfsafgreiðsla starfsmanns sýnir byggir á greiðslutíðni starfsmannsins. |
   | **Jöfnun greiðslutíðni** | Aðferðirnar við sléttun á hlutfalli eru: staðlað, stytt, venjulegt, niður á við og upp á við. </br></br><ul><li>**Hefðbundið** - Alltaf slétta upp. Til dæmis munu 10,611 slétta í 10,62. -10,231 sléttar að -10,23. </li><li>**Stytt** - Alltaf slétta niður. Til dæmis mun 10,619 slétta í 10,61. -10.231 sléttar í -10.24. </li><li>**Venjulegt** - Gildi aukastafa sem enda á 5 eða hærri tölu sléttast frá núlli. Gildi aukastafa sem enda á 4 eða minna munu sléttast í núll. Til dæmis munu 10,615 slétta í 10,62. -10,235 sléttar í -10,24. 10,614 sléttar í 10,61. -10.234 sléttar í -10.23. </li><li>**Niður á við** - Slétta að núlli. Til dæmis mun 10,619 slétta í 10,61. -10,231 sléttar að -10,23. </li><li>**Upp á við** - Slétta frá núlli. Til dæmis mun 10,619 slétta í 10,62. -10.231 sléttar í -10.24. |
   | **Upphæð starfsmanns fyrir þann sem reykir ekki** | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | **Upphæð vinnuveitanda fyrir þann sem reykir ekki** | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir þjónustuaðila fríðinda og hún ætti að vera byggð á greiðslutíðni fyrir uppsetningu taxtans. |
   | **Upphæð starfsmanns fyrir reykingamann** | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | **Upphæð vinnuveitanda fyrir reykingamann** | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir. Þetta er upphæðin sem vinnuveitandinn greiðir til bótaveitunnar og ætti að vera byggð á greiðslutíðni fyrir uppsetningar taxta. |
   | **Upphæð stjórnunar** | Stjórnsýslufjárhæð sem gjaldfærð er af þriðja aðila. Þetta er upphæðin sem vinnuveitandinn greiðir þriðja aðila og hún ætti að miðast við greiðslutíðni fyrir uppsetningu taxtans. |
   | **Sveigjanlegt útgjaldahlutfall** | Fjöldi flex eykur fríðindakostnaðinn. Þetta á aðeins við um vexti sem eiga við áætlun um fríðindi sem er tengd flex-lánsfjáráætlunum. Ef þú notar stigavaxta er sveigjanlegur lánshlutfall skilgreint í Aðgerðum > Lagavextir. |
   | **Breyta gildisdegi** | Dagsetningin þegar breyting á fríðindataxta tekur gildi. Kerfið breytir sjálfkrafa hlutfalli fríðinda og uppfærir allar fríðindaáætlanir sem tengjast þessum taxta, að því gefnu að uppfærsluferli taxtabreytingar sé keyrt. Stilltu þessa dagsetningu ekki nema þú viljir að kerfið uppfæri sjálfkrafa bætur áætlana starfsmanna út frá þessu gengi. Þetta er venjulega frátekið við sjálfvirka vinnslu á framtíðarbreytingum. Gildistaka breytingartímabilsins verður að vera innan gildistaxta og gildistíma fríðinda. |
   | **Breytingu á hlutfalli lokið** | Gátreiturinn **Taxtabreytingum lokið** verður sjálfkrafa valinn þegar breytingum á taxta bótagreiðslna hefur verið lokið með frávinnslu breytinga á taxta. |

4. Veldu til að fylgjast með og viðhalda breytingum á uppbótarhlutfalli **Aðgerðir** og veldu síðan **Viðhalda útgáfum**.

5. Veljið **Vista**. 

## <a name="set-up-tier-rates"></a>Setja upp taxta fyrir lög

Þú getur notað stighlutfall í taxtauppsetningunni ef hlutfallið er mismunandi eftir ýmsum þáttum. Til dæmis gætirðu stillt stigahlutfall til að segja að ef aldur þinn er allt að 34,99 þá er upphæðin sem ekki reykir 2. Ef aldur þinn er allt að 39,99, þá er upphæðin sem ekki reykir 3.

Þú getur líka notað tvöfalt lag. Ef þú velur **Tvöfalt lag** fyrir gildið **Nota lög** á **Uppsetningu taxta** formi, þú getur skilgreint verð byggt á tveimur víddum. Til dæmis gætirðu stillt kerfi með tveimur lögum til að segja að ef þú ert karlkyns og aldur þinn er allt að 34,99 þá er upphæðin sem ekki reykir 2. Ef þú ert karlkyns og aldur þinn er allt að 39,99, þá er upphæðin sem ekki reykir 3. Ef þú ert kvenkyns og aldur þinn er allt að 34,99, þá er upphæðin sem ekki reykir 1.8. Ef þú ert kvenkyns og aldur þinn er allt að 39,99, þá er upphæðin sem ekki reykir 2.8.

> [!IMPORTANT]
> Valkostur undir **Persónulegar upplýsingar** í skrá starfsmanns er notaður til að gefa til kynna hvort starfsmaðurinn reykir. Ef starfsmaðurinn er skráður sem reykingamaður er reykingataxtinn notaður. (Starfsmaðurinn fær aldrei að sjá þessa vísun í reykingar.)
   
1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hlutföll**.

2. Veldu eitt eða fleiri verð af listanum, veldu **Aðgerðir** og veldu síðan **Taxtar fyrir lög**.

3. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | lýsing |
   | --- | --- | 
   | **Lýsing** | Reitargildið **Lýsing** er fengið úr lýsingunni í færslunni fyrir uppsetningu hlutfalls. Þetta hjálpar þér að bera kennsl á hvaða hlutfall skipulag stig stig eru tengd við. |
   | **Kóði lags** | Veldu kóða fyrir lög. Kóðar fyrir lög eru skilgreindir í gluggnaum Kóðar fyrir lög. Kerfið birtir sjálfkrafa lýsingu á kóða fyrir lög í töflunni til vinstri. |
   | **Gerð þreps** | Tilgreinir hvaða reit ætti að nota sem valviðmið fyrir útreikningsferli kóða fyrir lög. Dæmi:</br></br><ul><li>Ef **Aldur** er notaður mun kerfið nota fæðingardag starfsmannsins við útreikningsferli fríðindahlutfallsins.</li><li>Ef **Laun** eru notuð mun kerfið nota árlegt hlutfall fríðinda af launum starfsmannsins við útreikningsferli fríðindahlutfallsins.</li><li>Ef **Starfsgerð** er notuð mun kerfið nota núverandi starf starfsmanns til að ákvarða starfsgerðina með verkfærslunni sem tengist stöðunni.</li></ul></br></br>Gerðir lagsins eru **Aldur**, **Laun**, **Líkamlegt ástand**, **Kyn**, og **Jafngildi fulls starfs**, **Tegund starfs**, **Launasvæði** og **Stig**. | 
   | **Stig** | Gildið sem á að nota með tegundinni við útreikning á fríðindataxta. Dæmi:</br></br><ul><li>Ef gerð lagsins er **Aldur**, verður þetta aldursgildið.</li><li>Til dæmis: Þegar gerð lagsins er **Laun**, verður það launaupphæðin.</li><li> Til dæmis: Þegar gerð lagsins er **Starfsgerð**, verður það starfsgerðin.</li></ul></br></br>Þegar gerð lagsins er **Aldur** eða **Laun**, táknar gildið í reitnum **Stig** efri mörk lagsins. Þegar gerð lagsins er **Starfsgerð**, notar kerfið nálgun nákvæmrar samsvörunar við val á hlutfalli lags. |
   | **Reiknigerð** | Tilgreinir hvernig á að nota upphæðina í reitnum útreikningsfjárhæðar og hvaða stærðfræðiútreikning á að framkvæma ef þörf krefur. Ef útreikningsgerðin er flöt upphæð notar kerfið upphæðarsviðina eins og er. Ef útreikningsgerðin er á hverja $ upphæð af launum eða umfjöllun notar kerfið útreikningsupphæðina og útreikningsstefnuna í stærðfræðiútreikningi sínum.</br></br>Ef útreikningartegundin er á hverja $ upphæð launa notar kerfið eftirfarandi stærðfræðijöfnur:</br></br>Árleg bótagreiðsla deilt með Útreikningsupphæð (ávöl upp eða niður) sinnum upphæðir fyrir reykingamann eða ekki reykingarmann fyrir starfsmann eða vinnuveitanda.</br></br>Ef útreikningartegundin er á hverja $ upphæð tryggingar notar kerfið eftirfarandi stærðfræðijöfnur:</br></br>Tryggingarupphæð deilt með Útreikningsupphæð (ávöl upp eða niður) sinnum upphæðir fyrir reykingamann eða ekki reykingarmann fyrir starfsmann eða vinnuveitanda.</br></br>Í báðum útreikningum er útreikningsstefnan notuð til að ákvarða hvort fara skuli niður árleg hlunnindi eða tryggingarupphæð deilt með útreikningsupphæð upp eða niður. |
   | **Reikningsupphæð** | Upphæðin sem á að nota við útreikningsferli fríðinda. Þessi upphæð verður deilir í stærðfræðiútreikning á stighlutfalli. |
   | **Stefna útreiknings** | Átt jöfnunar á upphæð reiknaðrar niðurstöðu. Kerfið styður þrjár áttir útreiknings: Auða (nákvæma aðferð), **Hækkun** og **Lækkun**.</br></br><ul><li>Ef það er autt mun kerfið nota nákvæma útreikning á launum / umfjöllunarfjárhæð deilt með útreikningsupphæðinni. Ef þetta gildi hefur brot, þá mun kerfið nota þetta við útreikning.</li><li>Þegar **Hækkun** er notuð, hækkar kerfið stærðfræðilega útreikninga á launum/tryggingarupphæð sem er deilt með reikningsupphæðinni í næstu heiltölu, sem þýðir að 12,25 hækka í 13.</li><li>Þegar **Lækkun** er notuð, lækkar kerfið stærðfræðilega útreikninga á launum/tryggingarupphæð sem er deilt með reikningsupphæðinni í núverandi heiltölu, sem þýðir að 12,25 lækka í 12.</li></ul> |
   | **Upphæð starfsmanns fyrir þann sem reykir ekki** | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir þjónustuaðila fríðinda og hún ætti að vera byggð á greiðslutíðni fyrir uppsetningu taxtans. |
   | **Upphæð vinnuveitanda fyrir þann sem reykir ekki** | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir þjónustuaðila fríðinda og hún ætti að vera byggð á greiðslutíðni fyrir uppsetningu taxtans. |
   | **Upphæð starfsmanns fyrir reykingamann** | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir þjónustuaðila fríðinda og hún ætti að vera byggð á greiðslutíðni fyrir uppsetningu taxtans. |
   | **Upphæð vinnuveitanda fyrir reykingamann** | Upphæðin sem veitandi fríðinda veitir fyrir starfsmann sem reykir ekki. Þetta er upphæðin sem vinnuveitandinn greiðir þjónustuaðila fríðinda og hún ætti að vera byggð á greiðslutíðni fyrir uppsetningu taxtans. |
   | **Upphæð stjórnunar** | Stjórnsýslufjárhæð sem gjaldfærð er af þriðja aðila. Þetta er upphæðin sem vinnuveitandinn greiðir þriðja aðila og hún ætti að miðast við greiðslutíðni fyrir uppsetningu taxtans. |
   | **Hlutfall sveigjanlegra útgjalda fyrir þann sem reykir ekki** | Fjöldi flex eykur ávinningskostnaðinn, miðað við útreikninginn sem er skilgreindur fyrir stig stig fyrir ekki reykingarfólk. Til dæmis, ef útreikningartegundin er **Á $ fjárhæð umfjöllunar**, þá er útreikningsupphæðin 10.000, og sveigjanleiki sem ekki reykir er 6, þá þýðir það að ef starfsmaður sem reykir ekki reykingar velur $10,000 af umfjöllun mun það kosta 6 beygja einingar. Ef þeir velja $20,000 af umfjöllun kostar það 12 flex einingar, og svo framvegis. |
   | **Hlutfall reykingamanns fyrir sveigjanleg útgjöld** | Fjöldi flex eykur ávinningskostnaðinn, miðað við útreikninginn sem er skilgreindur fyrir stig stig fyrir reykingarfólk. |

5. Veljið **Vista**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
