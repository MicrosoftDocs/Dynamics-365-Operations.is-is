---
title: Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur
description: Þessi grein lýsir því hvernig á að búa til sérsniðnar svarsíður fyrir 4xx og 5xx stöðukóðavillur með því að nota höfundarverkfærin í Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4a3b1762cebc74c1b77f9ca60925608bc966e306
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276401"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til sérsniðnar svarsíður fyrir 4xx og 5xx stöðukóðavillur með því að nota höfundarverkfærin í Microsoft Dynamics 365 Commerce.

Ef beiðni tekst ekki, gefur þjónninn út svör við HTTP stöðukóða. 404 stöðukóðinn er sóttur og skilað ef síðu er ekki að finna og 500 stöðukóðinn er sóttur og honum skilað ef villu á netþjóni kemur upp. Í Dynamics 365 Commerce geta notendur forrita smíðað sérsniðnar villusvarsíður stöðukóða sem eru sýndar notendum vegna þessara villusvörunar við stöðukóða.

## <a name="build-a-status-code-error-response-page"></a>Búðu til síðu viðbragðsstöðu við villukóða

Fylgdu þessum skrefum til að byrja að búa til villusvörunarsíðu með stöðukóða.

1. Í vafranum þínum skaltu skrá þig inn í Dynamics 365 Commerce. 
1. Veldu síðuna sem þú vilt byggja upp 4xx / 5xx villusvörunarsíðu stöðukóða fyrir.

### <a name="build-the-template"></a>Búðu til sniðmátið

Fylgdu þessum skrefum til að byrja að búa til sniðmát fyrir villusvörunarsíðu með stöðukóða.

1. Farðu í **Sniðmát**.
1. Veljið **Ný** til að stofna nýtt síðusniðmát.
1. Í svarglugganum **Nýtt sniðmát** undir **Heiti sniðmáts** skaltu slá inn heiti fyrir nýja sniðmátið og velja síðan **Í lagi**.
1. Búðu til sniðmát, byggt á uppbyggingunni sem þú vilt að villusvörunarsíða stöðukóðans hafi.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það. 

### <a name="build-the-status-code-error-response-page"></a>Búðu til síðu viðbragðsstöðu við villukóða

Fylgdu þessum skrefum til að búa til villusvörunarsíðu með stöðukóða.

1. Fara á **Síður**.
1. Veljið **Ný** til að búa til síðu.
1. Í svarglugganum **Veljið sniðmát** skal velja sniðmát og svo, undir **Síðuheiti** skal slá inn heiti fyrir svarsíð stöðukóðavillunnar. Skildu reitinn **Vefslóð síðu** eftir auðann.
1. Búðu síðuna til.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

> [!NOTE]
> Þú getur búið til aðskildar svörunarsíður stöðukóða fyrir stöðukóðavillur 4xx og 5xx. Að öðrum kosti er hægt að nota sömu svörunarsíðu með almennum stöðukóða fyrir báða villuflokkana.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Settu upp tilvísun fyrir villusvörunarsíðu stöðukóða

Fylgdu þessum skrefum til að setja upp framsendingu fyrir villusvörunarsíðu stöðukóða.

1. Farðu á **Vefslóðir \> Nýtt \> Nýtt auknefni** og veldu villusvörusíðu stöðukóða sem þú bjóst til fyrr.
1. Í reitinn **Auknefni** skaltu slá inn annaðhvort **sjálfgefið-4xx** eða **sjálfgefið-5xx**, allt eftir villusvörunarsíðu stöðukóða sem þú ert að setja upp framsendingu fyrir. Þessi auknefni verður að birta. Annars virkar framsendingin ekki.
1. Velja skal **Í lagi** til að staðfesta tenginguna.

> [!NOTE]
> Ef þú ert að nota eina villusvörunarsíðu fyrir stöðukóða fyrir báða villuflokka skaltu endurtaka þessa aðferð til að tengja auknefni fyrir hinn villuflokkinn við sömu síðu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Vinna með sniðmát](work-with-templates.md)

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Búa til síðuvefslóð](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
