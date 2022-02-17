---
title: Starfslok á Dynamics 365 Talent - Laða að og um borð forrit
description: Þetta efni lýsir starfslokum Dynamics 365 Talent - Laða að og um borð forrit.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: df33f35f66e356c3c2a99f0d81ebba1d0f34b5d9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069405"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract og starfslok um borð í forritum


Í desember 2019 tilkynntum við um starfslok 1. febrúar 2022 Dynamics 365 Talent - Laða að og Onboard öpp, gefa viðskiptavinum okkar tvö ár til að skipuleggja.

Fyrir frekari upplýsingar um starfslok þessara forrita, sjá:
 - [Að hætta störfum Dynamics 365 Talent - Laða að og Dynamics 365 Talent: Onboard Forrit](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Að byggja upp farsælli vinnuafl með Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Við höldum áfram að styðja Dynamics 365 Human Resources, sem mun hjálpa viðskiptavinum okkar að fá þá innsýn í vinnuafl sem þarf til að byggja upp gagnastýrða starfsreynslu á mörgum sviðum, svo sem:

- Laun
- Fríðindi
- Leyfi og fjarvera
- Samræmi
- Payroll
- Endurgjöf um frammistöðu
- Þjálfun og vottun
- Sjálfsafgreiðsluáætlanir

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent Algengar spurningar um starfslok forrit

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Hver er notendaupplifunin fyrir bæði Dynamics 365 Talent - Aðdráttarafl og forrit um borð frá og með 1. febrúar 2022?

Notendur munu ekki geta notað forritin og er vísað á eftirlaunasíðu.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Geta viðskiptavinir haldið áfram að flytja út gögn fyrir bæði Dynamics 365 Talent - Laða að og Onboard öpp eftir 1. febrúar 2022?
  
Nei, tilkynnt var um starfslok í desember 2019 og tilskilin útflutningsgeta var veitt til 1. febrúar 2022. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Munu gögn viðskiptavinarins tengjast hvoru tveggja Dynamics 365 Talent - Laðaðu að og um borð forrit inn Dataverse verði eytt eftir 1. febrúar 2022?

Nei, the Dataverse einingar verða áfram í viðskiptavinarins Microsoft Dataverse umhverfi jafnvel eftir starfslok nema Human Capital Management Talent lausninni sé eytt eða fjarlægð.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Ég veit hvað Talent umhverfið heitir. Hvernig get ég séð Attract og Onboard gögnin í Dataverse?

1.  Skrá inn Power Apps :https://make.powerapps.com
2.  Veldu umhverfið sem þú vilt sjá Attract og Onboard gögn í.
3.  Fara til **Dataverse > Töflur**. 
4.  Sláðu inn "msdyn_" inn **Leita**. Ef þú sérð lista yfir töflur sem byrja á "msdyn_" + töfluheiti (dæmi: msdyn_candidate) þá hefur þú fundið umhverfið með Attract og Onboard gögnum.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Ég veit ekki hvað Talent umhverfið heitir. Hvernig get ég fundið umhverfið sem hefur gögnin fyrir Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard umsóknir?

1)  Skrá inn Power Platform stjórnendamiðstöð:https://admin.powerplatform.microsoft.com/
2)  Veldu **Umhverfi**.
3)  Veldu tiltekið umhverfi til að meta.
4)  Veldu **Tilföng > Dynamics 365 forrit**.
5)  Ef þú sérð **HCM Talent** lausn uppsett, ætti þetta umhverfi að hafa Attract og Onboard gögn geymd í því. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> The **HCM Talent** lausn er einnig notuð í Dynamics 365 Human Resources.
