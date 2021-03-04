---
title: Fjarlægja tilvik
description: Þessi grein fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a8eac74f0d840251ab56445dd5af4d19d3c0490
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419059"
---
# <a name="remove-an-instance"></a>Fjarlægja tilvik

Þessi grein fer með þig í gegnum ferlið við að fjarlægja prufukeyrslu eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Fjarlægja prufukeyrsluumhverfi

Human Resources prufukeyrslum er úthlutað með 60 daga gildistíma. Hins vegar hafa eigendur prufukeyrsluumhverfa kost á því að ljúka prufuútgáfu snemma með því að ljúka eftirfarandi skrefum. 

1. Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)
2. Veldu **Umhverfi**.
3. Veldu umhverfi prufukeyrslu, sem er með nafngiftarmynstur svipað þessu: Prufukeyrsla - alias@domain
4. Veldu **Eyða** og staðfestu ákvörðunina. 

Núverandi umhverfi prufukeyrslu verður fjarlægt. Þegar það er fjarlægt getur þú skráð þig fyrir nýju prufukeyrsluumhverfi. 

## <a name="remove-a-production-environment"></a>Fjarlægja framleiðsluumhverfi

Þeessi grein gerir ráð fyrir að þú hafir keypt Human Resources í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA). 

Vegna þess að eitt Human Resources umhverfi er innifalið í einu Power Apps umhverfi, eru tveir valkostir sem þarf að hafa í huga. Fyrsti valkosturinn felur í sér að fjarlægja allt Power Apps umhverfið; annar valkosturinn felur í sér að fjarlægja aðeins Human Resources. Fyrsti kosturinn er valinn þegar þú hefur búið til Power Apps umhverfi sérstaklega með það fyrir augum að ráðstafa Human Resources, og þú hefur nýverið hafið framkvæmd eða þú hefur ekki sett af stað neinar samþættingar. Annar kosturinn er viðeigandi þegar þú hefur komið fyrir Power Apps umhverfi sem er útfyllt af ríkulegum gögnum sem eru fengin úr Power Apps og Power Automate.

> [!Important]
> Áður en Power Apps umhverfið er fjarlægt skal tryggja að það sé ekki verið að nota það við samþættingu ríkulegra gagna utan Human Resources sviðsins. Athugaðu einnig að sjálfgefið Power Apps umhverfi er ekki hægt að fjarlægja. 

Til að fjarlægja allt Power Apps umhverfið, þar á meðal Human Resources og tengd forrit og flæði:

1. Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)
2. Veldu **Umhverfi**.
3. Veldu umhverfið sem á að fjarlægja.
4. Veldu **Eyða** og staðfestu ákvörðunina. 
5. Bíddu þar til eyðingunni er lokið.
6. Skráðu þig inn á [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Human Resources. 
7. Veldu Human Resources verkið sem inniheldur umhverfið. 
8. Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn. 
9. Veldu tilvikið sem á að fjarlægja. 
10. Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína.  

Til að fjarlægja Human Resources umhverfi úr núverandi Power Apps umhverfi skaltu ljúka eftirfarandi skrefum. Athugaðu að nauðsyn þess að blanda notendaþjónustu við og hafa samband við hugbúnaðarteymi þróunar og aðgerða (DevOps) fyrir Human Resources er tímabundið þar til þessi eiginleiki er virkjaður beint í LCS.

1. Hafðu samband við Notendaþjónustu til að hefja beiðni um fjarlægingu.
2. Notendaþjónustan mun setja af stað beiðni um fjarlægingu með DevOps teymi fyrir Human Resources. 
3. Haltu áfram eftir að orðsending berst um að umhverfið hafi verið fjarlægt.
4. Skráðu þig inn á LCS með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Human Resources. 
5. Veldu Human Resources verkið sem inniheldur umhverfið. 
6. Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn. 
7. Veldu tilvikið sem þú vilt fjarlægja, sem ætti að vera merkt með uppsetningarstöðuna **Eytt**.
8. Veldu **Fjarlægja tilvika** og staðfestu ákvörðun þína. 

## <a name="recover-a-soft-deleted-environment"></a>Endurheimta umhverfi sem hefur verið fjarlægt úr birtingu

Ef Power Apps-umhverfinu sem umhverfi Human Resources tengist við er eytt, verður staða Human Resources-umhverfisins í Lifecycle Services að **Tekið úr birtingu**. Í slíku tilfelli geta notendur ekki tengst Human Resources.

Til að endurheimta umhverfið:

1. Fylgið leiðbeiningunum í [Endurheimta Power Apps-umhverfið](/power-platform/admin/recover-environment.md).

2. Hafa skal samband við notendaþjónustu til að endurheimta umhverfi Human Resources. Frekari upplýsingar er að finna í [Fá stuðning](hr-admin-troubleshooting-support.md).

> [!Warning]
> Power Apps-umhverfi eru aðeins vistuð í sjö daga frá eyðingu. Nauðsynlegt er að endurheimta umhverfið innan þessara sjö daga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]