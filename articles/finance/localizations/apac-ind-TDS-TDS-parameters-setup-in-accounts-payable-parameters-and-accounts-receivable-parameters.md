---
title: Stilla TDS-færibreytur í viðskiptaskuldum og viðskiptakröfum
description: Í þessu efnisatriði er útskýrt hvernig á að setja breytur í viðskiptaskuldir og viðskiptakröfur til að styðja við skatt sem dreginn er frá í uppruna (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023328"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Stilla TDS-færibreytur í viðskiptaskuldum og viðskiptakröfum

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja breytur í viðskiptaskuldir og viðskiptakröfur til að styðja við skatt sem dreginn er frá í uppruna (TDS).

1. Opnið **Skattur \> Uppsetning \> Færibreytur \> Færibreytur viðskiptakrafna**.
2. Á flipanum **Uppfærslur** skal velja **Uppfæra pöntunarlínur** til að opna gluggann **Uppfæra pöntunarlínur**.
3. Í hlutanum **TDS-hópur**, í reitnum **Uppfærsla TDS-hóps**, skal tilgreina aðferðina sem nota skal við uppfærslu TDS-hópsins á línustigi. Stillingin er notuð þegar TDS-hópurinn er uppfærður í pöntunarhaus. Eftirtaldir valkostir eru í boði:

    - **Aldrei** – TDS-hópurinn er ekki uppfærður í pöntunarlínunum þegar hann er uppfærður í pöntunarhausnum.
    - **Alltaf** – TDS-hópurinn uppfærist sjálfkrafa á pöntunarlínunum þegar hann uppfærist í pöntunarhausnum.
    - **Spurning** – Notendur fá skilaboð þar sem þeir eru beðnir um að uppfæra TDS hópinn á pöntunarlínunum.
4. Veljið **Í lagi**.

    [![Svargluggi fyrir uppfærslu afurða](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Opnið **Skattur \> Uppsetning \> Færibreytur \> Færibreytur viðskiptaskulda**.
6. Á flipanum **Almennt** á flýtiflipanum **Skipting á grundvelli afhendingarupplýsinga** skal stilla valkostinn **Innhreyfingarskjal** á **Já** til að birta og skipta innhreyfingarskjali með mismunandi heimilisföngum og skattreikningsnúmerum (TAN). Ef þessi valkostur er stilltur á **Nei** er ekki hægt að bóka fylgiseðil með öðru heimilisfangi og skattareikningsnúmerum.
7. Stillið valkostinn **Reikningur** á **Já** til að bóka og skipta innkaupareikningi með öðru heimilsföngum og skattareikningsnúmerum.

    [![Skipting á grundvelli afhendingarupplýsinga](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Lokið síðunni.
