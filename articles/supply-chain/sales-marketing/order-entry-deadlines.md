---
title: Tímamörk skráningar pantana
description: Þessi grein gefur upplýsingar um lokadag fyrir skráningu pantana. Lokadagur fyrir skráningu pantana er sá lokatími sem sker úr um það hvort pöntun viðskiptavinar er meðhöndluð (og uppfyllt) eins og hún sé móttekin á núverandi degi eða daginn eftir.
author: omulvad
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable, MCRAutoTaxRules
audience: Application User
ms.reviewer: kamaybac
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf2780edc75891d565a184135d6a915a0e6f8504
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839078"
---
# <a name="order-entry-deadlines"></a>Tímamörk skráningar pantana

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um lokadag fyrir skráningu pantana. Lokadagur fyrir skráningu pantana er sá lokatími sem sker úr um það hvort pöntun viðskiptavinar er meðhöndluð (og uppfyllt) eins og hún sé móttekin á núverandi degi eða daginn eftir.

Í mörgum fyrirtækjum verður sölupöntun að hafa borist fyrir ákveðinn tíma dags til þess að hún sé unninn eins og hún hafi borist þann dag. Allar pantanir sem er tekið eftir þann dag eru meðhöndlaðar eins og ef þær eru mótteknar í næsta virka dag. Þessi loktími fyrir pantanir kallast lokadagur fyrir skráningu pantana.  

Lokadagur fyrir skráningu pantana eru notaðar sem inntak fyrir pöntun lofað. Því eru þær aðstoðað við að stjórna væntingar viðskiptamanna um afhendingu. Til dæmis, viðskiptavini sjá að, ef þeir leggja inn pöntun hjá þér áður en á tilteknum tíma, muntu lofa að senda vörum á sama degi. Hins vegar ef þeir missa af þessum lokafresti geta þeir aðeins búist við sendingu næsta virka dag. Þú stillir lokadagur fyrir skráningu pantana samkvæmt getu vöruhúss og áætlunir farmflytjanda.  

Á **lokadagur fyrir skráningu pantana** síðu er að setja tíma fyrir lokadagur fyrir skráningu pantana fyrir alla daga vikunnar. Allar pantanir sem er tekið eftir þann dag eru meðhöndlaðar eins og ef þær eru mótteknar í næsta dag. Að sjálfgefnu þessir tímar eru stillt á 23:59 (það er eina mínútu fyrir miðnætti við lok viðkomandi dags). Hægt er að breyta sjálfgefnum tímum svo að þeir passi við raunverulega tímamarka sendingar eða innhreyfingar.  

Hægt er að skilgreina lokadagur fyrir skráningu pantana fyrir tiltekinn hóp viðskiptavina. Til dæmis gæti ætlunin verið að tiltekinn flokk af viðskiptavinum hafi lokadagur fyrir skráningu pantana sem er síðar en þær annarra viðskiptavina. Í þessu tilfelli er fyrst að skilgreina flokka lokadagur fyrir skráningu pantana á **flokkar fyrir lokadagur fyrir skráningu pantana** síðunni. Síðan skal tengja flokka við viðskiptavina á síðunni **Viðskiptavinir**.  

Ef fyrirtækið samanstendur af nokkrum staðsetningum, er hægt að setja upp lokadagur fyrir skráningu pantana fyrir hverja staðsetningu. Ef staðsetningarnar eru staðsett í mismunandi tímabeltum er lokadagur fyrir skráningu pantana settur upp í tímabelti staðsetningarinnar. Þegar verið er hins vegar að vinna með sölupantanir og sölutilboð er lokadagur fyrir skráningu pantana breytt í tímabeltið þitt í  síðunni **tiltækar sendingar og innhreyfingardagsetningar**.  

Á **Virkja samsetningar lokadags fyrir skráningu pantana** síðu er að skilgreina þær samsetningar svæða og flokka lokadaga fyrir skráningu pantana sem eru leyfð.

