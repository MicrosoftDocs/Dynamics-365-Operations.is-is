---
title: Formúlur og formúluútgáfar
description: Þetta efnisatriði veitir upplýsingar um formúlur og formúluútgáfur. Formúla skilgreinir efni, innihaldsefni og niðurstöður tiltekins ferils í framleiðsluferli. Formúlur eru notaðar til að skipuleggja og framleiða vörur í framleiðsluferli.
author: cvocph
manager: tfehr
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule, EcoResProductProdTypeFormulaNoActiveFormulaFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee15fc2a3edd9d0cc8cff17123981bc90ceeff2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246190"
---
# <a name="formulas-and-formula-versions"></a>Formúlur og formúluútgáfar

[!include [banner](../includes/banner.md)]

Formúla skilgreinir efni, innihaldsefni og niðurstöður tiltekins ferils í framleiðsluferli. Ásamt samsvarandi leið skilgreinir formúlan allt ferlið í framleiðsluferli. Formúlur eru notaðar til að skipuleggja og framleiða vörur í framleiðsluferli.

Formúla samanstendur af innihaldsefnum og magni sem þarf til að framleiða tiltekið magn af formúluatriði. Þú hefur aðgang að formúluvirkni úr birgðum og vörustjórnun eða afurðaupplýsingastjórnun, eftir því hvaða verk þú ert að framkvæma.

## <a name="formulas-and-formula-lines"></a>Formúlur og formúlulínur
Formúla samanstendur af einni eða fleiri formúlulínum sem auðkenna innihaldsefni eða hluti sem mynda formúluna. Formúlulína getur innhaldið uppskriftarvöruhluti, formúluvörur, afla, keyptar vörur, aukaafurðir eða hliðarafurðir. Vegna þess að margir hlutir eru notaðir í mörgum vörum er hægt að nota hlut í fleiri en einni formúlu.

Dæmi um formúlu er formúla fyrir súkkulaðibitaköku. Innihaldsefni þessarar formúlu nota margar línur, eins og hveiti, sykur, egg, smjör og súkkulaðibita. Formúlan fyrir súkkulaðibitakökur inniheldur innihaldsefni sem eru líklega notuð í öðrum formúlum. Þegar þú býrð til súkkulaðibitakökur kunna að vera afgangar, á borð við mola, eða sumar af smákökum gæti verið ofbakaðar eða of lítið bakaðar. Hægt er að setja þessa hluti upp sem aukaafurð eða hliðarafurð, allt eftir framleiðsluaðgerðum.

Þegar þú býrð til formúlulínu notar þú línugerðina til að gefa til kynna hvernig kerfið ætti að höndla línuna þegar þú keyrir áætlanagerð og framleiðir runupantanir. Sérhver línugerð gefur mismunandi niðurstöður. Eftirfarandi tafla lýsir línugerðunum sem þú getur valið. 

| Línugerð     | lýsing  |
|---------------|--------------|
| vara          | Veljið **Vara** þegar varan er hráefni eða vara, sem er næstum tilbúin og er tekin úr birgðum, eða þegar varan er þjónusta. |
| Skugga       | Veldu **Skugga** þegar ætlunin er að brjóta niður lægri stig af formúluvörur sem eru í formúlulínunni. Þegar runupöntunin er metin og formúluvaran er brotin niður eru íhlutirnir skráðir sem formúlulínur í runupöntuninni. Að auki er samsvarandi leiðum bætt við framleiðsluleiðina. Formúluvörur eru brotnar niður með gildandi skilgreiningu. Þegar línugerðin **Skugga** er notuð er hægt að annast framleiðslu- og mælingarskilgreiningar sem eiga sér stað í mismunandi formúlustigum. Ef þú velur **Phantom** fyrir vöru á **Verkfræðingur** flýtiflipanum á **Upplýsingar um losaðar afurðir** síðunni og notar svo þessa vöru í formúlu er gerð formúlulínunnar breytt í **Skugga**. Ekki er hægt að velja **Skugga** fyrir atriði fyrir þyngd afurðar, eða fyrir vörur þar sem vörugerðin er **Aukaafurð**, **Hliðarafurð** eða **Áætlunarvara**. |
| Þarfaraktar birgðir | Veljið **Fest framboð** til að búa til runupöntun, framleiðslupöntun, kanban, flutningspöntun eða innkaupapöntun fyrir innihaldsefni sem er að finna á formúlulínu. Samsvarandi röð er ákvörðuð miðað við stillingar sjálfgefinnar raðar og framleiðslutegund innihaldsefnisins og er búin til þegar runupöntunin er metin. Nauðsynlegt magn innihaldsefna eru frátekin fyrir runupöntunina. |
| Lánardrottinn        | Veljið **Lánardrottinn** ef framleiðsluferlið notar undirverktaka og ætlunin er að stofna undirframleiðslu eða innkaupapöntun fyrir undirverktakann. Þjónustan eða vinnan sem undirverktaki framkvæmir verður að vera búin til með formúluvöru eða þjónustuvöru. Hægt er að tengja vöruna við yfirvöruna sem formúlulínu. Leiðin verður að innihalda aðgerð sem er úthlutað til rekstrartilföng undirverktakans. Aðgerðin er fest við formúlulínuna með því að nota **Aðg.nr** reit. |

