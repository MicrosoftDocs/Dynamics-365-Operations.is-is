---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (13. apríl 2020)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f61283f3bab26f54d55ffe7cbea21b1201ed234
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555148"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (13. apríl 2020)

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3136. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="new-production-release-cadence"></a>Ný tíðni framleiðsluútgáfu

Með útgáfu þessarar viku breytist losunarferlið fyrir Human Resources úr vikulegri uppfærslu í hálfsmánaðar uppfærslu. Til að tryggja samræmingu við örugga notkun á vettvangi og viðhalda háum stöðlum um stöðugleika og áreiðanleika í þjónustunni er ferlið við að dreifa þjónustuuppfærslum á öllum svæðum núna í hálfsmánaðar útgáfu. Viðbótarprófanir og skjáir eru uppsettir til að staðfesta árangursríka dreifingu á hverju stigi ferlisins. Nánari upplýsingar um losunarrýmið, sjá [Uppfæra ferli](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Ekki er hægt að breyta reitnum Sléttunarnákvæmni þegar gerð sléttunar hefur verið tilgreind (435616)

Með þessari breytingu er reiturinn **Sléttunarnákvæmni** nú tiltækur eftir að þú uppfærir reitinn **Gerð sléttunar**.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Ekki hægt að breyta lokadegi leyfisskráningar þegar leyfistímabilið er ekki með uppsöfnunartímabil (413628)

Þú getur nú breytt lokadagsetningu skráningar án þess að fá villuna „Fylla verður út reitinn Grundvöllur uppsöfnunardags”.

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a>Starfseiningin samstillist ekki við Common Data Service (430834)

Þessi breyting leiðréttir vandamál þar sem starfsgögn samstilltust ekki við Common Data Service þegar fjárhagsvíddum hefur verið bætt við. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Fjarlægja fjölyfireiningar fyrir eininguna Tímabil vinnudagatals (431775)

Þessi breyting fjarlægir fjölyfireiningar fyrir eininguna **Tímabil vinnudagatals**.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Sía með CAST aðgerð virkar ekki á OData kall einingar Stöðuúthlutun starfskrafts (431699)

Þessi uppfærsla felur í sér breytingu til að leyfa síu með CAST aðgerð innan OData fyrir eininguna **Stöðuúthlutun starfskrafts**.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="leave-suspension"></a>Frestun leyfis

Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann. Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir. Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns. Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Yfirfærslureglur

Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar. Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga. Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Þekkt vandamál

## <a name="employment-details-entity"></a>Atvinnuupplýsingaeining

Einingin **Starfsupplýsingar** hefur verið uppfærð með eftirfarandi reitum:

- **Greiðslutíðni**
- **Kenni starfsgreinar**
- **Starfsheiti**
- **Kenni starfsheitis**
- **Staða starfsfríðinda**

Uppsetningargögnin fyrir þessa reiti treysta á að fríðindastjórnun sé virkjuð á vinnusvæðinu **Eiginleikastjórnun**. Þessa reitir ætti ekki að fylla út eða uppfæra í einingunni **Starfsupplýsingar** þar sem það mun valda villum við innflutning.

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