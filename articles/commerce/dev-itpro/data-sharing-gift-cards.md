---
title: Gagnamiðlun milli fyrirtækja fyrir gjafakort
description: Þessi grein lýsir því hvernig á að stilla Microsoft Dynamics 365 Commerce til að nota Dynamics 365 Finance gagnadeilingarvirkni milli gagnasvæða til að samstilla gjafakortagögn.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: b56890b546c3cd74b75cf447e62495733ea8d288
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387373"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Gagnamiðlun milli fyrirtækja fyrir gjafakort

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein lýsir því hvernig á að stilla Microsoft Dynamics 365 Commerce þannig að það noti Dynamics 365 Finance gagnadeilingarvirkni til að samstilla gjafakortagögn. Þá er hægt að nota gagnaskrársamnýtingu til að deila gögnum á milli tveggja gagnasvæða. Þannig getur innri gjafatafla Commerce deilt gögnum á milli tveggja fyrirtækjaeininga. Fyrir frekari upplýsingar um Dynamics 365 Finance gagnadeilingu milli fyrirtækja, sjá [Samnýting gagna milli fyrirtækja](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | Lýsing |
|---|---|
| Fyrirtæki | Lögaðilinn í Dynamics 365 Finance umhverfinu. |
| Gjafakort | The Dynamics 365 Commerce innri gjafakortavöru. |

## <a name="prerequisites"></a>Forkröfur

Notendur verða að stilla umhverfi sitt fyrir samnýtingu gagna milli fyrirtækja eins og lýst er í [Samnýting gagna milli fyrirtækja](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

**SmásöluGjafakortatöflu** verður að hafa **DataSharingType** reit stillt á **Afrit** til að virkja tvítekna færsludeilingu (DRS) fyrir gjafakortaborðið. Fyrir frekari upplýsingar, sjá [Samnýting gagna milli fyrirtækja fyrir þróunaraðila](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Stilltu gagnadeilingu milli fyrirtækja fyrir gjafakort

Til að stilla gagnadeilingu milli fyrirtækja fyrir gjafakort skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum viðskipta, farðu til **Kerfisstjórnun \> Uppsetning \> Stilltu gagnadeilingu milli fyrirtækja**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við samnýtingarskrá.
1. Í **Nafn** reit, sláðu inn heiti fyrir samnýtingarskrána (td **Gjafabréf**).
1. Í **Töflur og reiti til að deila** kafla, veldu **Bæta við**.
1. Í **Deildu nýju borði** valmynd, í **Nafn töflu** reit, slá inn **VERSLUNARGJAFAKORT** (borðið fyrir smásölugjafakort). The **Merki á borði** reiturinn ætti sjálfkrafa að vera stilltur á **Gjafakortaborð**.
1. Gakktu úr skugga um að **Vistaðu gögn fyrir hvert fyrirtæki**, **einstaka vísitölu**, og **Ekki deilt enn** gátreitirnir eru allir valdir. Val á þessum gátreitum kallar fram sannprófanir sem tengjast gagnadeilingarvirkninni.
1. Velja **Bæta við töflu**. The **Gjafakortaborð (RetailGiftCardTable)** skrá ætti nú að birtast undir **Töflur og reiti til að deila**. Veldu táknið (^) til að skoða alla töflureitina sem eru sjálfkrafa tengdir töflunni til að deila.
1. Í **Fyrirtæki sem deila gögnum í þessum töflum** kafla, veldu **Bæta við** að bæta við fyrirtæki til að deila gögnum með.
1. Í röðinni undir **Fyrirtæki**, veldu fyrirtæki í fellilistanum.
1. Í **Nafn** reit, sláðu inn nafn fyrirtækis.
1. Endurtaktu skref 8 til 10 til að bæta við fleiri fyrirtækjalínum.
1. Þegar þú hefur lokið við að bæta við fyrirtækjalínum skaltu velja á Aðgerðarrúðunni **Virkja**.
1. Þú færð viðvörunarskilaboð sem segja: „Mælt er með því að framkvæma þessa aðgerð eingöngu á verslunartíma. Allar samhliða færsluaðgerðir munu mistakast fyrir töflur í stefnunni. Viltu halda áfram?" Veldu **Já** að samþykkja.
1. Þú færð viðvörunarskilaboð sem segir: "Viltu afrita öll núverandi gögn yfir öll sameiginleg fyrirtæki núna?" Veldu **Já** að samþykkja.

Eftir að þú samþykkir bæði skilaboðin munu töflur byrja að afrita gögn yfir stillt fyrirtæki. Innstæður sem verða á móti einu gjafakorti fyrirtækisins verða þá sýnilegar hinu fyrirtækinu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Algengar spurningar um greiðslur](payments-retail.md)

[Greiðsluferliseining](../add-checkout-module.md)

[Greiðslueining](../payment-module.md)
