---
title: "Setja upp sniðmát fyrir strikamerki"
description: "Þetta efnisatriði lýsir því hvernig á að setja upp stafi sniðmáts strikamerkja, strikamerki, og hvernig á að úthluta strikamerkjum sniðmáts fyrir strikamerki til."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Setja upp sniðmát fyrir strikamerki

Þetta efnisatriði lýsir því hvernig á að setja upp stafi sniðmáts strikamerkja, strikamerki, og hvernig á að úthluta strikamerkjum sniðmáts fyrir strikamerki til.

<a name="set-up-bar-code-mask-characters"></a>Setja upp stafi fyrir sniðmát strikamerkja
-------------------------------

Strikamerki eru notuð til að búa til strikamerki og til að auðkenna fljótt strikamerkja sem er skönnuð í sölustað (POS). Sniðmát eru samsett stafi sem vinna sem frátakara sem á að tilgreina snið fyrir strikamerki sem verður stofnuð. Til að stilla sniðmát strikamerkja, þarf að setja upp stafi fyrir sniðmát strikamerkja. Fara í **Smásölu og commerce**&gt;**Birgðastjórnun**&gt;**Strikamerki og merkingar**&gt;**stafir Sniðmáts**. Smellið á **Nýtt** til að stofna stöfum sniðmáts strikamerkisins. Hægt er að stofna stafi fyrir sniðmát strikamerkja til að tilgreina eftirfarandi gögn strikamerki.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Frátakari fyrir afurðakenni.                                                                                     |
| **Any number**       | Notað til að tilgreina númer sem eru bundnar kóðaðir í strikamerki.                                                  |
| **Check digit**      | Tilgreinir snið strikamerkis í strikamerkja notar vartölu til að staðfesta gildi strikamerki. |
| **Size digit**       | Tilgreinir stærð í strikamerki stofnað fyrir afurðarafbrigði sem felur í sér stærð.                                 |
| **Color digit**      | Tilgreinir lit í strikamerki stofnað fyrir afurðarafbrigði sem felur í sér lit.                               |
| **Style digit**      | Tilgreinir stíl í strikamerki stofnað fyrir afurðarafbrigði sem felur í sér stíl.                             |
| **EAN license code** | Frátakari á EAN leyfi gefin út vegna EAN leyfiskóða.                                                       |
| **Verð**            | Gefur til kynna verð fyrir verð ívafinn strikamerki.                                                                   |
| **Quantity**         | Tilgreinir magn magn/handahófskenndri þyngd ívafinn strikamerkjum.                                                |
| **Employee**         | Tilgreinir hluti strikamerki fyrir númer starfsmanns nota fyrir innskráningu á Sölustað strikamerki.                                  |
| **Customer**         | Sýnir Kenni hluti viðskiptavinar.                                                                                  |
| **Innfærsla gagna**       | *Hefur enn ekki verið innleidd.*                                                                                          |
| **Discount code**    | Tilgreinir afsláttarkóða fyrir strikamerki sem er notuð til að bæta við afslætti punktur færslu sölu             |
| **Gjafakort**        | Tilgreinir númer gjafakorts þegar gaf eða borgun með gjafakort.                                               |
| **Loyalty card**     | Bætir við færsluna er vildarviðskiptavini og hægt er að nota þegar borgun með vildarkerfis.                             |

## <a name="define-bar-code-masks"></a>Tilgreina sniðmát fyrir strikamerki
Eftir að stafi fyrir sniðmát strikamerkja eru tilgreindar fyrir nauðsynlegar strikamerkja, fara **Smásölu og commerce**&gt;**Birgðastjórnun**&gt;**Strikamerki og merkingar**&gt;**uppsetning sniðmáts fyrir Strikamerki**. Á þessari síðu er hægt að skilgreina strikamerkja sem nota áður tilgreindum stafir. Þessar strikamerkja verður notað þegar skannaðar myndun strikamerki og verða einnig til að auðkenna strikamerki á Sölustaðnum.

1.  Smellt er á **Nýtt** til að stofna nýja strikamerkja.
2.  Færið inn gildi í á **Sniðmátskenni** og **Lýsing** svæði og veljið síðan gerð sniðmáts strikamerkja á **Gerð** svæði.
3.  Í í **Almennt** kaflanum skal velja gildi í í **strikamerkjastaðall** svæðinu og tilgreina síðan forskeyti strikamerki, ef þarf.
4.  Í því **hluti sniðmáts fyrir strikamerki** hlutanum, bæta strikamerki hlutar sem verður notaður í strikamerki til að stofna.

Sem dæmi, til að stofna sniðmát fyrir strikamerki með Sniðmátskenni 'Afurð' er væri að gera eftirfarandi:

1.  Stofna nýja strikamerkja og velja gerðinni 'Afurð'.
2.  Veljið staðlað strikamerki, til dæmis, "Kóða 39'.
3.  Veita forskeyti sem nota á til að auðkenna afstemmingarfærslur strikamerki. Til dæmis, "22'.
4.  Bæta hluti sniðmáts. Hluti sniðmáts 'Afurð' eru valin.
5.  Veita lengd fyrir hlutann afurð, til dæmis, "10'. Lengd ætti að samsvara lengd Afurðakenni sem er yfirleitt notað í verslun. Sniðmátskenni birt í forskoðun á **Almennt** hlutanum undir **Sniðmáts**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Strikamerki er úthlutað á strikamerki
Sniðmát fyrir strikamerki verður úthlutað á strikamerki áður en hægt er að nota þær. Haldið er áfram með fyrri dæmi strikamerkisins að úthluta strikamerki, gerið eftirfarandi:

1.  Fara í **fyrirtækisstjórnun**&gt;**Uppsetningu**&gt;**strikamerki**. Smellið á **Nýtt** til að stofna nýtt strikamerki.
2.  Færið inn gildi í á **Strikamerki****uppsetningu** og ** Uppsetningu ** svæði.
3.  Í á **Almennt**, í hlutanum við **gerð strikamerkis** skal velja 'Kóða 39'. Í því **Sniðmáts****Kenni** skal velja 'Afurð' sniðmáts áður stofnaðar.
4.  Undir **Stærð**, færa inn '12'.
5.  Click **Save**.

Nú er hægt að nota sniðmát fyrir strikamerki til að búa til strikamerki fyrir vörur. Skrefin að ofan eru dæmi um hvernig stofna á sniðmát fyrir strikamerki fyrir vörur, en þær sýna einnig hvernig stofna á sniðmát fyrir strikamerki fyrir allar aðrar gerðir studd strikamerki. Ætti að leiðrétta strikamerkja gerðir og hámarkslengd fyrir notkun í tilteknum umhverfinu.


