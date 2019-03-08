---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (14. desember 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7d2866923efd7f115ad5290f35ed4fcac5e47573
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304768"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a>Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (14. desember 2018)

[!include [banner](includes/banner.md)]

**Smíði 8.1.2085**

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.

## <a name="changes"></a>Breytingar

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>US - ACA (Affordable Care Act) stuðningur fyrir skattár 2018 eyðublöð 1095-B og 1095-C

Á hverju ári skulu Viðeigandi stórir vinnuveitendur (ALE) veita öllum starfsmönnum í fullu starfi 1095-C. Að auki, ef vinnuveitandinn veitir sjálfsábyrgðartryggingu skal hann útvega 1095-C (ef hann er ALE) og 1095-B (ef hann er lítill vinnuveitandi) til allra starfsmanna, í fullu starfi eða hlutastarfi, sem falla undir eina af sjúkratryggingum þeirra sem boðið er upp á. Þessi eiginleiki veitir prenthæf eyðublöð fyrir bæði 1095-C og 1095-B.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>Við innflutning er reiturinn SubmittedByPersonId í HcmPerfJournalEntity hunsaður

Við innflutning/útflutning á færslum frammistöðubókar er reiturinn **Sent inn af** hunsaður. Með þessari breytingu endurspeglar gildið **innflutt/útflutt** gildið í töflunni við útflutninginn, við innflutning verður kerfið uppfært með gildinu sem gefið er upp í innflutningsskránni.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Greiningarflipi á vinnusvæðinu „Leyfi og fjarvistir“ sýnir villuna „OpenConnectionError“ fyrir hlutverk sem heyrir ekki undir kerfisstjóra

Með þessari uppfærslu verða engar villur sendar þegar flipinn **Greiningar** er opnaður á vinnusvæðinu **Leyfi og fjarvistir**.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Sjálfsafgreiðsla starfsmanns, köfun niður í stöðustigveldi úr reit mistekst að sækja yfirhnút

Breyting hefur verið gerð til að leiðrétta villuna „Mistókst að sækja yfirhnútinn“ þegar stöðustigveldið hefur verið sérsniðið til að birtast á fyrirliggjandi vinnusvæði og staða er valin í stigveldinu.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Verður að vera kerfisstjóri til að sjá launaflipa á stöðusíðunni

Breyting hefur verið gerð til að hafa með réttar öryggiseiningar í fyrirliggjandi réttindum: „Vinna með upplýsingar um laun starfsmanns og stöðu“. Með þessari breytingu hefur launastjórinn sjálfgefið aðgang að launasvæðum á stöðusíðunni.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Villa þegar frammistöðumat var sent inn til yfirmanns og staðgengillinn %Reviews.PerfPeriod% er notaður í sendingarleiðbeiningum

Breyting hefur verið gerð sem leiðréttir villuna „Núlltilvísun“ þegar staðgengillinn %Reviews.PerfPeriod% er notaður í sendingarleiðbeiningum.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Skýrsla um vinnuafl Power BI sýnir villu þegar starfsaldursdagsetning starfskrafts er hlaupadagur

Með þessari breytingu eru hlaupadagar studdir í Power BI.

### <a name="integration-between-core-hr-and-attract"></a>Samþætting milli Core HR og Attract

Breyting hefur verið gerð til að uppfæra samþættingu milli Core HR og Attract sem tengist umsækjendum sem á að ráða. Til að umsækjendur sem á að ráða séu sýnilegir á vinnusvæðinu **Starfsmannastjórnun** eru eftirfarandi einingar CDS fyrir forrit (CDS 2.0) notaðar:

Starfsumsókn
- Ástæða stöðu verður að vera stillt á Tilboð samþykkt
-   Sýnir umsækjanda og laust starf

Umsækjandi
-   Sýnir upplýsingar um umsækjanda

Laust starf
-   Sýnir auðkenni fyrir laust starf og þátttakendur lausa starfsins

Þátttakendur lausa starfsins
-   Sýnir mannauðsstjóra

Þegar umsækjanda er bætt við starfsmannastjórnun getur hann nú einnig verið vísað frá með því að nota nýjan valkost sem er tiltækur á spjaldi umsækjanda.

## <a name="coming-soon"></a>Væntanlegt

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Leyfi og fjarvistir: Stöður á leyfi fram í tímann og spár um leyfi

Með breytinginum sem eru gerðar til að leyfa starfsmönnum að spá fyrir um frítíma og framtíðaróskum um frítíma án þess að það hafi áhrif á núgildandi stöður frítíma, hvernig stöður frítíma eru birtar er einnig að breytast. 

Tiltæk staða sem er sýnd eins og er er upphæð frítíma sem er í boði fyrir beiðnir, þ.m.t. uppsafnanir til og með deginum í dag og allar samþykktar leyfisbeiðnir fram til lok tímabils. 

Þegar getan til að spá fyrir er gefin út, breytist staðan sem sýnd er í núgildandi stöðu frítíma ásamt uppsöfnunum og beiðnum til og með deginum í dag. Starfsmenn og yfirmenn sjá þessar uppfærðu stöður í sjálfsafgreiðslu starfsmanna og yfirmanna í spjaldinu **Frítími** og í glugganum **Stöður frítíma**. Mannauðsstjórar munu sjá þessar uppfærðu stöður á vinnusvæðinu **Fólk** og glugganum **Úthlutaðar leyfisáætlanir** fyrir starfsmenn.

## <a name="known-issue"></a>Þekkt vandamál

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a>Vörpunarvillur í samþættingu við Finance and Operations

Eftirfarandi vandamál hafa verið greind í núgildandi sniðmáti fyrir samþættingu Talent við Dynamics 365 for Finance and Operations. Nýtt sniðmát verður birt fljótlega og verður notað fyrir öll ný samþættingarverk sem eru búin til. Hægt er að uppfæra vörpunarverkin fyrir núverandi samþættingarverk. Frekari upplýsingar um uppfærðar varpanir eru í eftirfarandi töflu. 

>[!NOTE]
> Úthlutunarverk á stöðum starfa til staða yfirstarfa samþættir ekki gögn. Þetta er mál sem verið er að rannsaka. Það er engin hjáleið í núverandi vörpun. 

Verk deilda til rekstrareiningar þarf eftirfarandi varpanir uppfærðar.

| Fyrirliggjandi upprunasvæði          | Nýtt upprunasvæði |
| -------------------------------|------------------|
| cdm_description (lýsing)  | cdm_name (heiti)  |

Einnig þarf að bæta við aukalegri vörpun. Veldu síðasta **Ekkert** svæðið til að bæta við eftirfarandi vörpun.

| Upprunasvæði                   | Áfangasvæði    |
| -------------------------------|----------------------|
| cdm_description (lýsing)  | NAMEALIAS (NAMEALIAS)|

Uppfærðu varpanirnar ættu að líta út eins og eftirfarandi mynd.

![Deildir til rekstrareiningar verk](./media/DepartmentMapping.png)


Verkið störf til upplýsingar um starf þarf eftirfarandi varpanir uppfærðar.

| Fyrirliggjandi upprunasvæði          | Nýtt upprunasvæði                   |
| -------------------------------|------------------------------------|
| cdm_name (heiti)                | cdm_description (lýsing)      |
| cdm_name (lýsing)         | cdm_jobdescription (starfslýsing)|


Uppfærðu varpanirnar ættu að líta út eins og myndin hér að neðan.

![Störf til upplýsinga um starf verk](./media/JobMapping.png)

Starfskraftar til vinnu verk þarf eftirfarandi varpanir uppfærðar.

| Fyrirliggjandi upprunasvæði                 | Nýtt upprunasvæði                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (netfang 1)   | cdm_primaryemailaddress (aðalnetfang |
| cdm_telephone1 (símanúmer 1)          | cdm_primarytelephone (aðalsímanúmer)       |

Umbreyting á svæði kyns þarf einnig að uppfæra. Veldu **fn** (virkni) vörpunargerð fyrir Kyn og uppfærðu eftirfarandi vörpunargildi.

| CDS-gildi                   | Gildi Finance and Operations                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Karl                                             |
| 75440001                    | Kona                                           |
| 75440002                    | Enginn                                             | 
| 75440003                    | Ótilgreint                                      |

Uppfærðu varpanirnar ættu að líta út eins og eftirfarandi myndir.

![Starfskraftar til starfskrafts verk](./media/WorkerMapping.png)

![Umbreyting á svæði kyns](./media/WorkerTransform.png)
