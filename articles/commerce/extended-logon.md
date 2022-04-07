---
title: Settu upp og notaðu aukna innskráningargetu
description: Þetta efnisatriði lýsir því hvernig á að setja upp og nota aukna innskráningargetu Microsoft Dynamics 365 Commerce Umsókn um sölustað (POS).
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d211ecfe1550f6093e1d35e7c2b37c036b50dd4a
ms.sourcegitcommit: 5aebb181004eb63210503fb566dcda5c55032bee
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/29/2022
ms.locfileid: "8491440"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Settu upp og notaðu aukna innskráningargetu

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp og nota aukna innskráningargetu Microsoft Dynamics 365 Commerce Umsókn um sölustað (POS).

Cloud POS (CPOS) og Modern POS (MPOS) bjóða upp á aukna innskráningarmöguleika sem gerir verslunarmönnum kleift að skrá sig inn á POS forritið með því að skanna strikamerki eða strjúka korti með því að nota segulröndalesara (MSR).

## <a name="set-up-extended-logon"></a>Settu upp aukna innskráningu

Til að setja upp aukna innskráningu fyrir POS-skrár í smásöluverslun skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Virkniprófílar**. 
2. Í vinstri yfirlitsrúðunni, veldu virknisniðið sem er tengt við smásöluverslunina.
3. Á **Aðgerðir** Flýtiflipi, undir **Viðbótarvalkostir fyrir innskráningu auðkenningar**, stilltu eftirfarandi valkosti á **Já** eða **Nei** eftir því sem við á:

    - **Innskráning á strikamerki starfsmanna** – Stilltu þennan valkost á **Já** ef þú vilt að starfsmenn þínir skrái sig inn á POS með því að skanna strikamerki. 
    - **Innskráning á strikamerki starfsmanna krefst lykilorðs** – Stilltu þennan valkost á **Já** ef þú vilt að starfsmenn þínir slái inn lykilorð þegar þeir skrá sig inn á POS með því að skanna strikamerki.
    - **Innskráning starfsmannakorta** – Stilltu þennan valkost á **Já** ef þú vilt að starfsmenn þínir skrái sig inn á POS með því að strjúka korti.
    - **Innskráning starfsmannakorts krefst lykilorðs** – Stilltu þennan valkost á **Já** ef þú vilt að starfsmenn þínir slái inn lykilorð þegar þeir skrá sig inn á POS með því að strjúka korti.

Strikamerki eða kort er tengt skilríkjum sem hægt er að úthluta starfsmanni. Skilríkin verða að hafa að minnsta kosti sex stafi. Strenginn sem inniheldur fyrstu fimm stafina verður að vera einstakur og telst vera *persónuskilríki* sem er notað til að fletta upp starfsmanni. Stafir sem eftir eru eru notaðir til öryggisstaðfestingar. Til dæmis ertu með tvö kort, annað þeirra hefur skilríkin 12345DGYDEYTDW og annað þeirra hefur skilríkin 12345EWUTBDAJH. Vegna þess að þessi tvö kort hafa sama auðkenni, 12345, er ekki hægt að úthluta þeim báðum til starfsmanna.

## <a name="assign-extended-logon"></a>Úthlutaðu aukinni innskráningu

Að sjálfgefnu geta aðeins stjórnendur úthlutað aukinni innskráningu til starfsmanna. Til að úthluta aukinni innskráningu á starfsmann er farið á **Aukin innskráning** á Sölustað. Síðan skal leita að starfskrafti með því að færa inn kenni stjórnanda hans í leitarreitnum. Veljið notanda og smellið á **Úthluta**. Á næstu síðu skal lesa eða skanna aukna innskráningu til að úthluta á starfsmanninn. Ef kortalestur eða skönnun er var lesin verður hnappuinn **Í lagi** tiltækur. Smellið á **Í lagi** til að vista aukna innskráningu fyrir þann starfsmann.

## <a name="delete-extended-logon"></a>Eyða aukinni innskráningu

Til að eyða aukinni innskráningu sem er úthlutað á starfsmann, skal leita að starfsmanni með því að nota aðgerðina **Aukin innskráning**. Veljið notanda og smellið á **Hætta við úthlutun**. Öll útvíkkuð skilríki sem eru tengd við starfsmanninn eru fjarlægð.

## <a name="use-extended-logon"></a>Notaðu lengri innskráningu

Eftir að útbreidd innskráning hefur verið stillt og strikamerki eða segulrönd er úthlutað á starfsmann, þarf starfsmaðurinn bara að strjúka eða skanna kortið sitt á meðan POS innskráningarsíðan er sýnd. Ef lykilorð er einnig krafist áður en hægt er að halda innskráningu áfram, er starfsmaðurinn beðinn um að slá inn lykilorðið sitt.

## <a name="extend-extended-logon"></a>Framlengdu framlengda innskráningu

Útfærsla á útvíkkuðum innskráningarmöguleikum út úr kassa krefst þess að skilríki hafi að lágmarki sex stafir að lengd og að fyrstu fimm stafirnir (skilríkiskennið) séu einstök. Það var upphaflega hugsað sem sýnishorn sem verktaki gæti sérsniðið til að uppfylla kröfur tiltekinnar útfærslu. (Til dæmis gæti það verið sérsniðið til að styðja fleiri stafi eða nota aðrar öryggisstaðfestingarreglur.) Fyrir nákvæmar upplýsingar um hvernig á að búa til viðbætur fyrir lengri innskráningu, sjá [Framlenging á aukinni innskráningarvirkni fyrir MPOS og Cloud POS](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Einnig er hægt að útvíkka innskráningarþjónustuna til að styðja við fleiri útbreidd innskráningartæki, svo sem lófaskanna. Fyrir frekari upplýsingar, sjá [POS stækkanleikaskjöl](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
