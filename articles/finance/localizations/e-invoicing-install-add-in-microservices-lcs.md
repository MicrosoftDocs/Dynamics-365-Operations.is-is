---
title: Setja upp viðbót smáþjónustu í Lifecycle Services
description: Þessi grein útskýrir hvernig á að setja upp innbót rafrænna reikninga í Microsoft Dynamics Lifecycle Services (LCS).
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 938b00192acc0ff5534239f2f280792471181fad
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710809"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Setja upp viðbót smáþjónustu í Lifecycle Services

[!include [banner](../includes/banner.md)]

Auðkenning í rafrænu reikningsfærsluþjónustunni krefst þess að þú skráir Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management umhverfi þitt á þjónustuverkvanginum með því að setja viðbótina fyrir umhverfi þitt í Microsoft Dynamics Lifecycle Services (LCS).

Til að skrá umhverfi skaltu fylgja þessum skrefum.

1. Skráðu þig inn á LCS-reikninginn þinn.
2. Veljið LCS verkefni á stjórnborði verkefnisins.
2. Í verkinu á stjórnborðinu **Umhverfi** skal velja uppsett umhverfi. Umhverfið sem er valið verður að vera í gangi.
3. Í flipanum **Power Platform Samþætting** í **Innbætur umhverfis** hlutanum skal velja **Setja upp nýja innbót**.
4. Velja **Rafræn reikningsfærsla**.
5. Í reitinn **AAD-forritskenni** skal færa inn fast gildi **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Þetta gildi er alltaf fast. Gakktu úr skugga um að þú sláir aðeins inn alþjóðlegt einkvæmt kennimerki (GUID). Ekki nota önnur tákn eins og bil, kommur, punkta eða tilvitnunarmerki.
6. Í reitinn **AAD-leigjandakenni** skal færa inn leigjandakenni Azure-áskriftareiknings. Leigjandi Azure Active Directory (Azure AD) sem þú tilgreinir á að vera sami leigjandinn og er notaður fyrir Regulatory Configuration Service (RCS).
7. Farið yfir skilmálana og veljið því næst gátreitinn.
8. Velja **Setja upp**. Eftir nokkrar mínútur ætti staðan að breytast úr **Setur upp** í **Uppsett**. Hugsanlega verður að endurhlaða síðuna til að sjá þessar breytingar.

Nú er rafræn reikningagerð tilbúinn til notkunar.

> [!NOTE]
> Fyrirtæki hafa yfirleitt nokkur Finance eða Supply Chain Management umhverfi. Þessi umhverfi eru framleiðsluumhverfi, umhverfi samþykkisprófunar notanda (UAT) og umhverfi þróunar (sandkassi). Þú verður að ljúka undanfarandi ferli fyrir öll umhverfi sem eiga að tengjast rafrænum reikningum.
