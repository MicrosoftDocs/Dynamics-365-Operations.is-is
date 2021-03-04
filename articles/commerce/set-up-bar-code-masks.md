---
title: Setja upp sniðmát fyrir strikamerki
description: Þetta efnisatriði lýsir því hvernig á að setja upp stafi sniðmáts strikamerkja, sniðmát fyrir strikamerki og hvernig á að úthluta sniðmátum strikamerkja á strikamerki.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 89b63843daaa714d9141fc362c3d6fcb6ca9a91e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413257"
---
# <a name="set-up-bar-code-masks"></a>Setja upp sniðmát fyrir strikamerki

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp stafi sniðmáts strikamerkja, sniðmát fyrir strikamerki og hvernig á að úthluta sniðmátum strikamerkja á strikamerki.

## <a name="set-up-bar-code-mask-characters"></a>Setja upp stafi fyrir sniðmát strikamerkja

Sniðmát strikamerkja eru notuð til að búa til strikamerki og til að auðkenna fljótt þau strikamerki sem er skönnuð í sölustað (POS). Sniðmát eru samsett úr stöfum sem vinna sem frátakarar sem tilgreina snið fyrir strikamerki sem verða stofnuð. Til að stilla sniðmát strikamerkja, þarf að setja upp stafi fyrir sniðmát strikamerkja. Fara í **Retail og Commerce** &gt; **Birgðastjórnun** &gt; **Strikamerki og merkingar** &gt; **Stafir sniðmáts**. Smellt er á **Nýtt** til að stofna nýja stafi sniðmáts strikamerkja. Hægt er að stofna stafi fyrir sniðmát strikamerkja til að tilgreina eftirfarandi strikamerkjagögn.

| Svæði            | lýsing |
|------------------|-------------|
| Afurð          | Frátakari fyrir afurðakenni. |
| Hvaða númer sem er       | Notað til að tilgreina númer sem eru bundnar kóðaðir í strikamerki. |
| Vartala      | Tilgreinir að snið strikamerkis í strikamerkja notar vartölu til að staðfesta gildi strikamerkis. |
| Stærðartala       | Tilgreinir stærð í strikamerki sem er stofnað fyrir afurðarafbrigði sem felur í sér stærð. |
| Litatala      | Tilgreinir lit í strikamerki sem er stofnað fyrir afurðarafbrigði sem felur í sér lit. |
| Stíltala      | Tilgreinir stíl í strikamerki sem er stofnað fyrir afurðarafbrigði sem felur í sér stíl. |
| EAN-leyfiskóði | Frátakari á EAN leyfi gefin út vegna EAN-leyfiskóða. |
| Verð            | Gefur til kynna verð fyrir verð ívafinn strikamerki. |
| Magn         | Tilgreinir strikamerki með magn í magn/handahófskenndri þyngd ívaf. |
| Starfsmaður         | Tilgreinir hluta strikamerkis fyrir númer starfsmanns sem er notað fyrir strikamerkisinnskráningu í POS. |
| Viðskiptavinur         | Sýnir hluta af kenni viðskiptavinar. |
| Gagnafærsla       | *Enn ekki framkvæmt.* |
| Afsláttarkóði    | *Úrelt* frá og með Dynamics 365 for Retail vorútgáfa 2017. Áður: Tilgreinir afsláttarkóða fyrir strikamerki sem er notað til að bæta við afslætti í sölufærslu. |
| Afsláttarmiðakóði      | Tilgreinir kóða útgefandi strikamerki notað til að bæta afslátt pöntunina. Þetta skipt kóða staðgreiðsluafsláttar. |
| Gjafakort        | Tilgreinir númer gjafakorts við útgáfu á eða borgun með gjafakorti. |
| Vildarkort     | Bætir vildarviðskiptavini við færsluna og er hægt að nota þegar borgað er með vildarkerfi. |

## <a name="define-bar-code-masks"></a>Skilgreina sniðmát fyrir strikamerki

Eftir að stafir fyrir sniðmát strikamerkja eru tilgreindir fyrir nauðsynleg sniðmát strikamerkja skal fara á **Retail og Commerce** &gt; **Birgðastjórnun** &gt; **Strikamerki og merkingar** &gt; **Uppsetning sniðmáts fyrir strikamerki**. Á þessari síðu er hægt að skilgreina sniðmát strikamerkja sem nota áður tilgreinda stafi. Þessi strikamerki verða notuð við myndun á strikamerkjum og einnig til að auðkenna strikamerki sem eru skökkuð í POS.

1. Smellt er á **Ný** til að búa til nýtt sniðmát strikamerkis.
2. Færið inn gildi í svæðin **Sniðmátskenni** og **Lýsing** og veljið síðan gerð sniðmáts strikamerkja í svæðinu **Gerð**.
3. Í kaflanum **Almennt** skal velja gildi í svæðinu **Strikamerkjastaðall** og tilgreina síðan forskeyti strikamerkis, ef þarf.
4. Í kaflanum **Hluti sniðmáts fyrir strikamerki** skal bæta við strikamerki hlutar sem verður notaður í strikamerki sem á að stofna.

Til dæmis, til að stofna sniðmát fyrir strikamerki með Sniðmátskenni 'Afurð' skal gera eftirfarandi:

1. Stofna nýtt sniðmát strikamerkis og velja gerðina „Afurð“.
2. Veldu strikamerkjastaðal, til dæmis, 'kóði 39'.
3. Veita forskeyti sem nota á til að auðkenna afstemmingarfærslur strikamerkis. Til dæmis „22“.
4. Bæta við hluta sniðmáts. Sniðmátshlutinn „Afurð“ verður valinn.
5. Veita lengd fyrir afurðarhlutann, til dæmis „10“. Lengd ætti að samsvara lengd Afurðakennis sem er yfirleitt notað í verslun. Sniðmátskenni verður birt í forskoðun í kaflanum **Almennt** undir **Sniðmáti**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Úthluta sniðmáti fyrir strikamerki á strikamerki

Sniðmátum fyrir strikamerki verður að úthluta á strikamerki áður en hægt er að nota þau. Svo haldið sé áfram með fyrra dæmi strikamerkisins, til að úthluta strikamerki, skaltu gera eftirfarandi:

1. Fara á **Fyrirtækisstjórnun** &gt; **Uppsetning** &gt; **Strikamerki**. Smellt er á **Ný** til að búa til nýtt strikamerki.
2. Færið inn gildi í reitina **Strikamerki** **uppsetning** og **Uppsetning**.
3. Í kaflanum **Almennt**, í svæðinu **Gerð strikamerkis** skal velja „Kóða 39“. Í svæðinu **Sniðmát** **Auðkenni** skal velja sniðmátið „Afurð“ sem var stofnað áður.
4. Undir **Stærð** skal færa inn „12“.
5. Smellið á **Vista**.

Nú er hægt að nota sniðmát fyrir strikamerki til að búa til strikamerki fyrir vörur. Skrefin að ofan eru dæmi um hvernig stofna á sniðmát fyrir strikamerki fyrir vörur, en þau sýna einnig hvernig stofna á sniðmát fyrir strikamerki fyrir allar aðrar gerðir studdra strikamerkja. Leiðrétta ætti stafi strikamerkja, gerðir og hámarkslengd fyrir notkun í tilteknum umhverfinu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]