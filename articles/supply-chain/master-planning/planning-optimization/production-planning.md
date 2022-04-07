---
title: Framleiðsluáætlun
description: Þetta efnisatriði lýsir áætlanagerð fyrir framleiðslu og útskýrir hvernig á að breyta áætluðum framleiðslupöntunum með því að nota fínstillingu skipulagningar.
author: t-benebo
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8f23cb62512dfd718fe199867a4b21aaa0eca3fd
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469059"
---
# <a name="production-planning"></a>Framleiðsluáætlun

[!include [banner](../../includes/banner.md)]

Fínstilling skipulagningar styður nokkrar framleiðsluaðstæður. Ef verið er að flytja sig úr fyrirliggjandi innbyggðri aðaláætlunarvél er mikilvægt að gera sér grein fyrir breyttri hegðun.

Eftirfarandi myndband gefur stutta kynningu á sumum þeirra hugtaka sem fjallað er um í þessu efnisatriði: [Dynamics 365 Supply Chain Management: Viðbætur við fínstillingu skipulagningar](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Kveikja á þessum eiginleika fyrir kerfið

Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessu efnisatriði skal fara í [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Áætlaðar framleiðslutillögur fyrir fínstillingu áætlanagerðar*.

## <a name="planned-production-orders"></a>Framleiðslutillögur

Þegar aðaláætlanagerð stofnar áætlaðar pantanir til að uppfylla kröfur er pöntunargerðin ákvörðuð af gildinu í reitnum **Gerð áætlaðrar pöntunar**. Ef reiturinn **Gerð áætlaðrar pöntunar** er stilltur á *Framleiðsla*, eru áætlaðar framleiðslupantanir stofnaðar. Í þessum áætluðu framleiðslupöntununum eru upplýsingar um virku uppskriftirnar og kenni leiðar úr tengdri uppsetningu framleiðslu.

## <a name="requirements-from-boms"></a>Kröfur úr uppskriftum

Upplýsingar um uppskrift eru teknar inn í myndina í aðaláætlanagerð. Útkoma áætlunarinnar felur í sér framboð á efni til að ná yfir tengda eftirspurn eftir efni fyrir framleiðslu.

Við aðaláætlanagerð er núgildandi virk uppskrift notuð til að ákveða efnin sem þarf fyrir framleiðslu. Þetta skref er gert í gegnum öll skipulagsstig uppskriftar sem tengist nauðsynlegri framleiðslupöntun. Efnisþörf er uppfyllt með því að nota tiltækar birgðir á lager, fyrirliggjandi framboð í pöntun og samþykktar áætlaðar pantanir. Ef meira efni þarf einhvers staðar verður áætluð pöntun stofnuð til að mæta eftirspurninni.

## <a name="scheduling-during-firming"></a>Áætlanagerð við staðfestingu

Áætlaðar framleiðslupantanir innihalda leiðakennið sem er nauðsynlegt fyrir framleiðsluröðun. Hins vegar er stuðningur áætlanagerðar í bið á meðan á keyrslu áætlunar stendur fyrir áætlaðar pantanir. Leiðarkennið er notað til að tímasetja áætlaðar framleiðslupantanir við staðfestingu. Þess vegna getur afhendingartími á áætluðum framleiðslupöntunum verið frábrugðinn afhendingartíma á tengdri áætlun, staðfestum framleiðslupöntunum sem eru myndaðar úr þeim, eins og lýst er hér:

- **Áætluð framleiðslupöntun** – Afhendingartími er byggður á föstum afhendingartíma úr útgefinni afurð.
- **Staðfest framleiðslupöntun** – Afhendingartími er byggður á áætlanagerð sem notar upplýsingar um leið og tengdar takmarkanir tilfanga.

Frekari upplýsingar um væntanlegt framboð eiginleikans er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).

Ef treyst er á virkni framleiðslu sem er ekki í boði sem stendur fyrir fínstillingu skipulagningar er hægt að halda áfram að nota innbyggðu aðaláætlunarvélina. Engar undantekningar eru nauðsynlegar.

## <a name="delays"></a>Seinkanir

Ef afhendingartími fyrir nauðsynlegt efni er lengri en tímabilið frá deginum í dag og til dagsetningar efnisþarfa, verður áætlaðri pöntun fyrir nauðsynlegt efni og tengda framleiðslupöntun frestað. Fyrir áætlaðar pantanir er seinkunin (í dögum) reiknuð út frá afhendingartíma útgefinnar afurðar. Upplýsingum um seinkun er síðan komið áleiðis í gegnum öll skipulagsstig uppskriftar. Þess vegna er hægt að fylgjast með áhrifum seinkaðra hráefna alla leið að sölupöntun viðskiptavinar.

## <a name="modifying-planned-orders"></a>Breyta áætluðum pöntunum

Þegar upplýsingum er breytt á áætlaðri pöntun birtast eftirfarandi skilaboð: „Hafið í huga að áhrif handvirkra breytinga á tillögur munu ekki koma fram í afganginum af áætluninni fyrr en við næstu keyrslu áætlunargerðar.“

Ef á að breyta upplýsingum um áætlaða pöntun og sjá áhrifin á tengda efnisþörf skal fylgja þessum skrefum.

1. Uppfærið áætluðu pöntunina.
2. Samþykkja áætlaða pöntun.
3. Keyra áætlanagerð.

Þegar aðaláætlanagerð er keyrð ætti ekki að nota síur ef áætlaðar framleiðslupantanir eru teknar með. Nánari upplýsingar er að finna í hlutanum [Síur](#filters) síðar í þessu efnisatriði.

> [!NOTE]
> Ef afhendingardagsetningu áætlaðrar pöntunar er breytt í síðari dagsetningu gæti eftirspurnin verið fest við nýja áætlaða pöntun. Þessi hegðun á sér stað þegar nýja birgðadagsetningin veldur töfum á festri eftirspurn en, samkvæmt stillingum afhendingartíma, er hægt að komast hjá seinkuninni.

## <a name="explosion-page"></a>Niðurbrotssíða

Hægt er að nota síðuna **Niðurbrot** til að greina eftirspurnina sem þarf fyrir tiltekna framleiðslupöntun eða áætlaða framleiðslupöntun, tengt umfang og upplýsingar um þarfarakningu. Upplýsingar á síðunni **Niðurbrot** eru uppfærðar við aðaláætlanagerð. Ekki er hægt að uppfæra upplýsingarnar beint af síðunni **Niðurbrot**.

## <a name="filters"></a><a name="filters"></a>Síur

Til að tryggja að fínstilling skipulagningar sé með upplýsingarnar sem þarf til að fá út rétta útkomu við útreikning þarf að hafa með allar afurðir sem á einhvern hátt tengjast afurðunum í öllu skipulagi uppskriftar fyrir áætluðu pöntunina. Fyrir aðstæður áætlanagerðar sem fela í sér framleiðslu er mælt með að forðast síaðar keyrslur aðaláætlanagerðar.

Þó að háðar undireiningar séu sjálfkrafa greindar og hafðar með í keyrslum aðaláætlanagerðar þegar innbyggð aðaláætlunarvél er notuð, þá framkvæmir fínstilling skipulagningar ekki þessi aðgerð eins og er.

Til dæmis ef einn bolti úr skipulagi uppskriftar fyrir afurð A er einnig notaður til að framleiða afurð B, þá verður að hafa með allar afurðir í skipulagi uppskriftar fyrir afurðir A og B í síuninni. Það getur verið mjög flókið að ganga úr skugga um að allar afurðir séu hluti af síunni og þar af leiðandi er mælt með að forðast keyrslur á síaðri aðaláætlanagerð þegar framleiðslupantanir eru hafðar með. Annars koma óæskilegar niðurstöður út úr aðaláætlanagerðinni.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Ástæður til að forðast síaðar keyrslur aðaláætlanagerðar

Þegar keyrð er síuð aðaláætlanagerð fyrir afurð ber fínstilling skipulagningar (ólíkt innbyggðri aðaláætlunarvél) ekki kennsl á allar undirafurðir og hráefni í skipulagi uppskriftar fyrir þessa afurð og hefur þær því ekki með í keyrslu aðaláætlanagerðar. Þótt fínstilling skipulagningar greinir fyrsta stigið í skipulagi uppskriftar fyrir afurðina, hleður hún ekki neinum afurðarstillingum (á borð við sjálfgefinni pöntunargerð eða vöruþekju) úr gagnagrunninum.

Í fínstillingu skipulagningar er gögnum fyrir keyrsluna hlaðið á undan og setur á síurnar. Þetta þýðir að ef undirafurð eða hráefni sem er hluti af tiltekinni afurð er ekki hluti af síunni, verða upplýsingar um hana ekki sóttar fyrir keyrsluna. Auk þess, ef undirafurðin eða hráefnið er einnig haft með í annarri afurð, þá myndi síuð keyrsla sem inniheldur aðeins upprunalega afurð og þætti hennar fjarlægja fyrirliggjandi áætlaða eftirspurn sem var búin til fyrir þessa aðra afurð.

Þessi rök geta valdið því að síaðar aðaláætlunarkeyrslur skili óvæntum niðurstöðum. Í eftirfarandi hlutum eru gefin upp dæmi sem sýna óvæntu niðurstöðurnar sem gætu komið upp.

### <a name="example-1"></a>Dæmi 1

Fullunnin vara *FG* samanstendur af eftirfarandi þáttum:

- Hráefni *R*
- Undirvara *S1*, sem samanstendur af undirvöru *S2*

Lagerbirgðir eru til staðar fyrir hráefnið *R* en undirafurðin *S1* er ekki til staðar í birgðunum.

Þegar gerð er síuð keyrsla aðaláætlanagerðar fyrir fullunna vöru *FG* kemur út áætluð framleiðslupöntun fyrir fullunnu vöruna *FG*, áætluð innkaupapöntun fyrir hráefnið *R* og áætluð innkaupapöntun fyrir undurafurðina *S1*. Þetta er óæskileg niðurstaða vegna þess að fínstilling skipulagningar hefur hunsað fyrirliggjandi framboð á hráefninu *R* og framleiða þarf undirafurðina *S1* með því að nota *S2* frekar en að panta beint. Þetta gerðist vegna þess að fínstilling skipulagningar er aðeins með lista yfir þættina fyrir fullunna vöru *FG* án tengdra upplýsinga, eins og núverandi framboð á þáttum hennar eða sjálfgefnum pöntunarstillingum.

### <a name="example-2"></a>Dæmi 2

Með hliðsjón af fyrra dæmi notar aukaleg fullunnin vara *FG2* einnig undirafurðina *S1*. Áætluð pöntun er til fyrir fullunna vöru *FG2* og áætluð eftirspurn er til fyrir alla þætti hennar, þ.m.t. *S1*.

Þú ákveður að leysa úr óæskilegum niðurstöðum á síaðri keyrslu aðaláætlanagerðar úr fyrra dæminu með því að bæta öllum undirafurðunum og hráefnunum úr skipulagi uppskriftar á fullunninni vöru *FG* við síuna og síðan keyra fulla endurmyndun.

Þegar full endurmyndun er keyrð eyðir kerfið öllum fyrirliggjandi niðurstöðum fyrir allar innifaldar afurðir og endurgerir síðan niðurstöðurnar samkvæmt nýju útreikningunum. Þetta þýðir að fyrirliggjandi áætlaðri eftirspurn eftir afurð *S1* er eytt og síðan endurgerð þar sem aðeins er tekið tillti til krafna fullunninnar vöru *FG* á meðan kröfur fullunninnar vöru *FG2* eru hunsaðar. Þetta gerist vegna þess að þegar fínstilling skipulagningar er keyrð felur hún ekki í sér áætlaða eftirspurn annarra áætlaðra framleiðslupantana&mdash;aðeins áætlaða eftirspurn sem myndast þegar keyrslan er notuð.

> [!NOTE]
> Ef fyrirliggjandi áætluð pöntun á fullunninni vöru *FG2* er með stöðuna *Samþykkt*, þá verður samþykkt áætluð eftirspurn höfð með jafnvel þótt yfirafurðinni sé ekki bætt við síuna.

Þar af leiðandi, nema öllum þáttum fullunninnar vöru *FG* er bætt við, er fullunnin vara *FG2* og allar aðrar afurðir sem þessir þættir eru hluti af (ásamt þáttum þeirra), mun síuð keyrsla aðaláætlanagerðar skila óæskilegum niðurstöðum.

Það getur verið mjög flókið að ganga úr skugga um að allar afurðir séu hluti af síunni og þar af leiðandi er mælt með að forðast keyrslur á síaðri aðaláætlanagerð þegar framleiðslupantanir eru hafðar með.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
