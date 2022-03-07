---
title: Framleiðsluáætlun
description: Þetta efnisatriði lýsir áætlanagerð fyrir framleiðslu og útskýrir hvernig á að breyta áætluðum framleiðslupöntunum með því að nota fínstillingu skipulagningar.
author: ChristianRytt
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 22b78f44940f71097ca8b1cdb74edb06274bba75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839224"
---
# <a name="production-planning"></a>Framleiðsluáætlun

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

Fyrir aðstæður áætlanagerðar sem fela í sér framleiðslu er mælt með að forðast síaðar keyrslur aðaláætlanagerðar. Til að tryggja að fínstilling skipulagningar sé með upplýsingarnar sem þarf til að fá út rétta útkomu við útreikning þarf að hafa með allar afurðir sem á einhvern hátt tengjast afurðunum í öllu skipulagi uppskriftar fyrir áætluðu pöntunina.

Þó að háðar undireiningar séu sjálfkrafa greindar og hafðar með í keyrslum aðaláætlanagerðar þegar innbyggð aðaláætlunarvél er notuð, þá framkvæmir fínstilling skipulagningar ekki þessi aðgerð.

Til dæmis ef einn bolti úr skipulagi uppskriftar fyrir afurð A er einnig notaður til að framleiða afurð B, þá verður að hafa með allar afurðir í skipulagi uppskriftar fyrir afurðir A og B í síuninni. Það getur verið mjög flókið að ganga úr skugga um að allar afurðir séu hluti af síunni og þar af leiðandi er mælt með að forðast keyrslur á síaðri aðaláætlanagerð þegar framleiðslupantanir eru hafðar með.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]