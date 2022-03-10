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
ms.openlocfilehash: 2205ddc1b651ff851a4285b1ded17106600e6058c719fecf0b447ac8c87d43cb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755617"
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
4. Veldu **Í lagi**.

    [![Svargluggi fyrir uppfærslu pöntunarlína.](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Opnið **Skattur \> Uppsetning \> Færibreytur \> Færibreytur viðskiptaskulda**.
6. Á flipanum **Almennt** á flýtiflipanum **Skipting á grundvelli afhendingarupplýsinga** skal stilla valkostinn **Innhreyfingarskjal** á **Já** til að birta og skipta innhreyfingarskjali með mismunandi heimilisföngum og skattreikningsnúmerum (TAN). Ef þessi valkostur er stilltur á **Nei** er ekki hægt að bóka fylgiseðil með öðru heimilisfangi og skattareikningsnúmerum.
7. Stillið valkostinn **Reikningur** á **Já** til að bóka og skipta innkaupareikningi með öðru heimilsföngum og skattareikningsnúmerum.

    [![Flýtiflipi fyrir skiptingu á grundvelli afhendingarupplýsinga.](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Lokið síðunni.
