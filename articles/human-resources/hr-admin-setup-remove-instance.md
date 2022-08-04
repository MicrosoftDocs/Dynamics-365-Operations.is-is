---
title: Fjarlægja tilvik
description: Þessi grein lýsir ferlinu við að fjarlægja reynsluakstur eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178473"
---
# <a name="remove-an-instance"></a>Fjarlægja tilvik

_**Á við um:** Mannauður á sjálfstæðum innviðum_ 

> [!NOTE]
> Frá og með júlí 2022 er ekki hægt að útvega nýtt mannauðsumhverfi á sjálfstæðum mannauðsinnviðum og nýjum Microsoft Dynamics Ekki er hægt að búa til verkefni um líftímaþjónustu (LCS). Viðskiptavinir geta innleitt mannauðsumhverfi á fjármála- og rekstrarinnviðum. Fyrir frekari upplýsingar, sjá [Veiting mannauðs í innviðum fjármála og rekstrar](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Fjármála- og rekstrarforritið styður eyðingu umhverfi. Fyrir frekari upplýsingar um hvernig á að eyða umhverfi, sjá [Eyða umhverfi](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

Þessi grein útskýrir ferlið við að fjarlægja reynsluakstur eða framleiðsluumhverfi fyrir Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Fjarlægja prufukeyrsluumhverfi

Human Resources prufukeyrslum er úthlutað með 60 daga gildistíma. Hins vegar hafa eigendur prufukeyrsluumhverfa kost á því að ljúka prufuútgáfu snemma með því að ljúka eftirfarandi skrefum. 

1. Fara í [Power Apps Stjórnendamiðstöð](https://admin.businessplatform.microsoft.com/)
2. Veldu **Umhverfi**.
3. Veldu umhverfi prufukeyrslu, sem er með nafngiftarmynstur svipað þessu: Prufukeyrsla - alias@domain
4. Veldu **Eyða** og staðfestu ákvörðunina. 

Núverandi umhverfi prufukeyrslu verður fjarlægt. Þegar það er fjarlægt getur þú skráð þig fyrir nýju prufukeyrsluumhverfi. 

## <a name="remove-a-production-environment"></a>Fjarlægja framleiðsluumhverfi

Þeessi grein gerir ráð fyrir að þú hafir keypt Human Resources í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA). 

Vegna þess að eitt mannauðsumhverfi er að finna í einu Power Apps umhverfi, það eru tveir valkostir sem þarf að hafa í huga þegar þú fjarlægir umhverfi: 
- **Fjarlægðu allt Power Apps umhverfi.** Þessi valkostur er valinn þegar Power Apps umhverfi var búið til í þeim tilgangi að útvega mannauð, innleiðing er nýhafin eða þú ert ekki með neinar staðfestar samþættingar.  
- **Fjarlægðu aðeins mannauð.** Þessi valkostur er viðeigandi þegar það er staðfest Power Apps umhverfi sem er fyllt með gögnum sem eru notuð í Microsoft Power Apps og Power Automate.


> [!Important]
> Áður en þú fjarlægir Power Apps umhverfi, tryggja að það sé ekki notað fyrir gagnasamþættingu utan sviðs mannauðs. Athugaðu einnig að sjálfgefið Power Apps umhverfi er ekki hægt að fjarlægja. 

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

Ef þú eyðir Power Apps umhverfi sem mannauðsumhverfið þitt er tengt við, verður staða mannauðsumhverfisins í LCS **Soft eytt**. Í slíku tilfelli geta notendur ekki tengst Human Resources.

Til að endurheimta umhverfið:

1. Fylgið leiðbeiningunum í [Endurheimta Power Apps-umhverfið](/power-platform/admin/recover-environment).

2. Hafa skal samband við notendaþjónustu til að endurheimta umhverfi Human Resources. Frekari upplýsingar er að finna í [Fá stuðning](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Apps-umhverfi eru aðeins vistuð í sjö daga frá eyðingu. Þú verður að endurheimta umhverfið innan sjö daga tímabilsins.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
