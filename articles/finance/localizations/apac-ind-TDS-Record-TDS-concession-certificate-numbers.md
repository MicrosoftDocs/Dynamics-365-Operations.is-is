---
title: Skrá vottorðanúmer TDS-skattaívilnunar
description: Í þessu efnisatriði er útskýrt hvernig á að skrá númer skattfrádráttarskírteinis á heimildarskírteini (TDS) sem eru gefin út til lánardrottna.
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
ms.openlocfilehash: 994ddbb4666c326d237d53d529ba126f42d48595
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727146"
---
# <a name="record-tds-concession-certificate-numbers"></a>Skrá vottorðanúmer TDS-skattaívilnunar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að skrá númer skattfrádráttarskírteinis á heimildarskírteini (TDS) sem eru gefin út til lánardrottna.

1. Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Ívilnanir staðgreiðsluskatts**.
2. Í reitnum **Skattgerð** skal velja **TDS** til að setja upp ívilnunarvottorð fyrir skattgerð TDS.
3. Í flipanum **Yfirlit** skal velja **Alt+N** til að stofna línu.

    [![Haus nýju línunnar.](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. Í reitnum **Staðgreiðsluskattskóði** skal velja TDS-skattkóða sem ívilnunarvottorð eru gefin út fyrir. Reiturinn **Heiti staðgreiðsluskattskóða** sýnir heiti TDS-skattkóðans.
5. Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal skilgreina gildistímabil fyrir ívilnunarvottorðið sem notar TDS skattkóðann til að reikna út TDS fyrir lánardrottinn á sérstökum grunni.
6. Í reitinn **Athugasemdir** eru færðar inn athugasemdir.
7. Í reitinn **kafli** er færður inn lagakaflakóðinn sem TDS-ivilnunarvottorðið er notað undir.

    Ef kaflakóðinn er 197 birtist gildið „A“ bæði í dálknum „Ástæða fyrir engum frádrætti/lægri frádrætti“ í eyðublaði 26Q og dálknum „Ástæða fyrir engum frádrætti/lægri frádrætti/hæækun (ef einhver er)“ í eyðublaði 27Q. Ef kaflakóðinn er 197A birtist gildið „B“ á báðum þessum stöðum.

8. Veldu **Vottorð** flýtiflipann til að skrá vottorðsskírteini TDS-ívilnunar fyrir lánardrottna.
9. Í svæðinu **Lánardrottinsreikningur** er valinn lánardrottinsreikningur sem TDS-ívilnunarvottorðið er gefið út fyrir.
10. Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal skilgreina gildistímabil TDS-ívilnanavottorðsins.

    Útreikningur TDS á ívilnunargrunni er byggður á tímabilinu þegar vottorðið er stofnað fyrir lánardrottin.

11. Í reitnum **Vottorð** skal færa inn númer vottorð TDS-ívilnana.

    [![Vottorðsflýtiflipi.](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Lokið síðunni.
