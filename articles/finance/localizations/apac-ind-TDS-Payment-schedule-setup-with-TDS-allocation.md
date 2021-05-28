---
title: Setja upp greiðsluáætlanir með TDS-úthlutun
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluáætlanir fyrir skattaúthlutanir sem er dreginn frá upprunalegri greiðslu (TDS).
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023336"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Setja upp greiðsluáætlanir með TDS-úthlutun

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluáætlanir fyrir skattaúthlutanir sem er dreginn frá upprunalegri greiðslu (TDS).

1. Farið í **Viðskiptaskuldir \> Greiðsluuppsetning \> Greiðsluáætlanir**.

    [![Síða greiðsluáætlunar](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Á aðgerðasvæðinu skal velja **Nýr** til að búa til greiðsluáætlun og færa inn nauðsynlegar upplýsingar.
3. Í svæðinu **Úthlutun** skal velja aðferðina sem á að nota til að úthluta greiðslunni fyrir greiðsluáætlunina:

    - Alls
    - Föst upphæð
    - Fast magn
    - Tilgreint

    Reiturinn **Úthlutun staðgreiðsluskatts** sýnir TDS-úthlutunaraðferðina fyrir greiðsluáætlunina. Ef þú velur **Alls** í reitnum **Úthlutun** er reiturinn **Úthlutun staðgreiðsluskatts** sjálfkrafa stilltur á **Alls**. Ef þú velur **Föst upphæð**, **Fast magn** eða **Tilgreint** í reitnum **Úthlutun** er reiturinn **Úthlutun staðgreiðsluskatts** sjálfkrafa stilltur á **Hlutfallslega**.

    > [!NOTE]
    > Ef svæðið **Úthlutun staðgreiðsluskatts** er stillt á **Samtals** eru afborganirnar reiknaðar á grundvelli brúttóupphæðarinnar, sem inniheldur TDS-upphæðina. Ef svæðið **Úthlutun staðgreiðsluskatts** er stillt á **Hlutfallslega** eru afborganirnar reiknaðar á grundvelli nettó reikningsupphæðar eftir að TDS-upphæðin er dregin frá.

4. Færið inn aðrar áskildar upplýsingar og lokið svo síðunni.
