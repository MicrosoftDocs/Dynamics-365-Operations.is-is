---
title: Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams
description: Þessi grein veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce og Microsoft Teams sameining.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 79e8c6899d84c3d6147c0a0c2834a7ad2f7b6927
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292055"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams

[!include [banner](includes/banner.md)]

Þessi grein veitir svör við algengum spurningum um Microsoft Dynamics 365 Commerce og Microsoft Teams sameining.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Hver í verslun verður eigandi teymis við úthlutun Teams úr Commerce? 

Öllum verslunarstjórum er sjálfkrafa bætt við sem eigendum í samsvarandi teymishóp þannig að þeir geti framkvæmt aðgerðir eins og að bæta við einkarás og bæta við eða eyða meðlimum. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Hvernig úthluta ég starfsmanni hlutverki „samskiptastjóra“ í Commerce Headquarters? 

Samskiptastjórar í Microsoft Teams hafa getu til að búa til og birta verkefnalista. Starfsmenn fyrirtækis sem þurfa að gerast samskiptastjórar verða að hafa fengið úthlutað hlutverkinu „stjórnandi smásöluverks“ í Commerce Headquarters.

Fylgið þessum skrefum til að úthluta hlutverki stjórnanda smásölu á starfsmann í Commerce Headquarters.

1. Farðu í **Retail og Commerce \> Starfsmenn \> Notendur**.
1. Velja starfsmann.
1. Á flýtiflipanum **Hlutverk notanda** velurðu **Úthluta hlutverkum**.
1. Í valmyndinni **Úthluta hlutverkum til notanda** velurðu hlutverkið **Stjórnandi smásöluverks** og velur síðan **Í lagi**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Hvernig býð ég upp á upphleðslu á ákveðnu fyrirtækjastigveldi í Microsoft Teams?

Í Commerce Headquarters tengist sérhvert stigveldi fyrirtækis að minnsta kosti einum tilgangi. Gangið úr skugga um að stigveldið sem ætlunin er að úthluta í Microsoft Teams hafi tilganginn **Skýrslugerð smásölu** tengdan við eins og sýnt er í eftirfarandi myndadæmi. 

![Dæmi um tilgang fyrirtækjastigveldis í Commerce Headquarters.](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Hvernig geri ég starfsmönnum smásöluverslunar kleift að skrá sig inn á sölustað Commerce með Azure Active Directory (Azure AD)?

Upplýsingar um hvernig á að skilgreina innskráningarupplifun sölustaðar Commerce til að nota Azure AD sannvotun er að finna í [Virkja Azure Active Directory sannvottun fyrir POS innskráningu](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Hvernig varpa ég verslunum og samsvarandi teymum í Commerce Headquarters ef fyrirtækið mitt hefur þegar stofnað teymi í Microsoft Teams?

Upplýsingar um hvernig á að varpa verslunum og teymum ef fyrirliggjandi teymi eru til staðar er að finna í [Varpa verslunum og samsvarandi teymum ef fyrirtækið þitt er með fyrirliggjandi teymi í Microsoft Teams](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Hvernig hreinsa ég lykil Microsoft Graph API sem geymdur er í lotugeymslu?

Notandi sem hefur skráð sig inn á sölustað með Azure Active Directory (Azure AD) reikningi ætti að skrá sig út af sölustað eða loka forritinu til að hreinsa lotugeymsluna. 

> [!TIP]
> Mælt er með að starfsmenn verslunar venji sig á að læsa alltaf afgreiðslukassanum eða skrái sig út úr lotu þegar þeir eru ekki að nota afgreiðslukassann. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Hvað gerist ef verslun er ekki með verslunarstjóra?

Ef verslun er ekki með stjórnendur verður teymishópur ekki stofnaður fyrri verslunina eða í Teams. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Hvað gerist ef verslunarstjóri yfirgefur fyrirtækið?

Allir sem eru með hlutverk eiganda geta bætt við nýjum verslunarstjóra í Commerce Headquarters og endurúthlutað Teams þannig að nýi stjórnandinn fái nauðsynleg réttindi í Teams fyrir hópinn. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit](commerce-teams-integration.md)

[Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka](enable-teams-integration.md)

[Ákvæði Microsoft Teams frá Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar](synchronize-tasks-teams-pos.md)

[Stjórna notandahlutverkum í Microsoft Teams](manage-user-roles-teams.md)

[Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams](map-stores-existing-teams.md)
