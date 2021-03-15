---
title: Taxtaforstillingar
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp gögn fyrir taxtaforstillingar.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973961"
---
# <a name="rating-profiles"></a>Taxtaforstillingar

Taxtaforstilling líkist vörustjórnunarsamningi (en ekki löglegum þjónustusamningi). Það er notað til að ákvarða flutningsgjaldskrá fyrir farma. 

Taxtaforstilling er einkvæm fyrir farmflytjanda. Í forstillingunni er hægt að tengja farmflytjanda við aðalsniðmát taxta. Aðalsniðmát taxta skilgreinir úthlutun grunntaxta og grunntaxtann. Grunntaxti ákvarðar taxta farmflytjanda.

Þú getur sett upp taxtaforstillingar með því að nota almenna uppsetningarskjámynd sem er með yfirlit yfir allar núverandi taxtaforstillingar. Einnig er hægt að setja upp taxtaforstillingar beint úr farmflytjanda. Í báðum tilvikum er hægt að nota upplýsingarnar sem eru settar upp fyrir fjárhagsforstillinguna.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Stofna eða breyta einkunnasniðmátið á síðunni Taxtaforstillingar

Á síðunni **Taxtaforstillingar** er hægt að fara yfir allar fyrirliggjandi taxtaforstillingar. Einnig er hægt að breyta fyrirliggjandi forstillingum og búa til nýjar forstillingar.

1. Opnið **Flutningsstjórnun \> Uppsetning \> Taxti \> Taxtaforstilling**.
1. Í aðgerðasvæði skal velja **Nýtt** til að bæta nýrri taxtareglu við hnitanetið eða velja **Breyta** til að breyta fyrirliggjandi forstillingu.
1. Í línunni fyrir nýja eða fyrirliggjandi taxtaforstillingu skal stilla eftirfarandi reiti:

    - **Taxtaforstilling** – Færðu inn einkvæmt kenni fyrir taxtaforstillinguna.
    - **Heiti** - Færið inn lýsandi heiti á taxtaforstillingunni.
    - **Farmflytjandi** – Veljið farmflytjanda. Taxtaforstillingin sem verið er að setja upp verður einnig sýnd á síðunni **Farmflytjendur** fyrir valinn farmflytjanda.
    - **Svæði** og **Vöruhús** – Veljið svæði og vöruhús.
    - **Taxtavél** – Veljið taxtavél fyrir taxtaforstillinguna.
    - **Aðalsniðmát taxta** – Veljið aðalsniðmát taxta fyrir taxtaforstillinguna. Hægt er að nota taxtasniðmátinu til að skilgreina með grunngerð og taxtagrunn. Frekari upplýsingar er að finna í [Setja upp aðalsniðmát taxta](set-up-rate-masters.md).
    - **Flutningstímavél** -Veljið flutningstímavél fyrir taxtaforstillinguna.
    - **Eldsneytisvísir flutningsaðila** – Veljið eldsneytisvísi flutningsaðila fyrir taxtaforstillinguna.
    - **Upphafsdagsetning og-tími** og **Lokadags. og-tími** – Skilgreinið tímabilið þegar taxtaforstillingin á að vera virk.

1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Búa til taxtaforstillingu beint á síðu farmflytjanda

1. Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Farmflytjendur**.
1. Veldu farmflytjanda í listanum.
1. Í flýtiflipanum **Taxtaforstilling** velur þú **Nýtt** til að búa til taxtaforstillingu.
1. Stillið reitina fyrir nýja taxtaforstilling. Þessir reitir samsvara reitum á síðunni **Taxtasniðmátum**, eins og lýst er í fyrri hluta atriðins.

> [!NOTE]
> Forstillingar sem búnar eru til á síðunni **Farmflytjendur** eru einnig sýndar á síðunni **Taxtaforstillingar**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]