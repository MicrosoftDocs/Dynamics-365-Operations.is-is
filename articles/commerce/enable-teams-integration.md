---
title: Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka
description: Þetta efnisatriði lýsir hvernig á að virkja Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 040cac9f3678a0a983d3dd917ae553a5184e4d1e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349449"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að virkja Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.

Til að úthluta Teams með upplýsingum frá Dynamics 365 Commerce og samstilla eiginleika verkstjórnunar milli Teams og forrits sölustaðar, þarf að virkja samþættingareiginleikana í Commerce Headquarters.

> [!NOTE]
> Með því að virkja Teams samþættingu samþykkir notandi að deila gögnum með Teams. Gögnum sem deilt er með Teams gætu verið geymd í öðru landi en gögnin í Commerce og gætu því fallið undir aðrar reglugerðir. Frekari upplýsingar eru í [Öryggismiðstöð Microsoft](https://www.microsoft.com/trust-center). Upplýsingar um persónuverndarstefnur Microsoft er að finna í [Persónuverndaryfirlýsing Microsoft](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Virkja samþættingu Teams

Áður en hægt er að virkja samþættingu Microsoft Teams við Commerce þarf að skrá Teams-forritið með leigjandanum í Azure-gáttinni.

Til að skrá Teams-forritið með leigjandanum í Azure-gáttinni skal fylgja þessum skrefum.

1. Fylgið skrefunum í [Stuttar leiðbeiningar: Skrá forrit á verkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app) til að skrá Teams-forritið með leigjandanum í Azure-gáttinni.
1. Afritið gildið **Forritskenni (biðlarakenni)** af síðunni **Yfirlit** fyrir skráð forrit. Þetta gildi er notað til að virkja Teams samþættingu í Commerce Headquarters.
1. Afritið gildi vottorðs sem slegið var inn þegar [vottorði var bætt við](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) í skrefi 1. Vottorðið er einnig þekkt sem almennur lykill eða forritalykill. Þetta gildi er notað til að virkja Teams samþættingu í Commerce Headquarters.

Fylgja skal eftirfarandi skrefum til að óvirkja Teams samþættingu í Commerce Headquarters.

1. Opnið **Retail og Commerce\> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Stillið **Virkja Microsoft Teams-samþættingu** á **Já**.
1. Í reitina **Forritskenni** og **Forritslykill** skal slá inn gildin sem fengin voru þegar Teams-forritið var skráð í Azure-gáttinni.
1. Í aðgerðarúðunni skal velja **Vista**.

Eftirfarandi mynd sýnir dæmi um skilgreiningar Teams samþættingar í Commerce Headquarters.

![Samþættingarskilgreining Teams í Commerce Headquarters.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Óvirkja samþættingu Teams

Fylgja skal eftirfarandi skrefum til að óvirkja Microsoft Teams samþættingu í Commerce Headquarters.

1. Opnið **Smásala og viðskipti \> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.
1. Á aðgerðarúðunni skal velja **Breyta**.
3. Stillið valkostinn **Virkja Microsoft Teams-samþættingu** á **Nei**.
4. Hreinsið gildin í reitunum **Forritskenni** og **Forritslykill**.
1. Í aðgerðarúðunni skal velja **Vista**.

> [!NOTE]
> Þegar slökkt er á samþættingu Teams við Commerce sýna afgreiðslukassar ekki lengur verk sem Teams-forritið gefur út.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit](commerce-teams-integration.md)

[Ákvæði Microsoft Teams frá Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar](synchronize-tasks-teams-pos.md)

[Stjórna notandahlutverkum í Microsoft Teams](manage-user-roles-teams.md)

[Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams](map-stores-existing-teams.md)

[Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams](teams-integration-faq.md)