## <a name="formula-versions"></a>Formúluútgáfur
Þegar ný formúla er búin til verður fyrst að búa til formúluútgáfu áður en formúlulínuhlutunum og sérstökum eiginleikum þeirra er bætt við. Hver formúla verður að hafa að minnsta kosti eina útgáfu. Hnappurinn **Samþykkt** á formúluútgáfu verður aðeins aðgengilegur eftir að útgáfufærsla hefur verið vistuð. Hver formúluútgáfufærsla er tengd einum eða mörgum aukaafurðum og hliðarafurðum sem hægt er að framleiða þegar fullunnin vara er framkvæmd. Hægt er að búa til margar vörur úr sömu innihaldsefnum í mismunandi runustærðum, í margföldun, eða með mismunandi ávöxtun. Hægt er að búa til eins margar útgáfur formúlu og þarf.

Til að stjórna mörgum virkum formúluútgáfum skal nota gildisdagsetninguna „frá“ í magnreitum. Margir virkar formúluútgáfur geta aðeins verið til ef dagsetningarsviðið og "frá" magn skarast ekki.

Ólíkt uppskriftum, þar sem ein uppskrift tengist oft mörgum uppskriftarútgáfum, er yfirleitt aðeins til ein formúluútgáfa fyrir hverja formúlu. Hafa skal í huga að aðeins er hægt að virkja eina formúluútgáfu fyrir þekjuvíddir og magn fyrir tiltekna vöru. Hins vegar geta margar formúluútgáfur verið til af öðrum ástæðum og hægt er að velja þær handvirkt þegar runupöntun er búin til.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Samþykkja og virkja formúlur og formúluútgáfur.
Formúlur og formúluútgáfur verður að samþykkja áður en hægt er að nota þær í áætlun og framleiðslu. Formúlur eru venjulega virkjaðar áður en þær eru notaðar. Meðan á framleiðslu stendur er hins vegar hægt að velja formúluútgáfu sem er samþykkt, en ekki virkjuð.

Til að tryggja formúlu- eða formúluútgáfu er hægt að stilla **Loka fyrir breytingar** og **Loka fyrir fjarlægingu á samþykki** á síðunni **Færibreytur framleiðslustýringar**.

Ef þú velur **Loka fyrir breytingar** og formúlan er samþykkt er ekki hægt að eyða eða breyta neinum reitum á formúlulínum. Ef þú hins vegar fjarlægir samþykki formúlunnar er hægt að eyða og breyta formúlulínunum. Einnig er hægt að stofna nýjar formúlur og nýjar formúluútgáfur.

Ef þú velur **Loka fyrir fjarlægingu á samþykki** er ekki hægt að fjarlægja samþykki samþykktrar formúlu eða formúluútgáfu. Þú getur hins vegar búið til nýjar formúlur og nýjar formúluútgáfur og fjarlægt virkjun formúluútgáfunnar.

Hægt er að bæta við fleiri stigum stýringar með því að nota rafræna undirskrift. Þegar notandi er settur upp þannig að rafrænnar undirskriftar sé krafist þegar formúla er samþykkt birtist síðan **Undirskrift** þegar formúlan er virkjuð. Notandinn verður að hafa heimild til að undirrita rafrænt og vottorðið verður að vera sannreynt áður en breytingin fer fram. Ef ekki er hægt að sannreyna undirskriftina er samþykki eða fjarlæging samþykkis hafnað og breytingin sem hófst með samþykki eða fjarlægingu samþykkis er afturkölluð.

## <a name="use-the-scalable-feature"></a>Nota kvörðunareiginleika
Aðeins er hægt að nota kvörðunareiginleikann ef allir íhlutir vörunnar í formúlunni eru stilltir á **Breytileg notkun**. Aðgerðin er ekki tiltæk ef íhlutir vöru eru stilltir á **Föst notkun** eða **Skrefanotkun**. Þegar kvörðunareiginleiki er notaður breytist magn annarra innihaldsefna í formúlu ef einu innihaldsefni er breytt. Einnig er stærð formúlunnar leiðrétt. Ef formúlustærð er breytt breytist magn allra kvarðanlegra efna. Þessi eiginleiki er sérstaklega ætlaður til að búa til og viðhalda formúlu. Það sýnir ekki hvort magn innihaldsefnis verði minnkað upp eða niður í runupöntun.

## <a name="use-step-consumption"></a>Nota skrefanotkun
Með skrefaneyslu þarf ekki að slá inn magn á flipann **Formúlulína** fyrir innihaldsefni. Í staðinn er skrefaneysla stillt þannig að það hefur gildi **Frá-röð** og **Magn**. Upplýsingarnar úr skrefaneyslu eftir skrefafærslu sem passar við magnið á runupöntuninni eru þess í stað valdar. Skrefanotkun er gagnleg þegar neysluhlutfallið er ekki línulegt við runupöntunarstærð og eykur aðeins kröfur þegar tilteknum magnþröskuldi er náð. Til að virkja þennan eiginleika fyrir nýja formúlu skal, undir **Útreikningur notkunar**, breyta formúlustillingu fyrir viðeigandi innihaldsefni úr **Venjulegt** í **Skref**. Þessi neysluaðferð er tilgreind á flipanum **Uppsetning** á síðunni **Formúlulína**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]