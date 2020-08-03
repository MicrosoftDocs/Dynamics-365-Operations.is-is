---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (1. maí 2020)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e4da626ce3412fba6f90dd7f953c1cbc79ab60c3
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555124"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (1. maí 2020)

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3196. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Nýjar frammistöðustjórnunareiningar sem eru í boði í Gagnastjórnunarramma (DMF)

Eftirfarandi einingar eru nú tiltækar. Ef þú sérð þessar einingar ekki skráðar á einingalistanum notarðu valkostinn **Uppfæra einingar** í **Rammafæribreytur > Einingastillingar > Uppfæra skrá yfir einingar**.

- **Umræðuhæfi**
- **Umræðumarkmið**
- **Umræðumælingar**
- **Umræðuefni**
- **Frammistöðubók**
- **Mæling**
- **Markmiðamælingar**

Að auki var **Heildarstigafjöldi** og **Meðalstigafjöldi** bætt við eininguna **Umræður**.

## <a name="increase-length-of-leave-request-comments-275641"></a>Auka lengd athugasemdar við leyfisbeiðni (275641)

Athugasemdir um leyfisbeiðnir geta nú innihaldið meira en 100 stafi.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Endanlegar athugasemdir við umsagnir birtast ekki þegar stjórnandi eða starfsmaður er skráður inn í annað fyrirtæki (431688)

Allar athugasemdir birtast nú þegar umsagnir eru skoðaðar.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Notandaskilgreindir tenglar eru ekki studdir á nýju eyðublaði Starfskrafts (390374)

Notandaskilgreindir tenglar eru nú virkjaðir á skjámyndinni **Starfskraftur**.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity veldur hruni í OData API (439476)

Þessi breyting leiðréttir API-hrun. Tvítekið heiti bjó til þessa villu.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="leave-suspension"></a>Frestun leyfis

Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann. Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir. Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns. Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Uppfæra notendaupplifun til að sýna að uppsöfnun sé frestað (429550)

Notandaupplifunin sýnir nú að uppsöfnun hafi verið frestað fyrir áætlun.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir (272447)

Í þessari útgáfu getur mannauður búið til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi. Ógreit leyfi getur verið gerð, en þarf ekki að vera það. Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-eining er í boði fyrir frestun uppsöfnunar (429549)

DMF-eining er ekki til staðar fyrir uppsöfnun í bið.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Bæta ástæðukóða við frestun uppsöfnunar (429547)

Ástæðukóðum hefur verið bætt við uppsöfnun í bið.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Hefja flutning úr færibreytum Human Resources í færibreytur leyfis og fjarvista

Þessi útgáfa byrjar á að sameina færibreytur mannauðsstjórnunar með færibreytum leyfis og fjarvista.

## <a name="carry-forward-rules"></a>Yfirfærslureglur

Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar. Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga. Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Þekkt vandamál

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint forsýning virkar ekki í sumum umhverfum

Ef forskoðun skjals fyrir skjöl sem eru vistuð í SharePoint virkar ekki, prófaðu eftirfarandi aðferð:

1. Staðfestu að notandareikningur stjórnanda sé með tölvupóst sem tengist notendaskránni. Þessar upplýsingar er hægt að skoða á síðunni **Notandi**. Ef tölvupóstur er ekki settur upp þarftu að bæta við tölvupóstinum og veitunni með OData Excel viðbótinni. Sjálfgefið er að netfangið er ekki til í Excel-hönnuninni. Þú þarft að breyta Excel hönnuninni, bæta við öllum reitum, beita og endurnýja. Þegar þú hefur lokið þessum skrefum geturðu uppfært stjórnandareikninginn.

2. Þegar stjórnandareikningurinn er með tilheyrandi tölvupóstreikning skaltu skrá þig inn á Human Resources með stjórnandaskilríkjum.

3. Opnaðu viðhengi í SharePoint til að hefja forskoðun skjalsins.

4. Skráðu þig inn með öðrum notendareikningi sem hefur aðgang að viðhengjum og sannreyndu að forsýningin virkar eins og búist var við.

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)