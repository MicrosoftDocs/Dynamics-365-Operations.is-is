---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (25. júní 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 23. júní 2020.
author: andreabichsel
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 228883dd4af3f4f51c53524813c1852d392c1d29
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053948"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (23. júní 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3347. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Þegar skráning rennur út fyrir starfsmann er leyfisgerðin, staðan og upphæðin öll hreinsuð í skjámynd leyfisskráningar (444867)

Gildunum í **Leyfisgerð**, **Staða** og **Upphæð** er nú haldið við í stað þess að hreinsa þau þegar þetta val er gert.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Rangt spáð staða þegar nýr eiginleiki (uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun) er virkjaður (456553)

Rétt spáð staða er nú sýnd þegar uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun hefur verið virkjað.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Einingar með tengslum sem leiða til tvítekinna skoðunareiginleika (456486)

Þessi útgáfa leiðréttir vandamál með skoðunareiginleika (tengsl) margra eininga. Tvítekin tengsl finnast. Þessar aðstæður hafa allar verið lagaðar.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Athugasemdir milli fyrirtækja vegna frammistöðumats (455536)

Athugasemdir milli fyrirtækja eru nú sýnilegar á frammistöðumati með þessari lagfæringu. Þessi breyting leiðréttir yfirlit yfir athugasemdir yfirlesara sem færðar voru inn í mismunandi fyrirtækjum fyrir sama frammistöðumatið.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Ósamræmi þegar gögn launastjórnunar eru sýnd (432562)

Samræmt yfirlit yfir launagögn er nú haldið við í sjálfsafgreiðslu stjórnanda. Háð því hvernig farið er inn í **Launaupplýsingar** starfsmanns, sjá stjórnendur núna alltaf launagögnin.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Sjálfgefin gildisdagsetning launafyrirkomulags fastra launa verður að deginum í dag (411994)

Upphafsdagur launa byggir núna á upphafsdagsetningu stöðunnar sem er starfsmanninum er úthlutað.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Skjámynd leyfis og fjarveru fyrir Virkja skilgreiningu hálfs dags er óvirk þegar skjámynd opnast (452607)

Með þessari breytingu verður **Virkja skilgreiningu hálfs dags** virkjuð þangað til nýjar leyfisfærslur verða til. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Ekki er hægt að birta HcmDiscussionEntity í gegnum Excel; reitarvilla TotalRatingScore (453899)

Nú er hægt að uppfæra reitinn **TotalRatingScore** með því að nota **HCMDiscussionEntity** í hönnuði Excel-vinnubókar.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="database-logging"></a>Gagnagrunnsskráning

Gagnagrunnsskráning gerir notendum kleift að ákvarða hvaða töflum og reitum á að fylgjast með. Hann gerir einnig kleift að ákvarða tilvikin sem eiga að kveikja á breytingarakningu. Notið möguleika gagnagrunnsskráningar til að sjá þessar breytingar yfir tíma. Frekari upplýsingar er að finna í [Skilgreina og stjórna gagnagrunnsskráningu](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>Áskildir reitir 

Nú er hægt að gera reiti áskilda með því að nota sérstillingarmöguleika Human Resources. Þessi eiginleiki krefst **Vistuð yfirlit**.

## <a name="human-resources-application-in-teams"></a>Forrit „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun
 
Einingar fríðindastjórnunar eru að gefa út. DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt. Sniðmát fríðindastjórnunar verður í boði til að flytja gögn. Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl.

## <a name="buy-and-sell-leave"></a>Kaupa og selja leyfisdaga 

Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga. Þessu ferli er oft stjórnað handvirkt. Þessi eiginleiki gerir umsjón með stefnum og beiðnum sjálfvirka fyrir mannauðsdeildina. Hann einfaldar ferli leyfisstjórnunar og hjálpar til við að koma í veg fyrir mistök. Frekari upplýsingar má finna á

- [Stjórna reglum fyrir kaup og sölu á leyfisdögum](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kaupa og selja leyfisdaga](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun

Viðskiptavinir geta unnið úr uppsöfnunum fyrir eitt fyrirtæki eða eina áætlun leyfis og fjarveru. Þessi möguleiki varpar betra ljósi á uppsöfnunarferlið yfir viðskiptavini með mismunandi reglur fyrir leyfisár eða leyfisuppsöfnun. Frekari upplýsingar er að finna í [Uppsafnað leyfi á fyrirtæki eða leyfisáætlun](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Bæta viðhengjum við fríbeiðnir

Möguleikinn á því að bæta viðhengjum við samþykktar leyfisbeiðnir er mikilvægur á þessum COVID 19-tímum. Starfsmenn geta nú bætt við þessum viðhengjum. Þeir hafa einnig meiri innsýn í hvernig uppfærslur á leyfisbeiðnum eru gerðar. Frekari upplýsingar er að finna í [Bæta viðhengi við fyrirliggjandi beiðni](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Bæta ástæðukóða við frestun uppsöfnunar 

Ástæðukóðum hefur verið bætt við uppsöfnun í bið.

## <a name="carry-forward-rules"></a>Yfirfærslureglur 

Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar. Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga. Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir

Hægt er að búa til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi. Ógreit leyfi getur verið gerð, en þarf ekki að vera það. Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-eining er í boði fyrir frestun uppsöfnunar 

DMF-eining er ekki til staðar fyrir uppsöfnun í bið.

## <a name="coming-soon"></a>Væntanlegt

## <a name="configure-the-name-of-employee-self-service"></a>Stilla heiti á sjálfsafgreiðslu starfsmanns

Nýr valkostur verður í boði í **færibreytum mannauðs** til að uppfæra heiti á vinnusvæði fyrir sjálfsafgreiðslu starfsmanns í Sjálfsafgreiðsla.

## <a name="checklist-entities-included-in-dataverse"></a>Einingar gátlista innifaldar í Dataverse

Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar innan Dataverse.

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]