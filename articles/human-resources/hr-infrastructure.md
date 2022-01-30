---
title: Dynamics 365 Human Resources sameining innviða - Útgáfa 10.0.25 uppfærsla
description: Þetta efni veitir upplýsingar um Microsoft Dynamics 365 Human Resources útgáfu 10.0.25, sem færir fyrstu bylgju getu í innviðasamruna.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b785248c31c2cc4feb5cedd77264f36bfe927e0e
ms.sourcegitcommit: 10b85a09e8a550155a69aa2a8877a7c88b887242
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/20/2022
ms.locfileid: "8014491"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources sameining innviða - Útgáfa 10.0.25 uppfærsla

Útgáfan 10.0.25 kemur með fyrstu bylgju getu í samruna innviða. Við samruna innviða, Microsoft Dynamics 365 Human Resources verður sameinað innviðum Fjármála- og rekstrarsviðs. Hins vegar verður það áfram leyfilegt sem sjálfstæð umsókn, eins og Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Fyrir frekari upplýsingar um innviðasamruna, sjá [Dynamics 365 Human Resources Algengar spurningar um sameiningu innviða](../human-resources/hr-infrastructure-merge-faq.md).

Sameiningin mun veita mannauðsnotendum samræmi á eftirfarandi hátt:

- [Umhverfisstjórnun og samþættingar eru í samræmi milli mannauðs- og fjármála- og rekstrarappa.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Stjórna umhverfi í Microsoft Dynamics Lifecycle Services, málefnaleit og Regression Suite Automation Tool.
    - Það er einn kóðagrunnur, þar sem ný virkni fyrir mannauð er gefin út sem hluti af venjulegu One Version uppfærsluferli.
    - Leiðin sem uppfærslur, uppfærslur og flýtileiðréttingar eru notaðar á umhverfi er í samræmi.

- [Stækkanleikavalkostir eru bættir.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Þú getur haldið áfram að nota Microsoft Power Platform verkfæri til að lengja eftir þörfum.
    - Þú getur aukið virkni með eyðublöðum, töflum, aðferðum og forritunarviðmóti (API).
    - Þú getur búið til og framlengt einingar.

    Fyrir frekari upplýsingar um framlengingarvalkostina sem eru í boði, sjá [Yfirlit yfir stækkanleika í Dynamics 365](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Búðu til eitt sett af mannauðsmöguleikum í Dynamics 365.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    Í útgáfunni 10.0.25 hefur hagnýtur möguleiki sem aðeins var til í Human Resources verið aðgengilegur á Finance and Operations innviði. Til þess að viðskiptavinir geti nýtt sér þessa möguleika í fjármála- og rekstrarumhverfi verður að virkja eftirfarandi mannauðseiginleika í eiginleikastjórnun.

    | Heiti eiginleika | Yfirlit | Losunarstaða | 
    |--------------|----------|----------------| 
    | Útreikningur starfsaldurs | Uppsetningarvalkostur gerir þér kleift að velja dagsetninguna sem er notuð fyrir **Margra ára þjónustu** útreikning. | Almennt tiltækt | 
    | Endurbætur á upplifun verkflæðis | Þessi eiginleiki veitir aukna notendaupplifun fyrir innsendingar á verkflæði og samþykki. | Almennt tiltækt | 
    | Prenta umsagnir um frammistöðu | Þú getur prentað árangursdóma á PDF formi. | Almennt tiltækt | 
    | Sérsniðnir tenglar inn **Sjálfsafgreiðslustjóri** | Þú getur búið til sérsniðna tengla sem birtast í **Tengdir tenglar** kafla af **Sjálfsafgreiðslustjóri**. | Almennt tiltækt | 
    | Launayfirlit þvert á fyrirtæki | Notendur geta skoðað bótaáætlanir í **Sjálfsafgreiðslustjóri** yfir alla lögaðila, án þess að þurfa að skipta um fyrirtæki. | Almennt tiltækt | 
    | Stilltu mörg launastig eftir starfi\*&dagger; | Störf styðja nú mörg launastig. | Almennt tiltækt | 
    | Verkefnastjórnun\* | Þú getur búið til gátlista og verkefni fyrir um borð, brottför og umskipti. | Forútgáfa | 
    | Straumlínulöguð starfsmannafærsla | Þessi eiginleiki veitir uppfærða notendaupplifun á núverandi **Vinnumaður** síðu. | Forútgáfa | 
    | Endurbætur á upplifun notanda í mannauði | Sjá töflu í næsta kafla.  | Forútgáfa | 

\* Það verður að kveikja á þessum eiginleika áður en **Upplifun mannauðs notenda** eiginleiki.

&dagger; Ekki er hægt að slökkva á þessum eiginleika eftir að hann hefur verið virkjaður.

## <a name="human-resource-user-experience-enhancements"></a>Upplifun mannauðs notenda

| Heiti eiginleika | Yfirlit | 
|--------------|----------| 
| Ítarlegri aðgangur | Aðgangur að starfsmönnum er takmarkaður miðað við lögaðila. | 
| Eyða ráðningu | Hægt er að eyða ráðningu starfsmanns. | 
| Vinnufjölskyldur | Þú getur fylgst með hópi starfa sem fela í sér svipaða vinnu og krefjast svipaðrar þjálfunar, færni, þekkingar og sérfræðiþekkingar. | 
| Fleiri atvinnusvið | Eftirfarandi reitum var bætt við: **Atvinnuflokkur**, **atvinnu**, og **Atvinnustaða**. | 
| **Starfsmenn án atvinnu** síðu | Síða sýnir lista yfir starfsmenn sem ekki hafa starfsskrá. | 
| Uppfærsla notendaupplifunar á stöðuvídd | Það er aukin notendaupplifun til að úthluta stöðuvíddum fyrir hvern lögaðila. | 
| Heimilisfangsbreytingar í **Starfsmannastjórnun** vinnurými | Þessi eiginleiki gefur upp talningu á öllum heimilisfangsbreytingum sem áttu sér stað á tilteknum fjölda daga, eins og skilgreint er á **Stærðir mannauðs** síðu. | 
| Skrár að renna út í **Starfsmannastjórnun** vinnurými | Þessi eiginleiki veitir lista yfir hluti sem eru útrunnir eða munu renna út fyrir skírteini, auðkenni, skilorð, skimun eða próf. | 
| **Staðfesting stigveldis** síðu | Athugun er gerð fyrir hringlaga tilvísanir í stigveldi stöðulínu. | 
| Landssértækar launaupplýsingar | Fleiri launareitir eru fáanlegir á **Atvinna verkamanna** síðu, allt eftir landi eða svæði lögaðilans þar sem starfsmenn eru starfandi. | 
| Endurbætur á reglufylgni | Viðbótartilkynningarmöguleikar eru í boði fyrir EEO-1, Vets 4212 og OSHA300a. | 
| Uppfærslur á **Starfsmannastjórnun** vinnurými | Uppfærslur hafa verið gerðar til að fylgjast með breytingum á heimilisfangi og skrám sem renna út. Að auki birta nýir flipar starfsmanns- og stöðuaðgerðir. | 