## <a name="example-order-entry-deadline"></a>Dæmi: Pöntunarfærsluskiladagur
Lokadagur fyrir skráning pantana á þriðjudögum hefur verið stilltur á 16:00. Á ákveðnum þriðjudegi, klukkan 17:00, reynirðu að stilla núverandi dagsetningu sem sendingardagsetningu. (Athugið að enginn afhendingartími er fyrir þetta dæmþ) Ef í **Stýring afhendingardagsetningar** gátreiturinn er valinn, færðu viðvörun sem tilgreinir að dagsetning er ekki gild. Viðvörunin birtist á á **Tiltækar sendingar- og móttökudagsetningar** síðuna þar sem er hægt að velja aðrar dagsetningar.

## <a name="example-different-order-entry-deadlines-per-site"></a>Dæmi: Mismunandi lokadagar fyrir skráningu pantana fyrir hvert vefsvæði
Fyrirtækið samanstendur af tveimur setrum. Staðsetningarnar eru staðsett í mismunandi tímabeltum, eins og sýnt er í eftirfarandi töflu.

| A-setur                      | B-setur                      |
|-----------------------------|-----------------------------|
| Kalifornía                  | Flórída                     |
| PST (staðaltími vesturhluta BNA og Kanada) | EST (staðaltími austurhluta BNA og Kanada) |

Staðsetningar A og B hafa skilgreint eftirfarandi lokadagur fyrir skráningu pantana.

| Vikudagur             | A: Lokadagar fyrir skráningu pantana (PST) | B: Lokadagur fyrir skráningu pantana (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Mánudagur                      | 13:00:00                          | 14:00:00                          |
| Þriðjudagur                     | 13:00:00                          | 14:00:00                          |
| Miðvikudagur                   | 13:00:00                          | 14:00:00                          |
| Fimmtudagur                    | 13:00:00                          | 14:00:00                          |
| Föstudagur                      | 13:00:00                          | 14:00:00                          |

Þú ert afgreiðslumaður pantana og staðsettur í Utah í tímabeltinu MST (staðaltími í Klettafjöllum). Þetta þýðir að svo fremi pöntun sé gerð á vefsvæði A fyrir 14:00 MST og á vefsvæði B fyrir 12:00 MST er lokadagur fyrir skráningu pantana mætt fyrir bæði vefsvæði.  

Eftirfarandi tafla sýnir lokadag fyrir skráningu pantana fyrir A og B-setur umbreytt í MST-tíma.

| A-setur: PST         | A-setur: MST        | B-setur: EST           | B-setur: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00:00               | 14:00:00              | 14:00:00                 | 12:00:00              |

**Athugasemd** Ef leiðrétting fyrir birtusparnaðartíma er virk, eru lokadagur fyrir skráningu pantana leiðréttir eftir því.

## <a name="example-same-order-entry-deadline-per-site"></a>Dæmi: Sama pöntunarfærsluskiladagar fyrir hvert vefsvæði
Fyrirtækið samanstendur af tveimur setrum. Staðsetningarnar eru staðsett í mismunandi tímabeltum, eins og sýnt er í eftirfarandi töflu.

| A-setur                      | B-setur                      |
|-----------------------------|-----------------------------|
| Kalifornía                  | Flórída                     |
| PST (staðaltími vesturhluta BNA og Kanada) | EST (staðaltími austurhluta BNA og Kanada) |

Staðsetningar A og B hafa skilgreint eftirfarandi lokadagur fyrir skráningu pantana.

| Vikudagur | PST og EST |
|-----------------|-------------|
| mánudagur          | 13:00:00       |
| þriðjudagur         | 13:00:00       |
| miðvikudagur       | 13:00:00       |
| fimmtudagur        | 13:00:00       |
| föstudagur          | 13:00:00       |

Þú ert afgreiðslumaður pantana og ert staðsettur í Utah í tímabeltinu MST. Þetta þýðir að svo fremi pöntun sé gerð á vefsvæði A fyrir 14:00 MST og á vefsvæði B fyrir 11:00 MST er lokadagur fyrir skráningu pantana mætt fyrir bæði vefsvæði. 

Eftirfarandi tafla sýnir lokadag fyrir skráningu pantana fyrir A og B-setur umbreytt í MST-tíma.

| A-setur: PST         | A-setur: MST        | B-setur: EST           | B-setur: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00:00               | 14:00:00              | 13:00:00                 | 11:00:00              |

**Athugasemd** Ef leiðrétting fyrir birtusparnaðartíma er virk, eru lokadagur fyrir skráningu pantana leiðréttir eftir því.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Afhendingaráætlanir](delivery-schedules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]