---
title: Viðbótargögn um staðsetningu
description: Í þessari grein er að finna yfirlit yfir nýjar staðsetningar sem bætt hefur verið við Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336516"
---
# <a name="additional-location-zones"></a>Viðbótargögn um staðsetningu

[!include [banner](../includes/banner.md)]

Þrír nýir svæðareitir eru í boði í Microsoft Dynamics 365 Supply Chain Management. Vöruhúsastjórnendur geta notað þá til að skilgreina fleiri fyrirtæki eða útlit vöruhúss. Nýju svæðareitina er hægt að stilla annaðhvort handvirkt eða með því að nota leiðsögnina **Uppsetning staðsetningar**. Hægt er að nota þá fyrir allar fyrirspurnir eða síur sem nota staðsetningartöfluna.

Ekki er krafist frekari uppsetningar til að nota svæðareitina.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Kveikja eða slökkva á eiginleika „Fleiri staðsetningarsvæði“

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. Sem hluti af Supply Chain Management, útgáfa 10.0.25, er sjálfgefið kveikt á þessum eiginleika. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Viðbótargögn um staðsetningu* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="use-location-zones"></a>Nota staðsetningar

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Uppsetningarforrit staðsetningar**.
2. Stilla eftirfarandi gildi:

    - Í reitnum **Vöruhús** skal velja _62_.
    - Í reitnum **Svæðiskenni** skal velja _FLOOR_.
    - Í reitnum **Viðbótarsvæði 1** skal velja _PICKZONE1_.
    - Í reitnum **Viðbótarsvæði 2** skal velja _WEBSHOP1_.
    - Í reitnum **Forstillingarkenni staðsetningar** skal velja _FLOOR_.

3. Veljið línuna **Gólf**.
4. Í reitinn **Númer frá** skal slá inn _1_. Í reitinn **Númer til** skal slá inn _3_.
5. Veljið línuna **Gangur**.
6. Í reitinn **Númer frá** skal slá inn _1_. Í reitinn **Númer til** skal slá inn _5_.
7. Velja **Stofna**.
8. Skilaboð birtast sem segja að búið sé að bæta við nýju staðsetningunum. Veljið hnappinn **Sýna skilaboð** til að skoða skilaboðin.
9. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**. Nýju staðsetningarnar birtast í listanum og allir svæðareitir eru tiltækir (þ.e. núverandi svæðareitur og nýju svæðareitirnir).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]