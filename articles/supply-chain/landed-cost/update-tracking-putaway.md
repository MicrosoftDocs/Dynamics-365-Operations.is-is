---
title: Uppfæra rakningu fyrir frágang
description: Þessi grein lýsir því hvernig á að setja upp og keyra uppfærslurakningu fyrir reglubundið verkefni.
author: Weijiesa
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b36fe5a9828ea018881f08b8af27d77cdf0babc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882606"
---
# <a name="update-tracking-for-put-away"></a>Uppfæra rakningu fyrir frágang

[!include [banner](../includes/banner.md)]

Reglubundna verkið *Uppfæra rakningu fyrir frágang* er hannað til að keyra sem endurtekin runa að næturlagi. Þar kemur fram hvaða ferðir hafa fengið allar birgðafærslur og hvaða ferðir hafa ekki gildi fyrir raunverulegan lokadag. Hún stillir síðan raunverulega lokadagsetningu á núgildandi dagsetningu eftir þörfum.

*Gámaaðgerðir* eru stofnaðar fyrir hvern *legg* ferðar fyrir hvern *Gám*. Þessi gildi eru skilgreind af ferðasniðmátinu sem er valið þegar ferðin er búin til. Fyrir hverja færslu gámaaðgerðar er hægt að stilla gildi fyrir reitina **Upphafsdagsetning**, **Áætluð lokadagsetning** og **Raunverulegur lokadagur**. Þessa reiti er hægt að uppfæra þegar staðfesting berst um að leggir sé byrjaður eða sé lokið.

Upplýsingar sem tengjast staðfestum dagsetningum eru yfirleitt veittar af þriðja aðila, svo sem flutningsmiðlara, vegna þess að þessum aðgerðum er haldið utan við Microsoft Dynamics 365 Supply Chain Management. Hinsvegar þarf ekki upplýsingar frá þriðja aðila til að fylgjast með komu vöru úr ferðalegg í vöruhús (merkt af frágangi vöru). Því er hægt að ákvarða rekjanleika út frá upplýsingum í Dynamics 365 Supply Chain Management.

Til að setja upp og keyra reglubundna verkið *Uppfæra rakningu fyrir frágang* skal fylgja þessum skrefum:

1. Farðu í **Heildarkostnaður \> Reglubundin verk \> Uppfæra rakningu fyrir frágang**.
1. Í svarglugganum **Uppfæra rakningu fyrir frágang**, í hlutanum **Færibreytur**, skal stilla eftirfarandi reiti:

    - **Leggur** – Veldu einkvæmt heiti/númer auðkenningar fyrir þann hluta ferðar sem á að uppfæra rakningu fyrir. Valið gildi verður að tákna komu ferðarinnar í vöruhúsið.
    - **Aðgerð** – Veldu aðgerðina sem var framkvæmd á völdum legg. Þessum gildum er úthlutað á hverja línu ferðasniðmáts í miðstöð rakningastjórnunar.

1. Til að takmarka færslufjöldann sem á að hafa með í uppfærslunni, í flýtiflipanum **Færslur til að taka með**, skal velja hnappinn **Sía**. Hefðbundin svargluggi fyrirspurnar birtist þar sem hægt er að skilgreina valskilyrði, röðunarskilyrði og tengingar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Supply Chain Management. Reitir hér eru skrifvarðir og sýna gildi sem tengjast fyrirspurninni.
1. Í flýtiflipanum **Keyra í bakgrunni** skal setja upp runu og áætlunarvalkosti eftir þörfum, rétt eins og yrði gert fyrir aðrar vinnugerðir í Supply Chain Management.
1. Veldu **Í lagi** til að nota stillingarnar þínar og til að keyra eða tímasetja uppfærsluna.
