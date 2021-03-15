---
title: Setja upp dótturfyrirtæki lögaðila fyrir sameiningu
description: Þetta efnisatriði útskýrir hvernig eigi að vinna með bókhaldslykla fyrir samstæðufyrirtæki.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 4ffe0ac0b11a3f58ca4a893d8786f04b4067b270
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975534"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Setja upp dótturfyrirtæki lögaðila fyrir sameiningu

[!include [banner](../includes/banner.md)]

Aðferðin sem notuð er til að útbúa reikninga dótturfyrirtækis fyrir samstæðu fer, að hluta til, eftir því að hve miklu marki skipulag bókhaldslykilsins í dótturfyrirtæki lögaðila endurspeglar bókhaldslykilinn í sameinaða lögaðilanum.

Áður en hafist er handa við samsetninguna sem hluti af lokun í lok tímabils, þarf að klára undirbúningsverkþætti fyrir lokun tímabils, en ekki á að loka dótturfyrirtækjalyklunum þar til samsetningunni er lokið. Frekari upplýsingar um lokun í lok tímabils er að finna í [Loka fjárhag í lok tímabils](close-general-ledger-at-period-end.md) og [Loka reikningsárinu](tasks/close-fiscal-year.md).

> [!NOTE]
>  Mælt er með því að nota Management reporter fyrir Microsoft Dynamics 365 Finance til að sameina fjárhagsniðurstöður fyrir marga lögaðila á sameinuðu sniði. Management Reporter gerir kleift að stofna sameinaðar fjárhagsskýrslur yfir alla lögaðila, nota Excel til að flytja inn samstæðugögn frá öðrum upprunum og umbreyta upphæðum í hvaða fjölda skýrslugjaldmiðla sem er án þess að þurfa að keyra sameiningarferlið í Dynamics 365 Finance.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Aðallyklum dótturfyrirtækis varpað í sameinaða aðallykla

Ef bókhaldslykill í lögaðila dótturfyrirtækis fylgir ekki bókhaldslykli í sameinaða lögaðilanum, er hægt að varpa aðallyklum í dótturfyrirtækinu í aðallykla í sameinaða lögaðilanum.

1. Í *lögaðili dótturfyrirtækis* skal fara í **Fjárhagur \> Uppsetning** \> **Bókhaldslykill \> Bókhaldslykill**.
2. Veljið bókhaldslykil. Í flýtiflipanum **Aðallyklar** skal velja aðallykil og síðan velja **Breyta**.
3. Veljið hvern aðallykil dótturfyrirtækis sem verður að varpa á sameinaðan aðallykil. Í flýtiflipanum **Almennt**, í reitinn **Samstæðulykill**, skal færa inn lykilinn í sameinuðum lögaðila þar sem millifæra þarf stöðuna eða færslur valins aðallykils dótturfyrirtækis. Hægt er að slá inn sama sameinaða aðallykilinn fyrir marga lykla dótturfyrirtækis.

    > [!NOTE]
    > Ef gerðir aðallykla dótturfyrirtækjalyklanna sem eru varpaðir eru öðruvísi en gerðir aðallykla lyklanna í sameinaða lögaðilanum, verða gildi lykla sem hafa gerð aðallykils **Samtala** yfirskrifuð á meðan á sameiningu stendur.

4. Undirbúa skýrslur og fjárhagsskýrslur fyrir sameinaðan lögaðila sem byggist á fjárhagsvíddum. Fylgið þessum skrefum til að varpa fjárhagsvíddum sem eru notaðar í dótturfyrirtækjalyklunum í fjárhagsvíddir í sameinaða lögaðilanum:

    1. Í *lögaðila dótturfyrirtækis* skal fara í **Fjárhagur \> Uppsetning \> Fjárhagsvíddir \> Fjárhagsvíddir**, velja fjárhagsvídd og síðan velja **Fjárhagsvíddargildi**.
    2. Veljið fjárhagsvíddargildi til að varpa á annað fjárhagsvíddargildi í sameinaða lögaðilanum.
    3. Í flýtiflipanum **Almennt**, í reitinn **Flokkavídd**, skal færa inn fjárhagsvíddina í sameinuðum lögaðila. Við sameiningu er þessari fjárhagsvídd úthlutað á færslur og stöður sem nota valda fjárhagsvídd í dótturfyrirtæki lögaðilans. Fjárhagsvíddirnar sem eru færðar hér inn verður að nota í sameinaða lögaðilanum. Hægt er að úthluta fjárhagsvíddina sem er notuð sem flokksfjárhagsvídd á nokkrar fjárhagsvíddir dótturfyrirtækja.

