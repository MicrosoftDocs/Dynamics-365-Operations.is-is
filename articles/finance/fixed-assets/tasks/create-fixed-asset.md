---
title: Stofna eign
description: Þetta efnisatriði útskýrir hvernig á að stofna nýja eignafærslu úr listasíðu eignar.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 770390092342e2db496dde850a75b2f7736bd4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817102"
---
# <a name="create-a-fixed-asset"></a>Stofna eign

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að stofna nýja eignafærslu af listasíðunni **Eignir**.

Kerfið úthlutar eignanúmeri, byggt á númeraröðinni sem er úthlutað á eignaflokkinn. Ef þú notar eignarsniðmátið til að flytja inn eignir í Microsoft Excel -innbót, eða ef þú notar annað innflutningsverk stofnar kerfið sjálfkrafa eignafærslur og stigvaxandi eignanúmer.

Til að stofna eignafærslu handvirkt skal fylgja þessum skrefum.

1. Opnaðu **Yfirlitssvæði \> Einingar \> Eignir \> Eignir \> Eignir**.
2. Í **aðgerðarúðunni** velurðu **Nýtt**.
3. Í reitnum **Eignaflokkur** skal færa inn eða velja gildi. Reiturinn **Númer** verður sjálfkrafa ef búið er að virkja **Sjálfvirka tölusetninaraðgerð eigna** í **Færibreytum eigna** og **Eignaflokki**. Færa skal inn einkvæman kóða til að auðkenna eignina.
4. Í reitinn **Heiti** skal slá inn gildi. Færið inn viðbótarupplýsingar sem fyrirtækið þarf fyrir þessa eign.
5. Á **aðgerðasvæðinu** skal velja **Bækur**.
6. Í reitinn **Kaupdagsetning** skal rita dagsetningu.
7. Í reitinn **Kaupverð** skal rita tölu.

    - Sláið inn viðbótarupplýsingar sem fyrirtæki þarf fyrir þessa bók.
    - Færið inn viðbótarupplýsingar sem fyrirtækið þarf fyrir eftirstandandi bækur.

8. Lokið síðunni.

Einnig er hægt að flytja eignir inn með Excel-innbót eða með því að nota innflutningsverk úr **Gagnastjórnun** vinnusvæðinu. Áður en innflutningur er keyrður skal færa inn gildin fyrir áskilda reiti í sniðmátinu.

Ef þú hefur ekki skilgreint eignanúmerið í sniðmáti Excel-innbótarinnar, eða í gagnastjórnun, stofnar kerfið númer eignar fyrir hverja innflutta eign og raðar sjálfkrafa númeraröðinni fyrir hverja. Ef eignir eru hins vegar fluttar inn og skilgreind eignarnúmer í sniðmátinu er númeraröðinni **ekki** sjálfkrafa stigskipt. Í þessu tilviki gæti stjórnandi þurft að uppfæra númeraröðina handvirkt. Ef eignanúmerið var skilgreint í sniðmáti Excel-innbótarinnar notar kerfið skilgreint eignanúmerið og stigvaxandi númeraröðina.

> [!NOTE]                                                                                                         
> Eftir að afskriftin hefur verið bókfærð eru reitirnir **Tekin í notkun** og **Dagsetning afskriftarkeyrslu** læstir á síðunni **Bók**. Hvorugt svæðið verður uppfært úr gagnaeiningunni.

> [!WARNING]
> Eignafærslu er ekki eytt ef færslur voru bókaðar í tengdu bókinni eða ef nýstofnaða eignin er færð inn í færslubókarlínu en ekki bókuð. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]