---
title: Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar
description: Þetta efnisatriði lýsir því hvernig á að samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar (POS).
author: gvrmohanreddy
ms.date: 02/17/2021
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
ms.openlocfilehash: c07ca28b45335de5e327305b7426d1b6de8ce5c7
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323498"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar (POS).

Einn megintilgangur samþættingar Teams er að gera kleift að samstilla verkstjórnun milli forrits sölustaðar og Teams. Þannig geta starfsmenn verslunar notað annaðhvort forrit sölustaðar eða Teams til að stjórna verkum og þurfa ekki að skipta á milli forrita.

Þar sem Planner er notað sem gagnageymsla fyrir verk í Teams, þarf að vera tengill milli Teams og Dynamics 365 Commerce. Þessi tengill er settur á með því að nota tiltekið áætlunarkenni fyrir tiltekið teymi verslunar.

Eftirfarandi ferli sýna hvernig á að setja upp samstillingu verkstjórnunar á milli forrita sölustaðar og Teams.

## <a name="publish-a-test-task-list-in-teams"></a>Birta lista yfir prufuverk í Teams

Eftirfarandi ferli gerir ráð fyrir því að teymi verslunar séu að nota Microsoft Teams samþættingu verkstjórnunar við Commerce í fyrsta skipti.

Fylgið þessum skrefum til að birta prófunarverk í Teams.

1. Skráðu þig inn á Teams sem samskiptastjóra. Yfirleitt eru samskiptastjórar notendur sem gegna hlutverki **Svæðisstjóra** í Commerce.
1. Á yfirlitssvæðinu vinstra megin skal velja **Verk eftir Planner**.
1. Í flipanum **Útgefnir listar** skal velja **Nýr listi** niðri vinstra megin og gefa nýja listanum heitið **Prufuverklisti**.
1. Velja **Stofna**. Nýi Listinn birtist undir **Drög**.
1. Undir **Verktitill** skal gefa fyrsta verkinu titilinn **Teams-samþætting prófuð**. Veljið síðan **Færa inn**.
1. Á listanum **Drög** skal velja verklistann. Veljið síðan  **Birta**  efst í hægra horninu.
1. Í svarglugganum **Velja hverjum á að birta** skal velja teymin sem eiga að taka á móti prufuverklista.
1. Veljið **Næst** til að fara yfir birtingaráætlunina. Ef gera þarf breytingar skal velja  **Til baka**. 
1. Veljið **Staðfestið til að halda áfram** og veljið því næst **Birta**.
1. Að birtingu lokinni gefa skilaboð efst í flipanum **Útgefnir listar** til kynna hvort tekist hafi að afhenta verklistann.

Frekari upplýsingar er að finna í [Birta verklista til að stofna og fylgjast með vinnu í fyrirtækinu](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

## <a name="link-pos-and-teams-for-task-management"></a>Tengja sölustaði og Teams fyrir verkefnastjórnun

Til að tengja forrit sölustaðar og Microsoft Teams fyrir verkstjórnun í Commerce Headquarters skal fylgja þessum skrefum.

> [!NOTE]
> Áður en þú reynir að samþætta Verkefnastjórnun við Microsoft Teams, vertu viss um að þú hafir virkjað [Dynamics 365 Commerce og Microsoft Teams sameining](enable-teams-integration.md). 

1. Farið í **Retail og Commerce \> Verkstjórnun \> Samþætting verka við Microsoft Teams**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Stillið **Virkja samþættingu verkstjórnunar** á **Já**.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á aðgerðasvæðinu skal velja **Setja upp verkstjórnun**. Þú ættir að fá tilkynningu sem sýnir að verið sé að búa til runuvinnslu sem kallast **Úthlutun Teams**.
1. Farið í **Kerfisstjórnun \> Fyrirspurnir \> Runuvinnslur** og finnið nýlegustu vinnuna sem er með lýsinguna **Úthlutun Teams**. Bíðið þar til verkið hefur verið keyrt.
1. Keyrið **CDX job 1070** til að birta auðkenni áætlunarinnar og tilvísanir í verslunar til Retail Server.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit](commerce-teams-integration.md)

[Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka](enable-teams-integration.md)

[Ákvæði Microsoft Teams frá Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Stjórna notandahlutverkum í Microsoft Teams](manage-user-roles-teams.md)

[Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams](map-stores-existing-teams.md)

[Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams](teams-integration-faq.md)