5. Ef verið er að gera sameiningu á netinu skal fylgja þessum skrefum til að ganga úr skugga um að flutningar gangi samkvæmt áætlun:

    1. Í *sameinuðum lögaðila* skal fara í **Fjárhagur \> Reglubundið \> Sameina \> Sameina \[Flytja út\]** til að opna síðuna **Sameina \[á netinu\]**.
    2. Í flipanum **Skilyrði** skal velja gátreitinn **Nota samstæðulykil**.
    3. Í flipanum **Fjárhagsvíddir** skal velja viðeigandi fjárhagsvíddir.
    4. Fyrir hverja fjárhagsvídd sem er valin skal færa inn tölu í reitinn **Röð hluta** til að gefa til kynna röðina sem víddirnar eiga að birtast í.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Sömu bókhaldslyklum viðhaldið í dótturlögaðilum og sameinuðum lögaðilum

Aðallyklar í dótturfyrirtæki lögaðila gætu verið með sömu lyklanúmer og sömu uppbyggingu fyrir bókhaldslykil og aðallykillinn í sameinaða lögaðilanum. Þá þarf ekki að varpa handvirkt aðallyklum í dótturfyrirtækinu í aðallykla í sameinaða lögaðilanum.

Áður en hafist er handa við sameiningu skal fylgja þessum skrefum.

1. Í *sameinuðum lögaðila* skal fara í **Fjárhagur \> Reglubundið \> Sameina \> Sameina \[Flytja út\]** til að opna síðuna **Sameina \[á netinu\]**.
2. Veljið gátreitinn **Nota samstæðulykil**. Á meðan á sameiningu stendur verða færslur og stöður sjálfkrafa fluttar á réttan lykil.

> [!NOTE]
> Ef lyklarnir passa ekki saman stöðvast sameiningin og munu skilaboð berast.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Stofna bókhaldslykla fyrir sameinaða lögaðilann á grundvelli eldri bókhaldslykils

Hægt er að gera sameiningu jafnvel ef bókhaldslykill hefur ekki þegar verið stofnaður í sameinaða lögaðilanum.

- Ef búið er að skipuleggja lykilskipulagið sem á að nota í sameinaða lögaðilanum er hægt að varpa dótturfyrirtækislyklum í þetta skipulag.
- Ef engin vörpun á dótturfyrirtækjalyklum eru lyklarnir í sameinaða lögaðilanum stofnaðir sjálfkrafa þegar gögn dótturfyrirtækja eru flutt í sameinaða lögaðilann. Þessir lyklar byggjast á aðallyklinum. Væntanlegum gögnum er safnað upp í lykla í sameinaða lögaðilanum sem hefur sama lykilnúmer og dótturfyrirtækjalyklarnir.

Burtséð frá því hvort lyklum hafi verið varpað, þá þarf að hreinsa gátreitinn **Nota samstæðulykil** á síðunni **Sameina** í sameinuðum lögaðila áður en þessi gerð sameiningar er keyrð.

> [!NOTE]
> Hægt er að nota þessa aðferð til að stofna bókhaldslykla í sameinaða lögaðilanum frá bókhaldslyklunum í einum af lögaðilum dótturfyrirtækisins. (Frekari upplýsingar er að finna í [Flokkar samstæðulykla og viðbótar samstæðulyklar](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Síðan er viðeigandi sameiningarumreikningsregla úthlutuð til sérhvers sameinaðs aðallykils, og sameiningin keyrð fyrir öll dótturfyrirtæki lögaðilans.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]