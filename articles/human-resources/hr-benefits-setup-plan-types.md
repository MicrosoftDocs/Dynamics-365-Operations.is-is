---
title: Yfirlit áætlunargerðar
description: Áætlunargerð í Microsoft Dynamics 365 Human Resources er há stigi flokkun á tilteknum tegundum af fríðindum.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ca14156c165ca3f536fc0120ebd03883284eb18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337306"
---
# <a name="plan-type-overview"></a>Yfirlit áætlunargerðar

[!include [banner](../includes/preview-banner.md)]

Áætlun gerð er há stigi flokkun á tilteknum tegundum af fríðindum. Hver áætlunartegund hefur kóða gerð áætlunar sem ákvarðar reglur fyrir gerð áætlunarinnar. Til dæmis mun áætlunargerðin **Grunnlíf** fá kóðann **Líf** í áætlunargerðina vegna þess að hún er tegund af líftryggingu og verður að falla undir reglur sem hafa verið settar fram fyrir áætlunargerðarkóðann **Líf**. Önnur áætlunargerð gæti verið **Viðbótarlíf**. Þessi áætlunargerð mun einnig fá áætlunargerðarkóðann **Líf**.

Hver áætlunartegund gefur til kynna hvort starfsmaður geti skráð sig í eina áætlun af sinni gerð eða margfeldi. Starfsmaður gæti til dæmis viljað geta skráð sig í bæði stefnurnar **Grunnlíf** og **Viðbótarlíf** í áætlunargerð lífs. Starfsmanni væri líklega leyft að skrá sig í eina stefnu af gerðinni Medical.

Ef áætlunartegundir fela í sér tengiliði, sýnir áætlunartegundin hvort tengiliðir séu styrkþegar eða á framfæri. Til dæmis hefði áætlunargerðin **Grunnlíf** verði með rétthöfum á meðan einföld sjúkratrygging hefði verið með aðstandendum. Í sumum tilvikum er ekki víst að nein persónuleg tengsl séu í áætlun. Til dæmis sveigjanlegur útgjaldareikningur eða bílastæðagreiðsla.


Áætlunartegundir geta skilgreint valkosti umfjöllunar. Valkostir tryggingar eru skilgreindir á síðunni **Tryggingarvalkostir**. Með umfjöllunarvalkosti er hægt að tilgreina fjárhæð bóta eða þá tengiliði sem eiga kost á áætlunartegundinni. Ef gerð tengiliðar er til dæmis **Rétthafi** ætti tryggingarvalkosturinn að skilgreina skilmálana um hvað rétthafi hefur rétt á að fá þegar fríðindin eru nýtt. Ef gerð tengiliðar er **Aðstandandi** ætti tryggingarvalkosturinn að skilgreina tengslin milli aðstandanda og starfsmanns. 

> [!IMPORTANT]
> Síðan **Áætlunargerðir** inniheldur helstu gögn sem hafa áhrif á valkosti sem eru tiltækir þegar nýtt fríðindaáætlun er búin til:
>
> - **Kóði áætlunargerðar** – Þessi reitur hefur áhrif á það sem er sýnt í flipanum **Skilgreining** þegar raunveruleg fríðindi eru sett upp.  
> - **Samhliða skráning** – Þessi reitur ákvarðar hvort margar skráningar eru leyfðar. (Fyrir sjúkratryggingu er reiturinn yfirleitt stilltur á **Ein skráning**.)
> - **Gerð tengiliðar** – Þessi reitur gerir kleift að bæta aðstandendum eða tryggingarþegum við áætlun. Ef hann er stilltur á **Ekkert** munu starfsmenn sem skrá sig fyrir fríðindum ekki möguleikann á að velja annaðhvort tryggingarþega eða aðstandanda.
> - **Tryggingarvalkostir** – Notaðu þennan reit til að tengja tryggingarvalkostina við áætlunargerðirnar. Hann skilgreinir annaðhvort einstaklingana sem falla undir þessa áætlunargerð eða tryggingaupphæðirnar sem eru í boði fyrir þessa áætlunargerð. Til dæmis er hægt að tilgreina að trygging vegna sjúkratryggingar verði eingöngu í boði fyrir starfsmanninn, starfsmanninn og einn annan einstakling eða starfsmanninn og fjölskylduna hans.

## <a name="create-plan-types"></a>Stofna gerðir áætlana

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Áætlunargerðir**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Gerð áætlunar** | Einstakt nafn sem auðkennir gerð áætlunarinnar. |
   | **Lýsing** | Lýsing á áætlunargerð. |
   | **Gerð kóða áætlunargerðar** | Veljið áætlunargerðarkóða úr í fellilistagildunum. Númeralisti áætlunartegundarinnar sýnir allar áætlunartegundir sem eru studdar í núverandi útgáfu. |
   | **Samhliða skráning** | Tilgreinir hvort starfsmaður geti skráð sig í margvíslegar fríðindaáætlanir af sömu áætlunartegund eða eingöngu einni fríðindaáætlun á hverja áætlunartegund. |
   | **Gerð tengiliðar** | Tilgreinir hlutverk persónulegs tengiliðar. Gildin eru auð, háð og rétthafi. Þú getur haft **Tengiliðagerð** auðan ef áætlunartegund þeirra þarfnast ekki háðs eða rétthafa miðað við tryggingarvalkostinn. |

4. Veldu til að stilla valkosti fyrir lífatburði **Aðgerðir** og veldu síðan **Valkostir fyrir viðburði**. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Gerð áætlunar** | Gerð áætlunarinnar til að stilla valkosti viðburða fyrir. |
   | **Auðkenni gerðar viðburðar** | Auðkenni tegundar atburðar í lífinu. |
   | **Breyta tryggingarvalkosti** | Tilgreinir hvort starfsmaður geti sagt upp breytt tryggingakostum meðan á viðburði stendur. |
   | **Breyta í nýja áætlun** | Tilgreinir hvort starfsmaður geti sagt upp breytt áætlunum meðan á viðburði stendur. |
   | **Opna sjálfkrafa aftur hæfnisathugun** | Tilgreinir hvort opna eigi sjálfkrafa aftur hæfnisathugun fríðindaskráningar á meðan viðburðinum stendur. |
   | **Skráningartímabil lífsviðburða** | Tilgreinir tilkynningarglugga viðburðar í dögum. **Athugið**: Ef þú slærð ekki inn upphæð gerir kerfið ráð fyrir að skýrsluglugginn sé núll og afgreiði ekki viðburðinn. |
   | **Aðeins stjórnendur geta breytt** | Tilgreinir hvort kerfisstjórar geti hætt við eða breytt áætlun meðan á lífsatburði stendur. Engar breytingar geta verið gerðar af starfsmanni í **Sjálfsafgreiðsla starfsmanna** vinnurými. |
   | **Hætta sjálfkrafa við áætlun** | Tilgreinir hvort áætlun eigi að hætta sjálfkrafa meðan á lífsatburði stendur. Eftir að lífsatburðarbreytingar eru unnar, er **Sjálfvirk hætta við áætlun** valkostur mun halda áætlunarvalinu. Aðeins **Staðfest** eða **Skoðaði** staða verður fjarlægð. Áætlunin er áfram valin. Þess vegna munu starfsmenn sem velja ekki áætlun á skráningartímabili lífsviðburða ekki missa áætlunarvalið. 

5. Veldu **Vista**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
