---
title: Afskriftarreglur eigna
description: Þetta efnisatriði gefur yfirlit yfir afskriftarreglur á eignum.
author: saraschi2
manager: AnnBe
ms.date: 03/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6880a4b97af0a819684dac7e0132ae10a8997533
ms.sourcegitcommit: 60aa392e7762d9b62baf007be27dec043bd078df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/21/2019
ms.locfileid: "884600"
---
# <a name="fixed-asset-depreciation-conventions"></a>Afskriftarreglur eigna

[!include [banner](../includes/banner.md)]

Afskriftarreglur eru notaðar til að ákvarða hvenær og hvernig afskrift er reiknuð bæði fyrir árið þegar eignin er keypt og árið þegar eignin er losuð.

Hægt er að úthluta afskriftarreglum á uppsetningu eignaflokkabókar. Til að skoða eða úthluta afskriftarreglum skal velja flokkinn **Egnir** í uppsetningarsvæði eigna. Veljið hnappinn **Bækur**. Í því tilfelli eru úthlutaðar afskriftarreglur notaðar sem sjálfgefin gildi þegar eignabækur eru stofnaðar. Einnig er hægt að setja afskriftarreglurnar á einstaka eignabók. Til að gera þetta skal velja **Bækur** í uppsetningarsvæði eigna og síðan velja hnappinn **Eignaflokkar**.


|  Afskriftarregla  |   Lýsing  |
|---------------------------|-----------------|
|           Enginn            |  Eignir byrja að rýrna á dagsetningunni <strong>Tekin í notkun</strong>.|
|         Hálft ár         |  Draga skal frá hálfsárs rýrnun fyrir bæði fyrsta árið og síðasta árið sem eignin er rýrð. Draga skal frá heilsárs rýrnun fyrir öll hin árin á afskriftartímabilinu. |
|        Heill mánuður         | Eignir sem hafa dagsetninguna <strong>Tekin í notkun</strong> hvenær sem er í mánuðinum byrja að rýrna á fyrsta degi þess mánaðar. Eignir sem eru teknar úr umferð hvenær sem er í mánuðinum eru álitnar lausar undan rýrnun á síðasta degi fyrri mánaðar.  |
|        Miður fjórðungur        | Til að reikna afskriftir fyrir árið þegar eignin var tekin í notkun skal margfalda afskriftina fyrir heilt ár með prósentu þess ársfjórðungs þegar eignin er tekin í notkun eins og sýnt er í eftirfarandi töflu.<table><thead><tr><th>Ársfjórðungur</th><th>Prósenta</th></tr></thead><tbody><tr><td>Fyrst</td><td>87,5</td></tr><tr><td>Annað</td><td>62,5</td></tr><tr><td>Þriðja</td><td>37,5</td></tr><tr><td>Fjórða</td><td>12,5</td></tr></tbody></table>Hálfsfjórðungs afskriftir eru teknar á ársfjórðungi losunar (eða ársfjórðungnum með fullum afskriftum). |
| Miður mánuður (fyrsti mánaðar)  | Eignir sem hafa dagsetninguna <strong>Tekin í notkun</strong> á fyrri hluta mánaðar (dögum 1 til 15) byrja að rýrna á fyrsta degi mánaðarins fyrir dagsetninguna <strong>Tekin í notkun</strong>. Eignir sem hafa dagsetninguna <strong>Tekin í notkun</strong> á seinni hluta mánaðar (dögum 16 til mánaðarloka) byrja að rýrna á fyrsta degi mánaðarins eftir dagsetninguna <strong>Tekin í notkun</strong>. Eignir sem eru teknar úr umferð á fyrri hluta mánaðar (dögum 1 til 15) teljast lausar undan rýrnun á síðasta degi fyrri mánaðar. Eignir sem eru teknar úr umferð á seinni hluta mánaðar (dögum 16 til mánaðarloka) teljast lausar undan rýrnun á síðasta degi þess mánaðar sem eignin var tekin úr umferð. |
| Miður mánuður (15. mánaðar) |  Til að reikna út afskriftir fyrir árið sem eignin var tekin í notkun skal margfalda afskriftirnar fyrir heilt ár með broti. Teljari (efri talan) brotsins er fjöldi heilra mánaða á árinu sem eignin er í notkun, auk 1/2 eða (0,5). Nefnarinn (neðri talan) er 12. Ef eignin er losuð fyrir lok afskriftartímabilsins skal nota sömu aðferðina til að reikna út afskriftir fyrir ráðstöfunarárið.   |
| Hálft ár (byrjun árs) | Eignir sem hafa dagasetninguna <strong>Tekin í notkun</strong> á fyrri helmingi ársins byrja að rýrna á fyrsta degi ársins (allt árið). Eignir sem hafa dagsetninguna <strong>Tekin í notkun</strong> á seinni hluta ársins byrja að rýrna á miðju ári.|
|   Hálft ár (næsta ár)   |   Eignir sem hafa dagasetninguna <strong>Tekin í notkun</strong> á fyrri helmingi ársins byrja að rýrna á fyrsta degi ársins (allt árið). Eignir sem hafa dagsetninguna <strong>Tekin í notkun</strong> á seinni hluta árs byrja að rýrna á fyrsta degi næsta árs. Eignir sem eru teknar úr umferð á fyrri hluta árs teljast á lausar undan rýrnun á síðasta degi fyrra árs. Allar afskriftir sem eru bókaðar á yfirstandandi ári verða að vera bakfærðar eða leiðréttar. Eignir sem eru teknar úr umferð á seinni hluta árs teljast lausar undan rýrnun á síðasta degi þess árs sem eignin er tekin úr umferð.|

