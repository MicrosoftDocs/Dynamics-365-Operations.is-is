---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (28. maí 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 28. maí 2020.
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42cb9e595c2997f17f487c31f674d1c099a3c80d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902948"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources (28. maí 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3287. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>LeaveRequest virkar ekki þegar margar gerðir eru gerðar fyrir hverja leyfisáætlun (447498)

Með þessari breytingu er **LeaveEnrollmentV2Entity** nú tiltæk til að leiðrétta villuna sem kemur upp þegar margar leyfisgerðir eru gerðar virkar.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Minnkunareiginleiki runusteytingar (forútgáfa) (446619)

Þegar þessi eiginleiki er gerður virkur má búast við fækkun á lokunum á rammatöflum runu við verkval og verklok.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UppdateConflict þegar starfsmenn eru vistaðir kemur í veg fyrir breytingu á færslu í Einstaklingar (427915)

Þessi breyting leiðréttir villu þegar nýjum starfsmanni er bætt við, upplýsingum um aðsetur er breytt og kjörstillingum tungumáls er breytt. Í þessari sérstöku atburðarás birtist villa sem gefur til kynna að ekki hafi verið hægt að uppfæra færsluna. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Ekki er hægt að bæta viðhengi við samþykkta beiðni um leyfi til að endursenda (425407)

Þessi breyting leyfir nú viðhengi við samþykktar leyfisbeiðnir.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Notandi getur fært inn laun fyrir starfsmann í skjámynd annars lögaðila (409529)

Þessi breyting slekkur á launavalkostum til að koma í veg fyrir að launafærslur séu óvart færðar inn í rangan lögaðila.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Villa þegar starfsmaður er fluttur og úthlutunardagur stöðu starfsmanns er á undan tímalengd stöðu (429402)

Villuboð þegar starfsmaður er fluttur í þessari atburðarás hafa verið uppfærð til að geta lýst betur þeim breytingum sem þarf til að leiðrétta vandamálið.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Möguleikar viðhengja í sjálfsafgreiðslu fríðindaskráningar starfsmanns
 
Nú er hægt að bæta viðhengjum við ferli fríðindaskráningar fyrir hverja áætlun sem starfsmaðurinn skráir sig í. Hægt er að skoða viðhengin í skjámyndinni **Skráð fríðindi starfsmanns**.

## <a name="in-preview"></a>Í kynningarútgáfu

## <a name="human-resources-application-in-teams"></a>Forrit „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](./hr-admin-teams-leave-app.md). 

## <a name="leave-suspension"></a>Frestun leyfis

Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann. Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir. Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns. Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Uppfæra notendaupplifun til að sýna að uppsöfnun sé frestað (429550)

Notandaupplifunin sýnir nú að uppsöfnun hafi verið frestað fyrir áætlun.

## <a name="coming-soon"></a>Væntanlegt

## <a name="database-logging-in-preview-in-june"></a>Skráning gagnagrunns (í forútgáfu í júní)

Eiginleiki gagnagrunnskladda gerir notendum kleift að ákvarða hvaða töflu og reiti á að fylgjast með. Hann gerir einnig kleift að ákvarða tilvikin sem eiga að kveikja á breytingarakningu. Fyrirspurnarmöguleikar eru í boði til að sjá þessar breytingar yfir tíma.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Kaupa og selja leyfisdaga (í forútgáfu 1. júní)

Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga. Þessu ferli er oft stjórnað handvirkt. Þessi eiginleiki býður upp á sjálfvirkari leið til að stjórna stefnum og beiðnum fyrir mannauðsdeildina og auðveldar að koma í veg fyrir mistök við einföldun á ferli leyfisstjórnunar. Frekari upplýsingar má finna á

- [Stjórna reglum fyrir kaup og sölu á leyfisdögum](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kaupa og selja leyfisdaga](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun
 
Einingar fríðindastjórnunar eru að gefa út. DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt. Sniðmát fríðindastjórnunar verður einnig í boði til að flytja gögn. Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Bæta ástæðukóða við uppsöfnun í bið (1. júní)

Ástæðukóðum hefur verið bætt við uppsöfnun í bið.

## <a name="carry-forward-rules-june-1"></a>Yfirfærslureglur (1. júní)

Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar. Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga. Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir (1. júní)

Í þessari útgáfu getur mannauður búið til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi. Ógreit leyfi getur verið gerð, en þarf ekki að vera það. Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF-eining er í boði fyrir frestun uppsöfnunar (1. júní)

DMF-eining er ekki til staðar fyrir uppsöfnun í bið.

## <a name="see-also"></a>Sjá einnig

[Nýjungar í Human Resources](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]