---
title: Grunnstilla rás til að nota skoðunarstigveldi rásar
description: Þetta efnisatriði lýsir hvernig á að grunnstilla rás til að nota skoðunarstigveldi rásar í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 79054573fa6f86bea5c4fe014233d71c01020348
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352591"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Grunnstilla rás til að nota skoðunarstigveldi rásar


[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að grunnstilla rás til að nota skoðunarstigveldi rásar í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Stigaleiðir rásarinnar skipuleggja vörur í flokka svo hægt sé að vafra um vörurnar á e-verslunarsíðu eða á sölustöðum (POS). Smásölu- og netrásir verða að vera stilltar með stigveldi rásar.

## <a name="configure-the-channel"></a>Stilltu rásina

Fylgdu þessum skrefum til að stilla rásina til að nota stigveldi rásarinnar.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.
1. Velja skal rásina sem á að skilgreina.
1. Í aðgerðarúðunni skal velja **Stilla eigind lýsigagna**.
1. Í fellilistanum **Tegundastigveldi** velurðu viðeigandi yfirlitsstigveldi rásarinnar.
1. Í aðgerðaglugganum velurðu **Vista.**
1. Undir **Eiginleikahópur** bætirðu við hvaða eigindahópum sem verða hnattrænir eiginleikar fyrir alla hnúta.

Eftirfarandi myndi sýnir hvernig stilla skuli rás til að nota stigveldi rásarinnar.

![Dæmi um rásaskilgreiningu.](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Stilla eigind lýsigagna

Ef þú setur lýsigögn eigindisins gerir það kleift að stilla eiginleika á hverjum hnút.

Til að stilla lýsigögn eigindar skal fylgja þessum skrefum.

1. Í aðgerðarúðunni skal velja **Stilla eigind lýsigagna**.
1. Fyrir hvern hnút velurðu **Afurðareigindir rásarinnar**.
1. Stilltu **Sýna eigindi á rás** á **Já** og **Hægt að fínpússa** að **Já**, til að gera fágunaraðilum kleift á þeirri rás.
1. Eftir að hafa stillt hvern hnút eins og óskað er, í **Aðgerðaglugganum** velurðu hnappinn **Vista** til að vista.
1. Veldu **X** efst í hægra horninu til að loka þessum skjá aftur á síðunni **Rásarflokkar og afurðareigindir**.

Eftirfarandi mynd sýnir dæmi um eiginleika rásafurða sem eru stilltir á hnút rásaflokks.

![Rásareigindir á hnút rásaflokks.](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Birta breytingar

Eigi breytingarnar að öðlast gildi verður að birta breytingarnar.

Til að birta breytingar skal fylgja þessum skrefum.

1. Veldu aðgerðarrúðuna **Birta uppfærslur rásar**.
1. Í glugganum **Birta rásaruppfærslur** velurðu **Í lagi**.

Eftirfarandi mynd sýnir hvernig á að birta uppfærslur á rásum.

![Birta uppfærslur rásar.](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Búa til skoðunarstigveldi rásar](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]