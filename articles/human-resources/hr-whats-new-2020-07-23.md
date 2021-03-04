---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (23. júlí 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 23. júlí 2020.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d0672e3039f54a4591db49eee00d69bf5e4278fd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528450"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (23. júlí 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3416. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Eyðing fjárhagsvídda fyrir stöðu virkar ekki eins og búist var við (445476)

Að fjarlægja víddir úr stöðu fjarlægir þessar sömu stöður úr Common Data Service.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Stöður sem ekki eru í stigveldi sýna óvirkar stöður (397257)

Stöður sem eru óvirkar (eru með útrunna tímalengd) birtast ekki lengur í stöðustigveldinu sem **Stöður sem ekki eru í stigveldi**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Sannprófun á milli LeaveEnrollmentEntity og HcmWorkerEntity í innflutningi gagnastjórnunarramma (DMF) veldur hægri hleðslu á gögnum (442324)

Breytingar á þessari útgáfu auka afköst **LeaveEnrollmentEntity**.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Ekki er hægt að sérsníða í fyrirtækisstjórnun (447490)

Með þessari breytingu er nú hægt að sérsníða tengla í **Fyrirtækisstjórnun**.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="mandatory-fields"></a>Áskildir reitir 

Nú er hægt að gera reiti áskilda með því að nota sérstillingarmöguleika Human Resources. Þessi eiginleiki krefst **Vistuð yfirlit**.

## <a name="human-resources-application-in-teams"></a>Forrit „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun
 
Einingar fríðindastjórnunar eru að gefa út. DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt. Sniðmát fríðindastjórnunar verður í boði til að flytja gögn. Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl.

## <a name="buy-and-sell-leave"></a>Kaupa og selja leyfisdaga 

Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga. Þessu ferli er oft stjórnað handvirkt. Þessi eiginleiki gerir umsjón með stefnum og beiðnum sjálfvirka fyrir mannauðsdeildina. Hann einfaldar ferli leyfisstjórnunar og hjálpar til við að koma í veg fyrir mistök. Frekari upplýsingar má finna á

- [Stjórna reglum fyrir kaup og sölu á leyfisdögum](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kaupa og selja leyfisdaga](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun

Viðskiptavinir geta unnið úr uppsöfnunum fyrir eitt fyrirtæki eða eina áætlun leyfis og fjarveru. Þessi möguleiki varpar betra ljósi á uppsöfnunarferlið yfir viðskiptavini með mismunandi reglur fyrir leyfisár eða leyfisuppsöfnun. Frekari upplýsingar er að finna í [Uppsafnað leyfi á fyrirtæki eða leyfisáætlun](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Bæta viðhengjum við frítímabeiðnir

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

## <a name="checklist-entities-included-in-common-data-service"></a>Einingar gátlista innifaldar í Common Data Service

Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Common Data Service.

## <a name="platform-changes"></a>Verkvangsbreytingar

Verkvangsuppfærsla 10.0.12 (36)

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]