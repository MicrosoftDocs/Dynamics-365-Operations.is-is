---
title: Bæta við upplýsingum kreditstjórnunar fyrir viðskiptavini
description: Þetta efni útskýrir hvernig á að bæta við upplýsingum um kreditstjórnun fyrir viðskiptavin.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 080b1c4a3887aa5f354743315dc11ffd9f089e73350429d5e08710927f6b2454
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724064"
---
# <a name="add-credit-management-information-for-customers"></a>Bæta við upplýsingum kreditstjórnunar fyrir viðskiptavini

[!include [banner](../includes/banner.md)]

Eftir að þú hefur sett upp færibreyturnar sem stjórna kreditstjórnun geturðu bætt við frekari upplýsingum fyrir hvern viðskiptavin. Þessar upplýsingar stjórna kreditstjórnunarferlunum og þær veita einnig viðbótarupplýsingar sem hjálpa meðlimum innheimtuteymisins að stjórna viðskiptavinum.

## <a name="customer-information"></a>Upplýsingar um viðskiptavin

Þú getur bætt við upplýsingum viðskiptavinarins á flýtiflipanum **Skuldir og innheimta** af síðunni **Allir viðskiptavinir** (**Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**).

1. Stilltu valkostinn **Ótakmörkuð lánamörk** á **Já** ef viðskiptavinurinn ætti ekki að vera takmarkaður af neinum prófum á lánamörkum.
2. Stilltu valkostinn **Útiloka frá kreditstjórnun** á **Já** til að útiloka viðskiptavininn frá aðgerðum sem venjulega eiga sér stað við útlánaumsýslu.
3. Veldu lánastjórnunarhóp fyrir viðskiptavininn.
4. Til að reikna út lánamörk í gjaldmiðli viðskiptavinarins slærðu inn í reitinn **Lánamörk í gjaldmiðli viðskiptavinar** lánamörk viðskiptavinarins. Lánamörkum í gjaldeyris fyrirtækisins verður umbreytt með því að nota gengi sem eru skilgreind með því hvaða lánamörk gengistegund er valin í breytum lánamála.
5. Í reitinn **Síðasta endurskoðunardagsetning** slærðu inn dagsetninguna þegar lánshæfismörk viðskiptavinarins voru síðast endurskoðuð af lánastjóri.
6. Í reitinn **Næsti áætlaði endurskoðunardagur** slærðu inn dagsetningu þegar viðskiptavinurinn er áætlaður fyrir lánshæfismat og uppfærslu.
7. Í reitinn **Hæf lánamörk** slærðu inn hæsta lánamörk sem hægt er að úthluta viðskiptavini, byggð á yfirferð þinni á lánssögu viðkomandi. Hæfileg lánamörk geta verið frábrugðin lánamörkum sem sýnd eru á flýtiflipanum **Skuldir og innheimta**.
8. Í reitinn **Hæfur gjaldmiðill lánamarka** slærðu inn gjaldmiðil gjaldgengs lánsfjárhámarks.
9. Í reitinn **Gjaldgeng dagsetning lánamarka** slærðu inn dagsetningu þegar gjaldgengt lánsfjárhámark var stofnað.
10. Í reitinn **Staða kreditlykils** slærðu inn stöðu kreditlykils viðskiptavinarins.
11. Í reitinn **Stöðuástæða** slærðu inn ástæðuna sem er tengd lykilstöðunni.
12. Stilltu valkostinn **Með umboð** á **Já** til að gefa til kynna að viðskiptavinurinn hafi verið úthlutaður á lánastofnun. Þetta gildi er aðeins til upplýsingar. Það er ekki notað í neinum lánastýringarferlum.
13. Stilltu valkostinn **Titill í bið** á **Já** til að gefa til kynna að titill sé í bið fyrir félagið. Þetta gildi er aðeins til upplýsingar. Það er ekki notað í neinu lánastýringarferli.
14. Í reitinn **Upphafsdagur viðskipta** slærðu inn dagsetninguna þegar viðskiptavinurinn byrjaði fyrst að eiga viðskipti. Þessar upplýsingar eru notaðar þegar áhættumat er búið til.
15. Í reitinn **Viðskiptavinur frá** slærðu inn dagsetninguna þegar fyrstu færslurnar voru afgreiddar fyrir viðskiptavininn. Þessar upplýsingar eru notaðar þegar áhættumat er búið til.
16. Sláðu inn athugasemdir sem lánsteymið getur notað til að meta frekar lánstraust viðskiptavinarins.

Athugaðu að sumar upplýsingarnar sem sýndar eru á síðunni **Viðskiptavinur** eru stofnaðar af öðru ferli:

- Reiturinn **Lokadagur lánamarks** sýnir dagsetninguna þegar lánamörkin renna út. Ef þú stillir þennan reit ekki renna lánamörk viðskiptavinarins ekki út.
- Reiturinn **Dagsetning lánamarks** sýnir dagsetninguna þegar lánamörkin voru stofnuð. Þessi reitur er uppfærður í hvert skipti sem lánsfjármörkin eru leiðrétt.
- Tímabundin lánamörk fara yfir lánamörk viðskiptavina um tíma. Þau eru notuð í stað lánamarka til að reikna út heildarlánamörk. Þessar upplýsingar eru aðeins sýndar ef virk lánamörk eru fyrir hendi. Þú getur bætt tímabundnum lánamörkum með leiðréttingum á lánamörkum.
- Reiturinn **Tryggingar og ábyrgðir** sýnir heildarverðmæti trygginga og ábyrgða sem geta aukið lánamörk viðskiptavinarins.
- Reiturinn **Heildarlánsmarka** sýnir lokalánamörk viðskiptavinarins. Í heildarhámörkum eru tryggingar og ábyrgðir og tímabundin lánamörk.

