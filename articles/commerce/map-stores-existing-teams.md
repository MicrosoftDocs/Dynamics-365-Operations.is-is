---
title: Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams
description: Þessi grein fjallar um hvernig á að kortleggja verslanir og samsvarandi teymi í Dynamics 365 Commerce höfuðstöðvar ef stofnunin þín hefur þegar stofnað teymi í Microsoft Teams fyrir viðskiptasamþættingu.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4cb18affd0df59dc986602a684a3fe3d418644fd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902738"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams

[!include [banner](includes/banner.md)]

Þessi grein fjallar um hvernig á að kortleggja verslanir og samsvarandi teymi í Dynamics 365 Commerce höfuðstöðvar ef stofnunin þín hefur þegar stofnað teymi í Microsoft Teams fyrir viðskiptasamþættingu.

Fyrirtækið gæti stofnað teymi fyrir sumar eða allar verslanirnar áður en Dynamics 365 Commerce og Microsoft Teams er samþætt. Ef svo er þarf að gefa upp vörpun verslana og samsvarandi teymis í Commerce Headquarters til að koma á samstillingu verks milli sölustaðar Commerce og Microsoft Teams.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Varpa verslunum og samsvarandi teymum í Commerce Headquarters 

Til að varpa verslunum og samsvarandi teymum í Commerce Headquarters skal fylgja þessum skrefum.

1. Opnið **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun**.
1. Velja **Flytja út**. 
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Undir **Heiti hóps** skal slá inn „Flytja út Teams vörpun“.
1. Á flýtiflipanum **Valdar einingar** skal velja **Bæta við einingu**. Svarglugginn **Bæta við einingu** birtist.  
1. Í fellilistanum **Heiti einingar** skal velja **Vörpun Teams milli uppruna og teymis**.
1. Í fellilistanum **Markgagnasnið** skal velja **CSV**.
1. Veljið **Bæta við** og síðan **Loka**.
1. Efst til vinstri undir Aðgerðarsvæðinu skal velja **Flytja út núna**.
1. Undir **Vinnslustaða einingar** skal velja **Sækja skrá**.
1. Í útfluttri CSV-skrá skal slá inn gildi fyrir **SOURCETYPE**, **SOURCEID** og **TEAMID** á eftirfarandi hátt:
    - Fyrir **SOURCETYPE** skal slá inn „RetailStore“. 
    - Fyrir **SOURCEID** skal slá inn númer verslunar (til dæmis „000135“ fyrir verslun í San Francisco). Hægt er að finna verslunarnúmer í **Smásala og viðskipti \> Rásir \> Verslanir**.
    - Fyrir **TEAMID** skal slá inn samsvarandi kenni teymis úr Microsoft Teams (til dæmis „5f8bc92b-6aa8-451e-85d1-3949c01ddc6c“). Kenni fyrir upplýsingar teymis má finna á [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Vistið CSV-skrána á staðbundinni vél.
1. Opnið **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun** og veljið síðan **Flytja inn**.
1. Á flýtiflipanum **Valdar einingar** skal velja **Bæta við skrá**. Svarglugginn **Bæta við skrá** birtist.
1. Í fellilistanum **Heiti einingar** skal velja **Vörpun Teams milli uppruna og teymis**.
1. Í fellilistanum **Snið upprunagagna** skal velja **CSV**.
1. Veljið **Hlaða upp og bæta við**, veljið CSV-skrána sem var vistuð áður og veljið síðan **Opna**.
1. Í svarglugganum **Bæta við skrá** skal velja **Loka**.
1. Á aðgerðasvæðinu skal velja **Vista** og síðan **Flytja inn**.

Eftirfarandi myndadæmi sýnir flokkinn **Flytja út vörpun teymis** í Commerce með einingarnar **Bæta við einingu** og útfluttan haus CSV-skráar auðkennd.

![Flytja út vörpun teymis í Commerce með einingarnar Bæta við einingu og útfluttan haus CSV-skráar auðkennd.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Þegar ofangreindum skrefum er lokið skal fylgja skrefunum í [Samstilla verkstjórnun á milli Microsoft Teams og sölustaðar](synchronize-tasks-teams-pos.md) til að samstilla verkstjórnun. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit](commerce-teams-integration.md)

[Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka](enable-teams-integration.md)

[Ákvæði Microsoft Teams frá Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar](synchronize-tasks-teams-pos.md)

[Stjórna notandahlutverkum í Microsoft Teams](manage-user-roles-teams.md)

[Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams](teams-integration-faq.md)
