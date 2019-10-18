---
title: Hvað er nýtt eða breytt í Dynamics 365 Talent (14. mars 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c3beef9ef4e73eaf76f861735bb154fa630703f
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023908"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-14-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 Talent (14. mars 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract
Það eru minniháttar villuleiðréttingar með í þessari útgáfu.

## <a name="changes-in-onboarding"></a>Breytingar á nýliðun
Það eru minniháttar villuleiðréttingar með í þessari útgáfu.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR
**Smíði 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Afkastastjórnun virkar ekki í öllum atburðarásum þegar tvítekin öryggishlutverk eru notuð
Breytingar sem gerðar eru í þessari útgáfu virkja atburðarásir afkastastjórnunar þegar notuð eru út-fyrir-kassann eða tvítekin hlutverk.

### <a name="mass-assign-checklists-to-workers"></a>Magnúthluta gátlistum á starfskrafta
Með þessari breytingu er nú hægt að velja marga starfsmenn og magnúthluta einum eða fleiri gátlistum á þessa starfsmenn. 

### <a name="platform-update-24-for-finance-and-operations"></a>Verkvangsuppfærsla 24 fyrir Finance and Operations
Frekari upplýsingar um verkvangsuppfærslu 24 fyrir Finance and Operations er að finna í [Hvað er nýtt og hvað hefur breyst í Finance and Operations verkvangsuppfærsla 24 (mars 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Verulegar breytingar á verkvangi 24 fela í sér: 

- Viðvaranir eru virkar í Talent.
- Uppfærða yfirlitsstikan er nú samsíða Office-hausnum.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Uppfærsla á staðsetningu skrifstofu færir samhengið efst á starfsmannalistanum
Með núverandi útgáfu mun breytingin á staðsetningu skrifstofu ekki lengur færa samhengið á starfskrafti sem þú ert að skoða þegar staðsetningu skrifstofu er úthlutað.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Lokadagsetning stöðuúthlutunar kemur ekki rétt fram í aðgerðum starfsmannaráðningar og flutnings
Lokadagsetningar stöðuúthlutunar kemur nú rétt fram byggt á æskilegu tímabelti notanda þegar aðgerðirnar eru notaðar.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Starfseiningin Common Data Service leyfir ekki reiti fyrir starfsgerð og starfshlutverk að uppfærast
Common Data Service-einingarnar samstillast nú rétt þegar þær eru uppfærðar með því að nota Common Data Service.

## <a name="coming-soon"></a>Væntanlegt

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Ítarlegt launaöryggi (fast og breytilegt)
Í mörgum fyrirtækjum er hugsanlegt að launa- og fríðindastjórar hafi aðeins aðgang að ákveðnum launafærslum. Þessar færslur gætu verið fyrir stjórnendur eða svæðisbundna starfsmenn. Með þessari breytingu geta mannauðsstjórar haft umsjón með launafyrirkomulaginu fyrir mismunandi starfsmannahópa í fyrirtækinu. Hægt er að úthluta öryggishlutverkum á fastar og breytilegar áætlanir sem ákvarða aðgang að áætlunum og starfsmannaupplýsingum sem tengjast áætlunum, t.d. launa- eða bónusfærslur. Aðeins hlutverk með veittan aðgang geta unnið úr launum fyrir þessa starfsmenn.

###  <a name="email-support-for-alerts"></a>Tölvupóstur út af viðvörunum
Með verkvangsuppfærslu 24 fyrir Finance and Operations geta notendur stofnað viðvörunarreglur sem senda sjálfkrafa tilkynningar í tölvupósti á tengiliði þegar þær ræsast út af tilviki.

### <a name="duplicate-employee-check-interface-changes"></a>Afrita athugun starfsmanns: Viðmót breytist
Með þessari breytingu er borið kennsl á tvítekningar á meðan þú færir inn heiti á reitum og staða sýnir hversu margar fundust. Þú getur valið tengilinn sem gefinn er upp til að opna nýja síðu til að meta hvort nota skuli samsvörun sem borin var kennsl á. Tvítekin skjámynd opnast ekki sjálfkrafa, til að koma í veg fyrir truflandi gagnafærslu.
