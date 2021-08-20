---
title: Skila raðnúmerastýrðum afurðum á sölustað
description: Í þessu efnisatriði eru útskýrðir möguleikarnir á að staðfesta röðuðum vörum sem hluti af skilaferlinu í Microsoft Dynamics 365 Commerce forriti sölustaðar.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e53c8ceb91a007775fa74f0c9598a65745f01cec
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638098"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Skila raðnúmerastýrðum afurðum á sölustað

[!include [banner](includes/banner.md)]

Í þessu efnisatriði eru útskýrðir möguleikarnir á að staðfesta röðuðum vörum sem hluti af skilaferlinu í Microsoft Dynamics 365 Commerce forriti sölustaðar.

> [!NOTE]
> Í Commerce-útgáfu 10.0.20 og nýrri er boðið upp á nýjan eiginleika sem heitir **Upplifun samræmdrar skilavinnslu á sölustað**. Til að nota staðfestingu raðnúmers við vinnslu á skilapöntun á sölustað þarf að kveikja á þessum eiginleika. Upplýsingar um möguleika annarra sem þessi eiginleiki veitir þegar kveikt er á honum er að finna í [Stofna skil á sölustað](POS-returns.md).
>
> Ekki er hægt að slökkva á eiginleikanum eftir að kveikt er á honum.

## <a name="options-for-validating-serialized-returns"></a>Valkostir fyrir staðfestingu á röðuðum skilum

Þegar kveikt er á eiginleikanum **Upplifun samræmdrar skilavinnslu á sölustað** geta fyrirtæki staðfest skil á raðnúmerastýrðum vörum í gegnum sölustað. Þessi möguleiki getur varað notendur við ef raðnúmerið sem verið að skila er ólíkt upprunalega raðnúmerinu sem var selt. Í Commerce-útgáfu 10.0.20 og nýrri eru skilaboðin sem notendur fá aðeins viðvörunarboð. Notendur geta haldið áfram að vinna úr skilum varðandi raðnúmer sem er ólíkt raðnúmerinu sem var upprunalega selt.

Til að stilla villuleit raðnúmers fyrir fyrirtæki þegar kveikt hefur verið á eiginleikanum **Upplifun samræmdrar skilavinnslu á sölustað** skal fara í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Commerce-færibreytur** í Commerce Headquarters. Í flipanum **Birgðir**, í flýtiflipanum **Birgðaaðgerðir verslunar**, skal stilla valkostinn **Virkja villuleit raðnúmera á skilum sölustaðar** á **Já**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Skilavinnsla fyrir raðnúmeraðar vörur á sölustað

Ef valkosturinn **Virkja villuleit raðnúmera á skilum sölustaðar** hefur verið stilltur á **Já**, þegar raðnúmerastýrðri vöru er skilað í gegnum sölustað, getur notandinn slegið inn raðnúmerið fyrir skilalínuna í upplýsingasvæðið á síðunni **Afurðir sem hægt er að skila**. Ef raðnúmerið sem er fært inn passar ekki við upprunalegt raðnúmer sem var selt fyrir sölufærsluna fær notandinn upp viðvörunarboð. Forritið kemur hinsvegar ekki í veg fyrir að notandinn geti haldið áfram að vinna úr skilunum.

> [!NOTE]
> Sem stendur styður sölustaðurinn villuleit raðnúmera eingöngu fyrir skilalínur þar sem upprunalegt pöntunarmagn er ekki meira en einn. Ef upprunalega sölupöntunarlínan var búin til í rás sem er ekki á sölustað og ef magnið sem var pantað fyrir raðnúmeraða vöru í tiltekinni sölulínu er meira en einn verður ekki hægt að skila vörunni á réttan hátt í gegnum sölustað.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna skil á sölustað](POS-returns.md)