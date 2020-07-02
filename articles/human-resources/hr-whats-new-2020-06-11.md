---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (11. júní 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 6/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39f18dc92fb01f9a0437f4166c0f08f8d6b1b81b
ms.sourcegitcommit: 218e22014a964b8b52fc0152e355b07b0b84ae2c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456621"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (11. júní 2020)

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3316. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Einfölduð skjámynd starfsmanns veldur því stundum að hnappar (X) sem loka undirskjámynd hætti að virka (442369)

Þegar nýja skjámyndin **Starfsmaður** var virkjuð, virkaði stundum ekki hnappurinn (**X**) í undirskjámyndum sem lokar skjámynd. Þetta vandamál kom upp annað slagið. Hægt var að loka skjámyndinni eftir að hafa farið úr henni og komið aftur. Til dæmis var hægt að velja valmyndaratriði vinstra megin og fara aftur í skjámyndina **Starfsmaður** og síðan loka henni. Útgáfa vikunnar lagar þetta vandamál. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>Einingin fyrir persónulegan tengilið starfsmanns flytur ekki út persónulega tengiliði með gerð yfirtengsla

Með þessari útgáfu flytur einingin **Persónulegur tengiliður starfskrafts** út allar tengslagerðir.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPositionWorkerAssignmentV2Entity ætti að vera sjálfgefið hluti af samþættingarpakka Ceridian-launaskrár (448506)

Með þessari breytingu er **HcmPositionWorkerAssignmentV2Entity** hluti af samþættingarpakka Ceridian-launaskrár.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="database-logging"></a>Gagnagrunnsskráning

Eiginleiki gagnagrunnskladda gerir notendum kleift að ákvarða hvaða töflum og reitum á að fylgjast með. Hann gerir einnig kleift að ákvarða tilvikin sem eiga að kveikja á breytingarakningu. Notið möguleika gagnagrunnsskráningar til að sjá þessar breytingar yfir tíma. Frekari upplýsingar er að finna í [Skilgreina og stjórna gagnagrunnsskráningu](hr-admin-database-logging.md).

## <a name="human-resources-application-in-teams"></a>Forrit „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun
 
Einingar fríðindastjórnunar eru að gefa út. DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt. Sniðmát fríðindastjórnunar verður í boði til að flytja gögn. Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl.

## <a name="buy-and-sell-leave"></a>Kaupa og selja leyfisdaga 

Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga. Þessu ferli er oft stjórnað handvirkt. Þessi eiginleiki gerir umsjón með stefnum og beiðnum sjálfvirka fyrir mannauðsdeildina. Hann einfaldar ferli leyfisstjórnunar og hjálpar til við að koma í veg fyrir mistök. Frekari upplýsingar má finna á

- [Stjórna reglum fyrir kaup og sölu á leyfisdögum](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kaupa og selja leyfisdaga](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun

Viðskiptavinir geta unnið úr uppsöfnunum fyrir eitt fyrirtæki eða eina áætlun leyfis og fjarveru. Þessi möguleiki varpar betra ljósi á uppsöfnunarferlið yfir viðskiptavini með mismunandi reglur fyrir leyfisár eða leyfisuppsöfnun. Frekari upplýsingar er að finna í [Uppsafnað leyfi á fyrirtæki eða leyfisáætlun](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

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

## <a name="new-platform-capabilities"></a>Nýir verkvangsmöguleikar 

Hægt verður að gera reiti áskilda með því að nota sérstillingu. Þessi eiginleiki gerir þér kleift að virkja **Vistuð yfirlit**.

## <a name="configure-the-name-of-employee-self-service"></a>Stilla heiti á sjálfsafgreiðslu starfsmanns

Nýr valkostur verður í boði í færibreytum mannauðs til að uppfæra heiti á vinnusvæði fyrir sjálfsafgreiðslu starfsmanns í Sjálfsafgreiðsla. 
