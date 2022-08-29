---
title: Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit
description: Þessi grein gefur yfirlit yfir Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 928322c6a391510621bfebbb57d3930f91e69e24
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282904"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit

[!include [banner](includes/banner.md)]

Þessi grein gefur yfirlit yfir Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.

Dynamics 365 Commerce samþættist við Teams til að auðvelda viðskiptavinum og starfsmönnum þeirra að bæta framleiðni með því að samstilla verkstjórnun milli forritanna tveggja. Hnökralaus verkstjórnunin sem samþætting Commerce og Teams býður upp á gerir verslunarstjórum og starfsmönnum kleift að búa til verklista, úthluta verkum á margar verslanir og rekja stöðu verka yfir verslanir úr öðru hvoru forritinu.

Samþætting Commerce og Teams er í boði frá og með Commerce útgáfu 10.0.18.

## <a name="key-features"></a>Lykileiginleikar

Hér eru nokkrir af helstu eiginleikunum sem samþætting Commerce og Microsoft Teams býður upp á:

- Úthluta Teams með því að nýta sér vel skilgreindar upplýsingar frá Commerce, t.d. skipulagseiningar fyrirtækis og upplýsingar um verslanir, starfsmenn, heimildir og yfirsýn viðskipta.
- Samstilla breytingar sem eru í gangi á auðveldan hátt (til dæmis viðbót nýrra verslana eða ráðning nýrra starfsmanna) milli Commerce og Teams, en halda Commerce sem aðaluppruna á skipulagsgögnum fyrirtækisins.
- Samþætta verkstjórnun milli Commerce og Teams til að auðvelda starfsfólki verslunar, verslunarstjórum, svæðisstjórum og samskiptastjórum að sjá um verkstjórnun úr öðru hvoru forritinu.

## <a name="prerequisites-for-using-integration-features"></a>Forsendur fyrir notkun samþættingareiginleika

Eftirfarandi skilyrði verða að vera til staðar áður en hægt er að nota Microsoft Teams samþættingareiginleika:

- Microsoft 365 Business Standard leyfi (Þetta leyfi inniheldur lið.)
- Azure Active Directory (Azure AD ) reikningar fyrir alla stjórnendur og starfsmenn í verslun
- Sölustaðakerfi (POS) sem eru grunnstillt með Azure AD sannvottun

## <a name="conceptual-architecture"></a>Hugmyndahönnun

Eftirfarandi mynd sýnir hugmyndahönnun samþættingar Dynamics 365 Commerce og Microsoft Teams með því að nota verslun í San Francisco sem dæmi. Bæði forritin Teams og Commerce á sölustað nota Microsoft Planner sem gagnageymslu þannig að verk sem gefin eru út í Teams koma til með að birtast í forriti sölustaðar og tilfallandi verkefni sem verslunarstjórar búa til í forriti sölustaðar birtast í Teams, sem leiðir til þægilegrar upplifunar í verkstjórnun á milli forritanna.    

![Hönnun samþættingar Commerce og Teams.](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka](enable-teams-integration.md)

[Úthlutun Microsoft Teams frá Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar](synchronize-tasks-teams-pos.md)

[Stjórna notandahlutverkum í Microsoft Teams](manage-user-roles-teams.md)

[Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams](map-stores-existing-teams.md)

[Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams](teams-integration-faq.md)
