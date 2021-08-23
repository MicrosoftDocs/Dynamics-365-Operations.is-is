---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (06. ágúst 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 6. ágúst 2020.
author: andreabichsel
ms.date: 08/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c9cd01f5d96794cf3ed7f29a9fae21b67cd298acda36401b7f0f65d073cbbfbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761879"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources (06. ágúst 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources. Breytingar eiga við um byggingarnúmer 8.1.3444. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.

## <a name="platform-update-1001236-is-now-available"></a>Verkvangsuppfærsla 10.0.12(36) er nú í boði

Frekari upplýsingar er að finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.12 fyrir Finance and Operations-forrit (ágúst 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12.md).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun
 
Einingar fríðindastjórnunar eru að gefa út. DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt. Sniðmát fríðindastjórnunar verður í boði til að flytja gögn. Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl. Frekari upplýsingar má finna á

- [Stuðningur DMF-einingu](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) í Dynamics 365 2020 útgáfutímabilsáætlun 1
- [Yfirlit gagnastjórnunar](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire stofnar verkflæði fyrir kaup og sölur á leyfisbeiðnum (446557)

Frekari upplýsingar má finna á

- [Leyfa starfsmönnum að kaupa og selja leyfi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) í Dynamics 365 2020 útgáfutímabilsáætlun 2
- [Stjórna reglum fyrir kaup og sölu á leyfisdögum](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kaupa og selja leyfisdaga](./hr-employee-self-service-buy-sell-leave.md)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Póstfangseining starfsmann V2 er með aðgang að lögaðilum með takmarkaðan aðgang (459126)

Með þessari breytingu mun einingin **Póstfang starfsmanns V2** takmarka samkvæmt aðgangi að lögaðila sem notandi fær.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Tengill í tölvupósti á verkflæði opnar ekki viðeigandi umsagnir (437398)

Þegar staðgengillinn er notaður til að opna frammistöðumat í verkflæði frammistöðu, opnar tengillinn sem myndaður er í tölvupóstinum núna völdu færsluna.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Nýjar einingar fyrir kaup og sölu leyfis (473180)

Rammaeiningar gagnastjórnunar eru nú til staðar til að kaupa og selja leyfi. Nánari upplýsingar er að finna í [Yfirlit gagnastjórnunar](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Þegar færsluupplýsingar eru skoðaðar og ítarlegar síur eru notaðar, getur notandi fengið aðgang að færslum annarra starfsmanna (472490)

Með þessari breytingu geta notendur sjálfsafgreiðslu starfsmanna aðeins fengið aðgang að eigin færslum þegar þeir nota sjálfsafgreiðslu starfsmanna. Að skoða upplýsingar um færslu á meðan síuvalkostinum er breytt birtir ekki lengur viðbótargögn.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Greiningar starfsmannastjórnunar innihalda lokaðar starfsmannaskrár (382893)

Með þessari útgáfu innihalda greiningar starfsmannastjórnunar nú aðeins virka starfsmenn. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Ekki er hægt að vinna úr verðleikaaukningu fyrir starfsmann (473125)

Þessi breyting gerir þér kleift að færa inn verðleikaaukningar þegar gildisdagsetningu fyrir nýja verðleikaaukningu er breytt.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Hægt er að hefja yfirferð verkflæðis oftar en einu sinni (467541)

Með þessari breytingu er aðeins hægt að hefja verkflæði frammistöðumats einu sinni. Staða stjórnanda birtir ekki lengur valkostinn um að hefja matið.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Verkflæði leyfisbeiðni endar í villu þegar hætt er við samþykkta leyfisbeiðni (472063)

Í þessari útgáfu, þegar hætt er við samþykkta beiðni um leyfi, er staða beiðninnar ekki lengur samþykkt og verkflæðið mun halda áfram.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Kerfið stingur upp á hættum starfsmönnum þegar ný skjámynd úr sniðmáti (460624)

Með þessari breytingu eru hættir starfsmenn ekki lengur í boði þegar nýtt mat er búið til úr sniðmáti. Ekki er hægt að búa til mat fyrir starfsmenn sem er fyrir utan ráðningartíma þeirra.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Hringtilvísun á stigveldi stöðu greint (415879)

Með þessari breytingu takmarkast greining á hringtilvísun á stigveldi stöðu við eitt skipti. Hægt er að keyra greiningu hringtilvísunar fyrir mismunandi dagsetningar til að sannprófa að skipulag skýrslugerðar sé ekki með neinar hringtilvísanir.

## <a name="buy-and-sell-leave"></a>Kaupa og selja leyfisdaga 

Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga. Þessu ferli er oft stjórnað handvirkt. Þessi eiginleiki gerir umsjón með stefnum og beiðnum sjálfvirka fyrir mannauðsdeildina. Hann einfaldar ferli leyfisstjórnunar og hjálpar til við að koma í veg fyrir mistök. Frekari upplýsingar má finna á

- [Leyfa starfsmönnum að kaupa og selja leyfi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) í Dynamics 365 2020 útgáfutímabilsáætlun 2
- [Stjórna reglum fyrir kaup og sölu á leyfisdögum](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kaupa og selja leyfisdaga](./hr-employee-self-service-buy-sell-leave.md)

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

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="mandatory-fields"></a>Áskildir reitir

Hægt er að gera reiti áskilda með því að nota sérstillingarmöguleika Human Resources. Þessi eiginleiki krefst **Vistuð yfirlit**. Nánari upplýsingar um vistuð yfirlit er að finna í:

- [Vistuð yfirlit - almennt framboð](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) í Dynamics 365 2020 útgáfutímabilsáætlun 2
- [Búa til skjámyndir sem nýta vistuð yfirlit til fullnustu](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Forrit „Human Resources“ í Teams

Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams. Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi. Frekari upplýsingar má finna á

- [Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 1
- [Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-eining er í boði fyrir frestun uppsöfnunar

DMF-eining er ekki til staðar fyrir uppsöfnun í bið.

## <a name="coming-soon"></a>Væntanlegt

## <a name="checklist-entities-included-in-dataverse"></a>Einingar gátlista innifaldar í Dataverse

Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Dataverse.

## <a name="known-issues"></a>Þekkt vandamál

Vinnusvæðið **Eiginleikastjórnun** sýnir hugsanlega eiginleika sem eru óvirkir sem eiginleikar forútgáfu þegar þeir eru almennt í boði. Hér að neðan er listi yfir almennt tiltæka eiginleika sem sýna ranga stöðu. 

1.  Fríðindastjórnun
2.  Málastjórnun
3.  Gagnagrunnsskráningar (eftirlit)
4.  Uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun
5.  Frestun uppsafnaðs leyfis og fjarvista
6.  Ástæðukóði og athugasemd við stöðuleiðréttingu
7.  Kaupa og selja leyfisdaga
8.  Leyfis- og fjarvistadagatal
9.  Reglur um yfirfærslu leyfis
10. Endurskoðun uppsafnaðs leyfis
11. Eyðing á uppsöfnuðu leyfi
12. Sléttun uppsafnaðs leyfis
13. Grunnstilla margar leyfisgerðir í einni leyfisáætlun
14. Uppfæra viðbætur fyrir frí
15. Nota JFS starfsmanns fyrir uppsöfnun
16. Launayfirlit þvert á fyrirtæki
17. Prenta árangursumsagnir
18. Leiðréttingar á uppsöfnun frídaga

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]