## <a name="temporary-credit-limits"></a>Tímabundin lánamörk

Tímabundin lánamörk fara yfir lánamörk viðskiptavina um skilgreindan tíma. Þú getur bætt tímabundnum lánamörkum með því að nota leiðréttingar á lánamörkum. Leiðréttingar á lánamörkum gera lánastjórnendum kleift að uppfæra lánamörk og gildistíma eins viðskiptavinar, hóps viðskiptavina eða allra viðskiptavina með bókunarferli.

Þú getur búið til aðlögunarfærslur fyrir lánamörk á síðunni **Leiðréttingar á lánamörkum** (**Lánastjórnun \> Leiðréttingar á lánamörkum \> Leiðréttingar á lánamörkum**).

## <a name="create-insurance-policies-and-guarantees"></a>Búðu til tryggingar og ábyrgðir

Þú getur búið til eina eða fleiri tryggingar og ábyrgðir fyrir hvern viðskiptavin. Þú getur síðan notað þær til að reikna út þá áhættu sem fyrirtækið þitt hefur þegar það býður viðskiptavini lánstraust. Vátryggingarskírteini og ábyrgðir geta einnig verið innifalin í lánamörkum viðskiptavinar.

Þú getur búið til tryggingar og ábyrgðir á síðunni **Allir viðskiptavinir** (**Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**). Veldu viðskiptavin og síðan á aðgerðasvæðinu á flipanum **Kreditstjórnun** velurðu **Tryggingar og ábyrgðir**.

> [!NOTE]
> Í eftirfarandi ferli velurðu vátryggjanda eða ábyrgðarmann úr altækri aðsetursbók. Þess vegna verður þú að ganga úr skugga um að vátryggjendum og ábyrgðarmönnum hefur verið bætt við altæku aðsetursbókina áður en þú byrjar á þessu ferli.

1. Í reitinn **Kennimerki** slærðu inn **Ábyrgð** eða **Tryggingar**.
2. Í reitnum **Gerð ábyrgðar/tryggingar** velurðu eina af ábyrgðar- eða tryggingagerðunum sem þú hefur áður sett upp.
3. Í reitnum **Vátryggjandi/ábyrgðarmaður** velurðu vátryggjanda eða ábyrgðarmann úr altækri aðsetursbók. 
4. Ef þú valdir **Tryggingar** í reitnum **Kennimerki** skaltu í reitnum **Gerð tryggingarreglu** velja eina af tryggingargerðum sem þú hefur áður sett upp. Þú getur ekki valið gerð tryggingarreglu fyrir ábyrgð.
5. Í reitinn **Auðkenni** slærð inn kenni reglunnar. Þetta kenni er venjulega reglunúmer.
6. Í reitnum **Virkt** slærðu inn upphafsdagsetningu vátryggingarskírteinisins eða ábyrgðarinnar.
7. Í reitnum **Lok gildistíma** slærðu inn dagsetninguna þegar vátryggingarskírteinisins eða ábyrgðarinnar. rennur út.
8. Í reitnum **Virði** slærðu inn virði vátryggingarskírteinisins eða ábyrgðarinnar. Þetta virði er fullt virði stefnunnar.
9. Í reitnum **Gjaldmiðill** velurðu gjaldmiðil fyrir virði reglunnar. 
10. Í reitnum **Uppfæra lánamörk** tilgreinirðu prósentu á milli **0** og **100**. Þessum prósentum verður beitt á vátryggingarvirðið og upphæðin, sem af því hlýst, verður notuð til að hækka lánsheimildina sem notuð er við útreikninga á lánamörkum. Reiknað gildi er sýnt undir **Heildarlánamörk, tryggingar og ábyrgðir** á flýtiflipanum **Skuldir og innheimta** á síðunni **Viðskiptavinir**.

    Eftirfarandi er dæmi:

    - Lánamarkið (A) er 100.000.
    - Vátryggingarvirðið (B) er 50.000.
    - Hlutfall **Uppfæra lánamörk** (C) er 50,00.
    
    Í þessu tilfelli er virkt lánsfjárhámark 125.000 (= A + \[B × C\]).

11. Veldu gátreitinn **Innifalið í útsetningu** til að draga úr lánamörkum sem notuð eru við útreikninga á lánamörkum að fullu gildi stefnunnar. Ef þessi gátreitur er valinn verður gildi sem reiknað er þegar hlutfallið **Uppfæra lánamörk** er tilgreint ekki notað í útreikningum á lánamörkum.

    Eftirfarandi er dæmi:

    - Lánamarkið (A) er 100.000.
    - Vátryggingarvirðið (B) er 50.000.
    - Hlutfall **Uppfæra lánamörk** (C) er 50,00.

    Í þessu tilfelli er virkt lánsfjárhámark 125.000 (= A + \[B × C\]).
    
    Hins vegar, ef þú velur gátreitinn **Innifalið í útsetningu** er virðið **Uppfæra lánamörk** upp á 50.000 (= 50,00 prósent af 100.000) fjarlægt og útsetningargildið er 75.000 (= A + \[B × C\] - B).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]