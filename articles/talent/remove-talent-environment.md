---
title: Fjarlægja Talent-umhverfi
description: Þetta efnisatriði fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 904c8eb1254a65e1627c33f14488a1a8e12f7c2b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518277"
---
# <a name="remove-talent-environments"></a>Fjarlægja Talent-umhverfi

[!include [banner](includes/banner.md)]

Þetta efnisatriði fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 for Talent.

## <a name="removing-a-test-drive-environment"></a>Að fjarlægja prufukeyrsluumhverfi

Talent prufukeyrslum er úthlutað með 60 daga gildistíma. Hins vegar hafa eigendur prufukeyrsluumhverfa kost á því að ljúka prufuútgáfu snemma með því að ljúka eftirfarandi skrefum. 

1. Farðu í [Stjórnendamiðstöð PowerApps](https://admin.businessplatform.microsoft.com/).
2. Veldu **Umhverfi**.
3. Veldu umhverfi prufukeyrslu, sem er með nafngiftarmynstur svipað þessu: Prufukeyrsla - alias@domain
4. Veldu **Eyða** og staðfestu ákvörðunina. 

Núverandi umhverfi prufukeyrslu verður fjarlægt. Þegar það er fjarlægt getur þú skráð þig fyrir nýju prufukeyrsluumhverfi. 

## <a name="removing-a-production-environment"></a>Að fjarlægja framleiðsluumhverfi

Þetta efnisatriði gerir ráð fyrir að þú hafir keypt Talent í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA). 

Vegna þess að eitt Talent umhverfi er „innifalið“ í einu PowerApps umhverfi, eru tveir valkostir sem þarf að hafa í huga. Fyrsti valkosturinn felur í sér að fjarlægja allt PowerApps umhverfið; annar valkosturinn felur í sér að fjarlægja aðeins Talent. Fyrsti kosturinn er valinn þegar þú hefur búið til PowerApps umhverfi sérstaklega með það fyrir augum að ráðstafa Talent, og þú hefur nýverið hafið framkvæmd eða þú hefur ekki sett af stað neinar samþættingar. Annar kosturinn er viðeigandi þegar þú hefur komið fyrir PowerApps umhverfi sem er útfyllt af ríkulegum gögnum sem eru fengin úr PowerApps og Flows.

> [!Important]
> Áður en PowerApps umhverfið er fjarlægt skal tryggja að það sé ekki verið að nota það við samþættingu ríkulegra gagna utan Talent sviðsins. Athugaðu einnig að sjálfgefið PowerApps umhverfi er ekki hægt að fjarlægja. 

Til að fjarlægja allt PowerApps umhverfið, þar á meðal Talent og tengd forrit og Flows:

1. Farðu í [Stjórnendamiðstöð PowerApps](https://admin.businessplatform.microsoft.com/).
2. Veldu **Umhverfi**.
3. Veldu umhverfið sem á að fjarlægja.
4. Veldu **Eyða** og staðfestu ákvörðunina. 
5. Bíddu þar til eyðingunni er lokið.
6. Skráðu þig inn á [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent. 
7. Veldu Talent verkið sem inniheldur umhverfið. 
8. Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn. 
9. Veldu tilvikið sem á að fjarlægja. 
10. Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.  

Til að fjarlægja Talent umhverfi úr núverandi PowerApps umhverfi skaltu ljúka eftirfarandi skrefum. Athugaðu að nauðsyn þess að blanda notendaþjónustu við og hafa samband við hugbúnaðarteymi þróunar og aðgerða (DevOps) fyrir Talent er tímabundið þar til þessi eiginleiki er virkjaður beint í LCS.

1. Hafðu samband við Notendaþjónustu til að hefja beiðni um fjarlægingu.
2. Notendaþjónustan mun setja af stað beiðni um fjarlægingu með DevOps teymi fyrir Talent. 
3. Haltu áfram eftir að orðsending berst um að umhverfið hafi verið fjarlægt.
4.  Skráðu þig inn í LCS með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent. 
5. Veldu Talent verkið sem inniheldur umhverfið. 
6. Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn. 
7. Veldu tilvikið sem þú vilt fjarlægja, sem ætti að vera merkt með uppsetningarstöðuna **Mistókst**.
8. Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína. 

