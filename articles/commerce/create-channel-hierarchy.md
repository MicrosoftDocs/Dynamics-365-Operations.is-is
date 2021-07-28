---
title: Stofna yfirlitsstigveldi rásar
description: Þetta efnisatriði lýsir hvernig á að stofna yfirlitsstigveldi rásar í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
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
ms.openlocfilehash: e43c4c00545dfecb2f9a2192f81cd25300e3d6e6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352471"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Búa til skoðunarstigveldi rásar


[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að stofna yfirlitsstigveldi rásar í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Yfirlitsstigveldi rásar er notað til að flokka og skipuleggja afurðir í flokka svo hægt sé að skoða afurðirnar á netinu eða á sölustöðum (POS).

## <a name="create-a-channel-navigation-hierarchy"></a>Stofna yfirlitsstigveldi rásar

Fylgdu þessum skrefum til að stofna yfirlitsstigveldi rásar.

1. Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Yfirlitsflokkar rásar**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitnum **Heiti** færirðu inn heiti.
1. Í reitinn **Lýsing** skal færa inn lýsingu.
1. Velja **Stofna**.
1. Í aðgerðarglugganum skal velja **Nýr tegundarhnútur** til að búa til rótarhnút.
1. Í reitnum **Heiti** færirðu inn heiti.
1. Í reitinn **Lýsing** skal færa inn lýsingu.
1. Í reitinn **Stutt heiti** slærðu inn stutt heiti.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um rótarhnút.

![Dæmi um rótarhnút.](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Stofnun yfirlitsflokkahnúta

Fylgdu þessum skrefum til að búa til fleiri yfirlitsflokkahnúta til að tákna afurðaflokka á rásinni.

1. Í yfirlitsglugganum velurðu yfirhnútinn sem þú vilt bæta flokknum við.
1. Í aðgerðarúðunni velurðu **Nýr tegundahnútur**.
1. Í reitnum **Heiti** færirðu inn heiti.
1. Í reitinn **Lýsing** skal færa inn lýsingu.
1. Í reitinn **Stutt heiti** slærðu inn stutt heiti.
1. Í reitinn **Sýna röð** slærðu inn röð birtingar (valfrjálst).
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um yfirlitsstigveldi rásar sem er lokið.

![Dæmi um rásarstigveldi.](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Bæta afurðum við flokkshnúta

Fylgdu þessum skrefum til að bæta afurðum við flokkahnúta.

1. Velja flokkshnút.
1. Undir **Afurðir** velurðu **Bæta við**.
1. Finndu nýju afurðirnar sem þú vilt bæta við með afurðarnúmeri eða afurðarheiti og veldu síðan **Í lagi**.
1. Í aðgerðaglugganum velurðu **Vista.**

> [!NOTE]
> Að bæta afurðum við hnút inni í stigveldi rásarinnar dugar ekki til þess að afurðirnar birtist á valinni rás, einnig verður að tengja afurðirnar við rás. Frekari upplýsingar um vöruúrval er að finna í [Stjórnun vöruúrvals](assortments.md).

Eftirfarandi mynd sýnir dæmi um hnút með afurðum sem er bætt við.

![Afurðum bætt við flokkshnút.](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Bættu afurðareigindahópum við flokkshnúta

> [!NOTE]
> Það verður að búa til eigindahópa áður en þú getur bætt þeim við hnút innan yfirlitsstigveldi rásar.

Til að bæta afurð og eigindahóp við flokkshnút skaltu fylgja þessum skrefum.

1. Velja flokkshnút.
1. Undir **Afurðaeigindahópur** velurðu **Bæta við**.
1. Finndu eigindahópa sem þú vilt bæta við og veldu síðan **Í lagi**.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um hnút með afurðareigindir sem er bætt við.

![Eigindaflokkar afurðar á hnút.](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp úrval](set-up-assortments.md)

[Stjórna eigindum og eigindahópum](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
