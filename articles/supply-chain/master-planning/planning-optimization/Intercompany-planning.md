---
title: Áætlanagerð innan samstæðu
description: Þessi grein lýsir áætlanagerð milli fyrirtækja og útskýrir hvernig á að stilla áætlanagerð milli fyrirtækja með áætlanagerð fínstillingu í Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 65467fd9525ae8fb5a65a9316b7307f611fa6e42
ms.sourcegitcommit: ec15857b753ebedd86503170efd54c8007b87231
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475613"
---
# <a name="intercompany-planning"></a>Áætlanagerð innan samstæðu

[!include [banner](../../includes/banner.md)]

Í sumum fyrirtækjum eru aðgerðir vörustjórnunar háðar öðrum lögaðilum (fyrirtækjum) innan fyrirtækisins. Þessar aðgerðir eru meðhöndlaðar með sölu og innkaupum innan samstæðu, vegna þess að hver lögaðili hefur aðskilda bókhaldslykla.

Þessi grein lýsir áætlanagerð milli fyrirtækja og útskýrir hvernig á að stilla áætlanagerð milli fyrirtækja með áætlanagerð fínstillingu í Microsoft Dynamics 365 Supply Chain Management.

Þessi grein notar eftirfarandi mikilvæga samstæðuskilmála:

- **Fyrir ofan** – Afstæð tilvísun í fyrirtæki eða aðfangakeðju. Gefur til kynna hreyfingu í áttina að hráefnisbirgi.
- **Fyrir neðan** – Afstæð tilvísun í fyrirtæki eða aðfangakeðju. Gefur til kynna hreyfingu í áttina að viðskiptavininum.
- **Áætluð eftirspurn innan samstæðu** – Áætluð eftirspurn eftir afurð í fyrirtæki miðað við áætlaða eftirspurn afurðarinnar hjá fyrirtæki fyrir neðan.

Við aðaláætlanagerð getur áætlun í einu fyrirtæki falið í sér áætlaða eftirspurn innan samstæðu sem tengist áætluðum pöntunum úr áætlun í öðru fyrirtæki. Þessi eiginleiki er gagnlegur vegna þess að hann býður upp á fullan sýnileika á áætluðum pöntunum milli fyrirtækja. Slíkt tryggir einnig að allar nauðsynlegar áætlaðar birgðapantanir séu stofnaðar, en án þess að krefjast þess að áætlaðar pantanir séu staðfestar fyrir eftirspurn innan samstæðunnar.

Þegar aðaláætlanagerð er keyrð úr aðaláætlun sem inniheldur áætlaða eftirspurn fyrir neðan, verða innkaupatillögur úr tengdum lánardrottnum innan samstæðu teknar með í áætluninni sem eftirspurn.

## <a name="required-setup"></a>Nauðsynleg uppsetning

Til að nota samstæðuáætlun verður þú að undirbúa kerfið þitt á eftirfarandi hátt:

1. Losa verður viðeigandi afurðir í öllum viðeigandi fyrirtækjum. Fyrir frekari upplýsingar, sjá [Stilltu og notaðu viðskipti milli fyrirtækja í Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Eftirspurn fyrir neðan verður að svara með innkaupum af lánardrottinn sem er með samstæðutengsl við fyrirtækið fyrir ofan og viðeigandi sjálfgefnar birgðavíddir (svæði og vöruhús) viðskiptavinarins. Fyrir frekari upplýsingar, sjá [Stilltu og notaðu viðskipti milli fyrirtækja í Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Aðaláætlunin í fyrirtækinu fyrir ofan verður að innihalda áætlaða eftirspurn fyrir neðan og tilgreina verður viðeigandi fyrirtæki og aðaláætlun í áætlunum fyrir neðan.

## <a name="include-planned-downstream-demand"></a>Þ.m.t. áætluð eftirspurn forstreymis

Fylgið eftirfarandi skrefum til að skilgreina aðaláætlunina þannig að hún feli í sér áætlaða eftirspurn fyrir neðan.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Velja eða stofnið aðaláætlun.
1. Á flýtiflipanum **Samstæðuáætlun** skal stilla eftirfarandi reiti:

    - **Taka með áætlaða eftirspurn fyrir neðan** – Stillið þennan valkost á *Já* til að virkja áætlanagerð innan samstæðu fyrir aðaláætlunina.
    - **Áætlanir fyrir neðan** – Ef þú stillir **Taka með áætlaða eftirspurn fyrir neðan** á *Já* skaltu nota verkfæraslána og hnitanetið til að bæta við aðaláætlunum frá öðrum fyrirtækjum eins og óskað er eftir.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Festa milli fyrirtækja með því að nota festingu á mörgum stigum

Í marglaga þarfarakningu er hægt að skoða þarfarakningu í mörgum fyrirtækjum til að sjá upphaflegan uppruna eftirspurnarinnar sem framboð mætir.

Fylgdu eftirfarandi skrefum til að skoða marglaga upplýsingar um þarfarakningu.

1. Fara í **Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir**.
1. Velja eða opna áætlaða pöntun.
1. Á aðgerðasvæðinu, í flipanum **Skoða**, í flokknum **Kröfur**, skal velja **Festingu á mörgum stigum**.

### <a name="intercompany-example-that-involves-two-companies"></a>Samstæðudæmi sem inniheldur tvö fyrirtæki

Í þessu dæmi er áætluð framleiðslupöntun stofnuð í USMF-fyrirtækinu til að mæta sölupöntun DEMF-fyrirtækisins. Í USMF er bein eftirspurn áætluð eftirspurn innan samstæðu. Til að þessi eftirspurn birtist í USMF er aðaláætlanagerð keyrð fyrst í DEMF og síðan í USMF.

Eftirfarandi mynd sýnir hvernig þetta dæmi kann að birtast á síðunni **margbrotin Þarfarakning** fyrir áætluðu framleiðslupöntunina.

![Samstæðudæmi sem inniheldur tvö fyrirtæki.](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Dæmi um fyrirtæki innan samstæðu sem felur í sér þrjú fyrirtæki

Í þessu dæmi er áætluð innkaupatillaga stofnuð í USMF-fyrirtækinu til að mæta sölupöntun FRRT-fyrirtækisins. Í fyrirtækjunum DEMF og USMF er bein eftirspurn áætluð eftirspurn innan samstæðu. Til að þessi eftirspurn birtist í USMF er aðaláætlanagerð keyrð fyrst í FRRT, síðan í DEMF og loks í USMF.

Eftirfarandi mynd sýnir hvernig þetta dæmi kann að birtast á síðunni **margbrotin Þarfarakning** fyrir áætluðu framleiðslupöntunina.

![Dæmi um fyrirtæki innan samstæðu sem felur í sér þrjú fyrirtæki.](media/IntercompanyPlanning2.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
