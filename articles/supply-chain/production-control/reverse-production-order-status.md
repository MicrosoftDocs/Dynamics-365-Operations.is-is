---
title: "Bakfæra stöðu framleiðslupöntunar"
description: "Þetta efnisatriði lýsir því skal bakfæra stöðu framleiðslupöntunar."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4761e44b6bbc93ebf4a395948f42c2a73013ecb9
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="reverse-the-production-order-status"></a>Bakfæra stöðu framleiðslupöntunar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því skal bakfæra stöðu framleiðslupöntunar. 

Ef stöðu framleiðslupöntunar er bakfærð er pöntunin sjálf og allar aðgerðir tengdar leiðunum bakfærðar aftur á fyrra skref í framleiðslulíftímanum. Til dæmis hefur framleiðslupöntunin stöðuna **Áætlað**, og hægt er að breyta stöðu aftur í **Stofnað**. Í þessu tilfelli þarf kerfið fyrst að breyta stöðunni í **Metið**, sem er staða kemur strax á undan væntanlegri **Áætlað**. Það getur þá breytt stöðunni í þá stöðu sem óskað er eftir **Stofnað**. **Athugasemd** Ef pöntunin hefur náð stöðunni **tilkynna sem lokið** er enn hægt að bakfæra hana aftur á fyrra stig. Hins vegar þarf aftur að keyra matið og aðgerðaröðun, vinnsluröðun eða báðar gerðir röðunar til að uppfæra upplýsingarnar um pöntunina. Þetta skref er nauðsynlegt, Ástæðan er sú að hvers kyns frátekningar á eftirstöðvum vörunotkunar og tilfanganotkun aðgerðar þarf að endurstilla. Afgangurinn af þessari grein útskýrir hvað gerist þegar þú bakfærir stöðu framleiðslupöntunaar á eftirfarandi hátt:

-   Frá **metnu** til **stofnað**
-   Frá **Áætlað** í **Áætlað**
-   Frá **Losað** í **Áætlað**
-   Frá **Hafið** í **Losað**

## <a name="from-estimated-to-created"></a>Frá metnu til stofnað
Þegar stöðu framleiðslupöntunar er bakfært úr **Metið** til **Stofnað**, er vörunotkunin sem reiknuð var út fyrir vörur í uppskrift (BOM) fjarlægð. Birgðafærslur á framleiðslulínunni er eytt og **staða Eftirstöðva** reitur í uppskriftarlínur framleiðslupöntunar er endurstillt á **Lokið**. Þegar **Afleidd innkaup** og **Afleidd framleiðsla** valkostir eru valdir, eru allar undirliggjandi innkaupapantanir eða framleiðslupantanir eytt. Ef kostnaður fyrir framleiðslupöntun er metin, eða ef vörur voru handvirkt fráteknar svo að hægt væri að nota þær í framleiðslu, eru þessar færslur fjarlægðar.

## <a name="from-scheduled-to-estimated"></a>Frá Áætlað í metið
Þegar stöðunni framleiðslupöntunar er bakfæð úr **áætlað** í **metið**, er áætlaðar upphafs- og lokadagsetningar fjarlægðar. Frátekin afkastageta sem gerð var við röðun eru fjarlægðar og vinnslum sem stofnaðar voru við vinnsluröðun er eytt. Allar upplýsingar sem er skráð um aðgerðaröðun og vinnsluröðun á í **upplýsingar um Framleiðslupöntun** síðu er endurstillt.

## <a name="from-released-to-scheduled"></a>Frá Losað í Áætlað
Þegar staða framleiðslupöntunar er bakfært úr **losað** í **áætlað**, er eina breyting sem gerist er gildið í stöðusvæðinu.

## <a name="from-started-to-released"></a>Frá Hafið í Losað
Þegar stöðu framleiðslupöntunar er bakfært úr **hafið** í **losað**, eru allar vörur sem tilkynntar eru tilbúnar færðar aftur. Ef efni hefur verið sótt eða afhendingar á inn- og útleið hafa verið gerðar til framleiðslu, er þessum stillingum einnig snúið við. **staða Eftirstöðva** í uppskriftarlínum framleiðslupöntunarinnar er breytt úr **Lokið** til **efnisnotkun**. Ef tími hefur verið skráður, eða ef magn hefur verið tilkynnt sem lokið fyrir aðgerðirnar í framleiðsluleið, eru þessar stillingar færðar til baka. **Staða Eftirstöðva** í uppskriftarlínum framleiðslupöntunarinnar er breytt úr **Lokið** í **leiðarnotkun** í framleiðsluleið. Stillingar fyrir allar vörur sem eru bókaðar sem í vinnslu eða verk í vinnslu eru bakfærðar. Á **upplýsingar um Framleiðslupöntun** síðuna svæða sem sýna magnið sem var ræst eða skráð sem lokið eru endurstillt. Dagsetningar fyrir þær færslur sem eru einnig endurstillar.




