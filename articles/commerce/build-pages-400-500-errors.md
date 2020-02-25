---
title: Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur
description: Þetta efnisatriði lýsir því hvernig á að búa til sérsniðnar svarsíður fyrir villur í 4xx og 5xx stöðukóða með því að nota höfundatólin í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001131"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Búa til sérstilltar svarsíður fyrir 4xx/5xx stöðukóðunarvillur


[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að búa til sérsniðnar svarsíður fyrir villur í 4xx og 5xx stöðukóða með því að nota höfundatólin í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Ef beiðni tekst ekki, gefur þjónninn út svör við HTTP stöðukóða. 404 stöðukóðinn er sóttur og skilað ef síðu er ekki að finna og 500 stöðukóðinn er sóttur og honum skilað ef villu á netþjóni kemur upp. Í Dynamics 365 Commerce geta notendur forrita smíðað sérsniðnar villusvarsíður stöðukóða sem eru sýndar notendum vegna þessara villusvörunar við stöðukóða.

## <a name="build-a-status-code-error-response-page"></a>Búðu til síðu viðbragðsstöðu við villukóða

Fylgdu þessum skrefum til að byrja að búa til villusvörunarsíðu með stöðukóða.

1. Í vafranum þínum skaltu skrá þig inn í Dynamics 365 Commerce. 
1. Veldu síðuna sem þú vilt byggja upp 4xx / 5xx villusvörunarsíðu stöðukóða fyrir.

### <a name="build-the-template"></a>Búðu til sniðmátið

Fylgdu þessum skrefum til að byrja að búa til sniðmát fyrir villusvörunarsíðu með stöðukóða.

1. Farðu í **Sniðmát \> Nýtt sniðmát**.
1. Gefðu nýja sniðmátinu heiti.
1. Búðu til sniðmát, byggt á uppbyggingunni sem þú vilt að villusvörunarsíða stöðukóðans hafi.
1. Skráðu sniðmátið inn og birtu það.

### <a name="build-the-status-code-error-response-page"></a>Búðu til síðu viðbragðsstöðu við villukóða

Fylgdu þessum skrefum til að búa til villusvörunarsíðu með stöðukóða.

1. Farðu á **Síður \> Ný síða**.
1. Nefndu villusvörusíðu stöðukóða, en stilltu **ekki** reitinn **Vefslóð**.
1. Búðu síðuna til.
1. Skráðu síðuna inn og birtu hana.

> [!NOTE]
> Þú getur búið til aðskildar svörunarsíður stöðukóða fyrir stöðukóðavillur 4xx og 5xx. Að öðrum kosti er hægt að nota sömu svörunarsíðu með almennum stöðukóða fyrir báða villuflokkana.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Settu upp tilvísun fyrir villusvörunarsíðu stöðukóða

Fylgdu þessum skrefum til að setja upp framsendingu fyrir villusvörunarsíðu stöðukóða.

1. Farðu á **Vefslóðir \> Nýtt \> Nýtt auknefni**og veldu villusvörusíðu stöðukóða sem þú bjóst til fyrr.
1. Í reitinn **Auknefni** skaltu slá inn annaðhvort **sjálfgefið-4xx** eða **sjálfgefið-5xx**, allt eftir villusvörunarsíðu stöðukóða sem þú ert að setja upp framsendingu fyrir. Þessi auknefni verður að birta. Annars virkar framsendingin ekki.
1. Velja skal **Í lagi** til að staðfesta tenginguna.

> [!NOTE]
> Ef þú ert að nota eina villusvörunarsíðu fyrir stöðukóða fyrir báða villuflokka skaltu endurtaka þessa aðferð til að tengja auknefni fyrir hinn villuflokkinn við sömu síðu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Vinna með sniðmát](work-with-templates.md)

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Búa til síðuvefslóð](create-page-url.md)
