---
title: Smásöluverðskýrslur
description: Þessi grein veitir yfirlit yfir verðskýrslueiginleikann sem hægt er að nota til að skoða væntanlegar verðbreytingar fyrir hinar ýmsu vörur.
author: ShalabhjainMSFT
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 09350d15660978126d36199a3b4e93f6be5fe157
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269028"
---
# <a name="retail-price-reports"></a>Smásöluverðskýrslur

[!include [banner](includes/banner.md)]


Til þess að geta veitt viðskiptavinum sínum samkeppnishæf verð breyta söluaðliar oft verðum á afurðum. Verslunarstjórar vilja nálgast á auðveldan hátt nýlegar eða væntanlegar verðbreytingar svo þeir geti gert áætlun um nauðsynleg tilföng til að uppfæra verðmerkingar sem sjást í hillum verslunar. Með útgáfu 10.0 af Retail getur verslunarstjóri opnað skýrsluna **Verð** með því að fletta upp á **Allar verslanir \> Verslun \> Verðskýrsla** og skoða uppfærð verð fyrir afurðirnar sem tengjast versluninni. 

Til að virkja verðskýrsluna verður að kveikja á færibreytunni **Virkja verðskýrslu fyrir verslun**. Þessi færibreyta er staðsett í flipanum **Færibreytur Commerce \> Afslættir \> Ýmislegt**. Þegar síðan **Verðskýrsla** er opnuð birtist svargluggi með ýmsum skilgreiningum. Tiltækar skilgreiningar eru sýndar hér að neðan.

| Grunnstilling | lýsing |
|---|---|
| Frá dagsetningu / Til dagsetningar| Dagsetningabilið sem verðskýrslan ætti að vera búin til fyrir. Tímalengdin er sem stendur takmörkuð við 7 daga. |
| Rás| Verslunin sem verðskýrslan ætti að vera búin til fyrir. |
| Sýna afurðir með tiltækar birgðir| Ef þetta er stillt á **Já** verða verðin sýnd fyrir aðeins þessar afurðir sem eru með tiltækar efnislegar birgðir sem stendur í versluninni. |
| Sýna verð á afbrigðum | Ef þetta er stillt á **Já** verða verðin sýnd fyrir afbrigðin ásamt afurðarsniðmátunum. Aðeins ætti að stilla þetta á **Kveikja** ef þú ert með verð sem miðast við afbrigði, vegna þess að fjöldi lína eykst umtalsvert. Í framtíðarútgáfum munum við virkja víddarmiðuð verð svo verslunarstjórinn geti valið víddirnar þar sem sýna á verðin. |
| Sýna afurðir með verðbreytingum | Ef þetta er stillt á **Já** verða verðin sýnd fyrir aðeins þessar dagsetningar sem verðinu hefur verið breytt. Verðið fyrir *Einum degi á undan* valdri **Frá dagsetningu** verður alltaf sýnt svo verslunarstjórinn geti auðveldlega borið kennsl á afurðirnar sem hafa ekki breyst í verði yfir allt tímabilið sem var valið, og svo hann geti einnig skoðað núgildandi verð. |

Eftir að skýrslan er búin til er hægt að hlaða niður Excel-skránni fyrir allar nauðsynlegar viðbótarsíur. Einnig er hægt að nota verðskýrsluna til að athuga eldri verð á afurðum fyrir fyrri dagsetningar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
