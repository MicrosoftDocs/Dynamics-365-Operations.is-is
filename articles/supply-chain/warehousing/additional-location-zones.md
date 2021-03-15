---
title: Viðbótargögn um staðsetningu
description: Í þessu efnisatriði er að finna yfirlit yfir nýjar staðsetningar sem bætt hefur verið við Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 662725edf5bf8d95be038f7c989b73d8d05fa0df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996427"
---
# <a name="additional-location-zones"></a>Viðbótargögn um staðsetningu

[!include [banner](../includes/banner.md)]

Þrír nýir svæðareitir eru í boði í Microsoft Dynamics 365 Supply Chain Management. Vöruhúsastjórnendur geta notað þá til að skilgreina fleiri fyrirtæki eða útlit vöruhúss. Nýju svæðareitina er hægt að stilla annaðhvort handvirkt eða með því að nota leiðsögnina **Uppsetning staðsetningar**. Hægt er að nota þá fyrir allar fyrirspurnir eða síur sem nota staðsetningartöfluna.

Ekki er krafist frekari uppsetningar til að nota svæðareitina.

## <a name="turn-on-the-additional-location-zone-feature"></a>Kveiktu á eiginleikanum „Viðbótargögn um staðsetningu“

Áður en þú getur notað eiginleikann *Aukaleg staðsetning*, verður að vera kveikt á honum í kerfinu þínu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Aukaleg staðsetning*

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