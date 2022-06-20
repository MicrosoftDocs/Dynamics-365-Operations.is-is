---
title: Setja upp viðbót smáþjónustu í Lifecycle Services
description: Þessi grein útskýrir hvernig á að setja upp rafræna reikningaviðbótina Microsoft Dynamics Lífsferilsþjónusta (LCS).
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 26f92262eff07ded3e894ee5513dd8dbaa6f94a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849806"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Setja upp viðbót smáþjónustu í Lifecycle Services

[!include [banner](../includes/banner.md)]

Staðfesting í rafrænum reikningaþjónustu krefst þess að þú skráir þitt Microsoft Dynamics 365 Fjármál eða Dynamics 365 Supply Chain Management umhverfi á þjónustuvettvangi með því að setja upp viðbótina fyrir umhverfið þitt í Microsoft Dynamics Lífsferilsþjónusta (LCS).

Til að skrá umhverfi skaltu fylgja þessum skrefum.

1. Skráðu þig inn á LCS-reikninginn þinn.
2. Veldu LCS verkefni á stjórnborði verkefnisins.
2. Í verkinu á stjórnborðinu **Umhverfi** skal velja uppsett umhverfi. Umhverfið sem er valið verður að vera í gangi.
3. Á **Power Platform Samþætting** flipa, í **Umhverfisviðbætur** kafla, veldu **Settu upp nýja viðbót**.
4. Velja **Rafræn reikningsfærsla**.
5. Í reitinn **AAD-forritskenni** skal færa inn **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Gildið er fast. Gakktu úr skugga um að þú slærð aðeins inn alþjóðlegt einstakt auðkenni (GUID). Ekki láta önnur tákn fylgja með, eins og bilum, kommum, punktum eða gæsalappir.
6. Í reitinn **AAD-leigjandakenni** skal færa inn leigjandakenni Azure-áskriftareiknings. The Azure Active Directory (Azure AD) leigjandi sem þú tilgreinir ætti að vera sami leigjandi og notaður er fyrir Regulatory Configuration Service (RCS).
7. Skoðaðu skilmálana og veldu síðan gátreitinn.
8. Velja **Setja upp**. Eftir nokkrar mínútur ætti staðan að breytast úr **Setur upp** í **Uppsett**. Þú gætir þurft að endurnýja síðuna til að sjá þessa breytingu.

Rafræn reikningur er nú tilbúinn til notkunar.

> [!NOTE]
> Fyrirtæki hafa venjulega nokkur fjármála- eða framboðsstjórnunarumhverfi. Þetta umhverfi inniheldur framleiðsluumhverfi, User Acceptance Test (UAT) umhverfi og þróunarumhverfi (sandkassa). Þú verður að ljúka ofangreindu ferli fyrir öll umhverfi sem þú vilt tengja við rafræna reikningagerð.
