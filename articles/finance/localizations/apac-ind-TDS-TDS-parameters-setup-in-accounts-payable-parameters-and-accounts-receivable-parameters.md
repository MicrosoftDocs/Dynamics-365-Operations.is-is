---
title: Stilla TDS-færibreytur í viðskiptaskuldum og viðskiptakröfum
description: Þessi grein útskýrir hvernig á að stilla færibreytur í Viðskiptaskuldir og Viðskiptakröfur til að styðja frádrátt frá skatti sem dreginn er frá við uppruna (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e547b92f9f7e0ccc5b92df4cd991ce402369b568
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883151"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Stilla TDS-færibreytur í viðskiptaskuldum og viðskiptakröfum

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að stilla færibreytur í Viðskiptaskuldir og Viðskiptakröfur til að styðja frádrátt frá skatti sem dreginn er frá við uppruna (TDS).

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
