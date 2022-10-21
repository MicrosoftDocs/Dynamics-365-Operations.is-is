---
title: Endurskoðun samstillingu á rekstri viðskiptavina í höfuðstöðvum
description: Þessi grein útskýrir hvernig á að endurskoða samstillingu á aðgerðum viðskiptavina í Microsoft Dynamics 365 Commerce höfuðstöðvar til að hjálpa til við að laga hvers kyns vandamál notenda.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690965"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Endurskoðun samstillingu á rekstri viðskiptavina í höfuðstöðvum

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein útskýrir hvernig á að endurskoða samstillingu á aðgerðum viðskiptavina í Microsoft Dynamics 365 Commerce höfuðstöðvar til að hjálpa til við að laga hvers kyns vandamál notenda.

Þegar stofnanir byrja að tileinka sér hæfileikann til að búa til og breyta viðskiptavinum ósamstillt, þurfa síðustjórnendur leið til að skoða og leysa aðgerðir, byggt á beiðnum notenda síðunnar eða vinnslubilunum. Í þeim tilfellum ættu síðustjórar að geta endurskoðað stofnun viðskiptavina og breytt aðgerðum og lagað allar bilanir með því að nota sjálfsafgreiðslulíkan.

## <a name="customer-synchronization-status"></a>Samstillingarstaða viðskiptavinar

Þegar þú velur ósamstillta stillingu viðskiptavinastjórnunar og samsvarandi eiginleika hennar, verða stjórnendur Commerce höfuðstöðva að búa til og skipuleggja endurtekið lotuverk fyrir **P-starf**, hinn **Samstilltu viðskiptavini og viðskiptafélaga úr ósamstilltu stillingu** starf, og **1010** starf, þannig að ósamstilltum viðskiptavinum er breytt í samstillingarviðskiptavini í höfuðstöðvum Commerce. Samstilling viðskiptavinastjórnunaraðgerða á sér stað þegar þessi störf eru keyrð. Fyrir frekari upplýsingar, sjá [Ósamstilltur viðskiptahamur til að búa til](async-customer-mode.md).

Sem eigandi fyrirtækis geturðu framkvæmt eftirfarandi aðgerðir:

- Skoðaðu allar aðgerðir til að búa til/breyta síðunotendum. Upplýsingar innihalda stöðu og tímastimpil.
- Sía aðgerðir með því að nota einhvern af reitum og gildum viðskiptavinatöflu til að þrengja endurskoðunarskrána.
- Skoðaðu stuttar lýsingar á breytingum ásamt stöðuupplýsingum til að skilja aðgerðir á háu stigi.
- Fyrir bilanir, breyttu og lagfærðu erfiða reiti og síðan vistaðu og samstilltu sérstakar aðgerðir viðskiptavina.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Hlutir á stöðusíðu samstillingar viðskiptavinar

Til að skoða lista yfir allar samstillingaraðgerðir skaltu fara í höfuðstöðvar Commerce á **Verslun og verslun \> Viðskiptavinir \> Samstillingarstaða viðskiptavina**. Eftirfarandi mynd sýnir dæmi um **Samstillingarstaða viðskiptavina** síðu.

![Stöðusíða fyrir samstillingu viðskiptavina í höfuðstöðvum Commerce.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Sjálfgefið er listi yfir samstillingaraðgerðir viðskiptavina vinstra megin á **Samstillingarstaða viðskiptavina** síða inniheldur eftirfarandi dálka:

- Heiti rásar
- Viðskiptavinalykill
- Ósamstilltur viðskiptavinalykill
- Tímastimpill rekstrar
- Samstillingarstaða viðskiptavina

Efst til hægri á síðunni eru upplýsingar um viðskiptavinareikning, svo sem **Viðskiptavinareikningur**, **rekstur smásölu**, **viðskiptavina**, og **Síðasta þekkta villa** gildi.

The **Breyta lýsingu** kafla inniheldur lýsingu á tegund viðskiptavinastjórnunaraðgerðar sem var í gangi (til dæmis stofnun viðskiptavina, uppfærslu reiknings eða samstillingarbilun með smáatriðum).

The **Eiginleikar viðskiptavina** kafla inniheldur rist sem sýnir alla eiginleika viðskiptavina ásamt gömlum og nýjum gildum. Þú getur breytt þessum hluta ef þú vilt breyta eiginleikum viðskiptavina til að laga villur og samstilla síðan aftur.
