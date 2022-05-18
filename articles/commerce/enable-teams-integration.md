---
title: Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka
description: Þetta efnisatriði lýsir hvernig á að virkja Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dfada577ab97fdb9912c22d2399529f934b25d54
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695735"
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
1. Á **App Skráning** flipanum, veldu forritið sem þú bjóst til í fyrra skrefi. Síðan, á **Auðkenning** flipa, veldu **Bættu við vettvangi**.
1. Veldu í glugganum **Vefur**. Þá, í **Tilvísunarslóðir** reit, sláðu inn vefslóð á sniðinu **\<HQUrl\> /oauth**. Skipta um **\<HQUrl\>** með slóð höfuðstöðva viðskipta (til dæmis,`https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Á **Yfirlit** síðu skráða appsins, afritaðu **Auðkenni umsóknar (viðskiptavinar).** gildi. Þú verður að gefa upp þetta gildi til að virkja Teams samþættingu í höfuðstöðvum Commerce í næsta hluta.
1. Fylgdu leiðbeiningunum í [Bættu við leyndarmáli viðskiptavinar](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) til að bæta við leyndarmáli viðskiptavinar. Afritaðu síðan **Leynilegt gildi** gildi fyrir viðskiptavininn. Þú verður að gefa upp þetta gildi til að virkja Teams samþættingu í höfuðstöðvum Commerce í næsta hluta.
1. Veldu **API heimildir**, og veldu síðan **Bættu við heimild**.
1. Í **Biðja um API heimildir** valmynd, veldu **Microsoft graf**, veldu **Úthlutaðar heimildir**, stækka **Hópur**, veldu **Group.ReadWrite.All**, og veldu síðan **Bæta við heimildum**.
1. Í **Biðja um API heimildir** valmynd, veldu **Bættu við heimild**, veldu **Microsoft graf**, veldu **Umsóknarheimildir**, stækka **Hópur**, veldu **Group.ReadWrite.All**, og veldu síðan **Bæta við heimildum**.
1. Í **Biðja um API heimildir** valmynd, veldu **Bættu við heimild**. Á **API sem stofnunin mín notar** flipi, leitaðu að **Microsoft Teams Smásöluþjónusta**, og veldu það.
1. Veldu **Úthlutaðar heimildir**, stækka **TaskPublishing**, veldu **TaskPublising.ReadWrite.All**, og veldu síðan **Bæta við heimildum**. Fyrir frekari upplýsingar, sjá [Stilltu biðlaraforrit til að fá aðgang að vef-API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Fylgja skal eftirfarandi skrefum til að óvirkja Teams samþættingu í Commerce Headquarters.

1. Opnið **Retail og Commerce\> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Stillið **Virkja Microsoft Teams-samþættingu** á **Já**.
1. Í **Auðkenni umsóknar** reit, sláðu inn **Auðkenni umsóknar (viðskiptavinar).** gildi sem þú fékkst á meðan þú skráðir Teams forritið í Azure gáttinni.
1. Í **Umsóknarlykill** reit, sláðu inn **Leynilegt gildi** gildi sem þú fékkst á meðan þú bættir við leyndarmáli viðskiptavinar í Azure gáttinni.
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
