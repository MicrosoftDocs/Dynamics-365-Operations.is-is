---
title: Staðfesta greiðsluáætlanir eignarleigu í runu
description: Þetta efnisatriði útskýrir hvernig á að staðfesta margar greiðsluáætlanir í runu.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 82e985d3b1518a287fbf0916ab3afc71d4bd6466f93992b587942053af44cf59
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767081"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Staðfesta greiðsluáætlanir eignarleigu í runu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að staðfesta margar greiðsluáætlanir í runu. Greiðsluáætlanir eru annaðhvort staðfestar á grundvelli leigusamnings eða í gegnum staðfestingarrunuferli. Aðeins er hægt að bóka bókarfærslu gegn leigusamningi með staðfesta greiðsluáætlun. Staðfesting á greiðsluáætlun þjónar sem endanlegt samþykki fjárhagsupplýsinga fyrir leigu. Allar breytingar á fjárhagsupplýsingum leigusamningsins í framtíðinni eins og greiðslum og leigutímanum eru leiðrétting á leigusamningnum og skal vinna úr þeim á þann hátt.

Til að staðfesta margar greiðsluáætlanir skal fylgja þessum skrefum.

1. Opnið **Eignarleiga \> Reglubundið \> Staðfestingarruna**.
2. Á síðunni **Staðfestingarruna** skal velja **Staðfestingarruna**.
3. Í svarglugganum sem birtist er hægt að sía fyrir bækurnar sem á að staðfesta.

    - Til að staðfesta allar bækur tiltekins leiguflokks skal velja flokkinn í svæðinu **Leigusamningsflokkur**.
    - Til að staðfesta tilteknar bækur skal velja bækurnar í svæðinu **Bókarkenni**.
    - Til að staðfesta allar bækur skal kveikja á færibreytunni **Fyrir allar bækur**.

Upplýsingar fyrir nýstaðfestar bækur eru sýndar á síðunni **Staðfestar bækur**. Eftir að greiðsluáætlanir eru staðfestar er hægt að bóka upphaflegar færslur í færslubók gegn leigusamningunum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
