---
title: Sjónræn framkvæmd og samvinnuframkvæmd
description: Í þessari grein er útskýrt hvernig á að fylgjast með aftengingarpunktum eftirspurnardrifinnar efnisþarfaáætlunar (DDMRP), svæðum öryggisbirgða, áætluðum pöntunum og ferli.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: ce32a4449da8e85f958f212f2c2dfd2841ca6887
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740824"
---
# <a name="visual-and-collaborative-execution"></a>Sjónræn framkvæmd og samvinnuframkvæmd

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Í þessari grein er útskýrt hvernig á að fylgjast með aftengingarpunktum eftirspurnardrifinnar efnisþarfaáætlunar (DDMRP), svæðum öryggisbirgða, áætluðum pöntunum og ferli.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Fylgjast myndrænt með öryggisbirgðum og magni fyrir valda vöru

Í Microsoft Dynamics 365 Supply Chain Management er hægt að fylgjast myndrænt með því hvernig öryggisbirgðir, lagermagn og stig nettóflæðis breytast með tímanum fyrir hvaða valda útgefna afurð sem er. Fylgið eftirfarandi skrefum til að opna og yfirfara línuritin.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu losaða vöru sem er sett upp sem aftengingarpunktur. (Frekari upplýsingar eru í [Birgðastaðsetning](ddmrp-inventory-positioning.md)).
1. Á aðgerðasvæðinu, í flipanum **Áætlun** skal velja **Vöruþekja**.
1. Á síðunni **Vöruþekja** skal velja færslu vöruþekju sem býr til aftengingarpunkt. (Þessi færsla mun sýna nafn þekjuflokks sem er settur upp til að búa til aftengingarpunkta).
1. Veldu flipann **Á lager**. Þessi flipi inniheldur graf sem sýnir hvernig lagermagn breytist með tímanum, ásamt gildinu fyrir lagerstöðuna sem var skráð fyrir tiltekið tímabil í hvert skipti sem aðaláætlanagerð var keyrð. Flipinn inniheldur líka töflu sem sýnir hvað af eftirfarandi flokkum hverrar skráðrar lagerstöðu hún tilheyrir:

    - **Mjög lítið** – Minna en helmingur af lágmarki tímabilsins.
    - **Lágmark** – Á milli helmings lágmarksins og lágmarksins.
    - **Meðaltal á lager** – Á milli lágmarks og lágmarks plús græna svæðið.
    - **Hærra en meðaltal** – Hærra en meðaltal.

    ![Söguleg gildi á lager á flipanum Á lager.](media/ddmrp-on-hand-graph.png "Söguleg gildi á lager á flipanum Á lager")

    > [!NOTE]
    > Litirnir sem eru notaðir í flipanum **Á lager** standa fyrir mismunandi svið en svipaðir litir sem notaðir eru í flipanum **Stöður öryggisbirgða**.

1. Til að sjá hvernig stöður öryggisbirgða breytast með tímanum og hvernig þær eru í samanburði við lagerstöðu og stöðu nettóflæðis skal velja flipann **Stöður öryggisbirgða**.

    ![Söguleg gildi á lager og netflæði á flipanum Biðminnisgildi](media/ddmrp-buffer-values-graph.png "Söguleg gildi á lager og netflæði á flipanum Biðminnisgildi")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Fylgjast með stöðu og áætluðum pöntunum fyrir aftengingarpunkta

Vinnusvæðið **Eftirspurnarstýrt MRP** býður upp á ýmis verkfæri ásamt afkastamælikvörðum (KPI) og yfirlitum yfir stöðu á vörum og tengdum áætluðum pöntunum aftengingarpunktsins. Til að opna það skal fara í **Aðaláætlanagerð \> Vinnusvæði \> Eftirspurnarstýrt MRP**.

![Eftirspurnarstýrt MRP vinnusvæði.](media/ddmrp-workspace.png "Eftirspurnarstýrt MRP vinnusvæði.")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Fá yfirlit yfir tengipunkta og áætlaðar pantanir

Auk vinnusvæðisins **Eftirspurnarstýrt MRP** býður Supply Chain Management upp á nokkrar síður þar sem hægt er að skoða upplýsingar um uppsetningu DDMRP, aftengingarpunkta og áætlaðar pantanir. Sumar af þessum síðum bjóða einnig upp á þægilega hnappa á aðgerðasvæðinu sem gera þér kleift að stjórna öryggisbirgðum, keyra aðaláætlanagerð og opna tengd yfirlit.

- Til að skoða stöðu aftengingarpunkts eftir stigi nettóflæðis skal fara í **Aðaláætlanagerð \> Aðaláætlanagerð \> DDMRP \> Staða aftengingarpunkta eftir nettóflæði**.
- Til að skoða stöðu aftengingarpunkts eftir lagerbirgðum skal fara í **Aðaláætlanagerð \> Aðaláætlanagerð \> DDMRP \> Staða aftengingarpunkta eftir lagerstöðu**.
- Til að skoða áætlaðar pantanir fyrir aftengingarpunkta skal fara í **Aðaláætlanagerð \> Aðaláætlanagerð \> DDMRP \> Áætlaðar pantanir fyrir aftengingarpunkta**.
- Til að skoða aftengda afhendingartíma skal fara í **Aðaláætlanagerð \> Aðaláætlanagerð \> DDMRP \> Aftengdur afhendingartími**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Hreinsun á öryggisbirgðastöðum aftengingarpunkts

Kerfið þitt mun með tímanum byggja upp mikið magn af sögulegum gögnum sem tengjast áframhaldandi útreikningum á öryggisbirgðum. Þessi sögulegu gögn valda því að gagnamagnið eykst og getur að lokum haft áhrif á afköst kerfisins. Þess vegna er mælt með því að hreinsa af og til upp gamlar öryggisbirgðastöður aftengingarpunkts.

> [!WARNING]
> Hreinsunarvinnslan fjarlægir stillingar á sögulegri öryggisbirgðastöðu og upplýsingar um sögulegar lagerbirgðir/nettóflæði. Það er ekki afturkræft.

Fylgið eftirfarandi leiðbeiningum til að hreinsa biðminnisgildi aftengingarpunkts.

1. Farðu í **Aðaláætlanagerð \> Aðaláætlanagerð \> DDMRP \> Hreinsa upp öryggisbirgðastöðu aftengingarpunkts**.
1. Í svarglugganum **Hreinsa upp öryggisbirgðastöður aftengingarpunkts** skal stilla eftirfarandi reiti:

    - **Eyða skrám sem eru eldri en (dagar)** – Tilgreindu aldur yngstu skránna sem á að geyma, í dögum. Öllum færslum um öryggisbirgðastöðu aftengingarpunkts sem eru eldri en þetta gildi verður eytt.
    - **Aðaláætlun** – Veldu aðaláætlun sem inniheldur vörur sem þessi hreinsun á að hafa áhrif á. Hreinsunin mun gilda um allar vörur í áætluninni eftir að **Síustillingarnar** sem þú tilgreinir í þessum svarglugga eru notaðar.

1. Til að takmarka þann fjölda færslna sem þessi runuvinnsla ætti að keyra á skal velja á flýtiflipanum **Færslur til að taka með** valkostinn **Sía** til að opna svargluggann **Fyrirspurn**. Svargluggi virka rétt eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Í flýtiflipanum **Keyra í bakgrunni** skal tilgreina hvernig, hvenær og hversu oft á að gera hreinsun. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veljið **Í lagi** til að bæta nýja verkinu við runubiðröð fyrir keyrslu.
