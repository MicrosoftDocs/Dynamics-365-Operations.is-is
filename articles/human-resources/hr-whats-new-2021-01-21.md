---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 21. janúar 2021
description: Þessi grein lýsir eiginleikum sem eru annað hvort nýir eða breyttir í Microsoft Dynamics 365 Human Resources fyrir 21. janúar 2021.
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f1daf630d3a9354012db9b5b487d8a5ed11e0ed
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066701"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 21. janúar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir eiginleikum sem eru nýir, breyttir eða koma fljótlega í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 2 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.3866.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Verkvangsuppfærsla 10.0.16(40) | -- | [Palluppfærslur fyrir útgáfu 10.0.16 af fjármála- og rekstraröppum (febrúar 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| Bættar verkflæðisbeiðnir og samþykktir | [Endurbætur á viðmóti fyrir verkflæði fyrirtækis- og starfsmannastjórnunar](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Uppfærslur á reglufylgni Affordable Care Act fyrir eyðublað 1095-C, eyðublað 1095-B og rafræna skýrslugerð í eldri fríðindum | -- | -- | 
| Fríðindastjórnun styður nú skýrslugerð ACA-reglufylgni fyrir lögaðila í Bandaríkjunum | -- | [Mynda ACA-skýrslur í Fríðindastjórnun](hr-benefits-management-aca-reports.md) |
| Fríðindastjórnun er nú með einingar fyrir lög fríðindahlutfalls og tvöföld lög fríðindahlutfalls  | -- | -- |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þessa grein til að innihalda villuleiðréttingar sem komu inn í bygginguna eftir að þessi grein var upphaflega birt.

| Númer úthreyfingar | Gefa út |  Lýsing |
| --- | --- | --- |
| 533079 | Skoðunarvilla „Ekki var kallað rétt á eyðublað“ þegar við reynum að líta á frádrátt. | Villa löguð þegar frádráttur fríðinda var skoðaður með yfirlitinu **Frá og með dagsetningu**. |
| 543641 | Póstnúmer fyllist ekki út í rafrænni skýrslugerð.  | Innri villa löguð þar sem póstnúmer birtist ekki í rafrænum ACA-skýrslum fyrir fríðindastjórnun þegar tryggingakóðinn er M til Q. |
| 542815 | Skjámynd persónulegs tengiliðar í sjálfsafgreiðslu starfsmanns gerir starfsmönnum kleift að sjá persónulega tengiliði annarra. | Villa löguð þar sem **Breyta** í eyðublaði fyrir persónulega tengiliði í sjálfsafgreiðslu starfsmanns takmarkar ekki fyrirspurnina nógu vel til að tryggja að aðeins einn persónulegur tengiliður er sóttur, sem leyfir notanda að nota flýtilykla á lyklaborði til að skoða tengiliðaupplýsingar annarra. |
| 536157 | Ekki er hægt opna síðuna **Microsoft Dataverse samþætting** í kerfisstjórnun vegna kalls IsVirtualEntityPackageInstalled(). | Vandamál kemur í veg fyrir að síðan **Microsoft Dataverse samþætting** hlaðist í Human Resources. |
| 533079 | Skoðunarvilla „Ekki var kallað rétt á eyðublað“ þegar við reynum að líta á frádrátt. | Villa löguð sem kemur upp í **Frádrætti** í eyðublaði fyrir fríðindastjórnun þegar skoðað sem **Frá og með dagsetningu**. |
| 537264 | Flýtiflipann **Persónulegar upplýsingar** vantar úr færslu umsækjanda. | Persónulegar upplýsingar umsækjandans eru nú í boði í færslu umsækjanda. |
| 537267 | **Starfsreynsla** birtist ekki í færslum innri umsækjanda. | Flýtiflipinn **Starfsreynsla** birtist nú í færslum innri umsækjanda. Áður fyrr, ef umsækjandinn var innri umsækjandi, var **Starfsreynslu** skipt út fyrir **Ráðningarsögu**, sem er ráðningarsaga umsækjandans innan fyrirtækisins. Bæði á við og verður að birtast fyrir innri umsækjanda. |
| 537067 | **Má hafa samband við vinnuveitanda** birtist ekki. | Stýringin **Má hafa samband við vinnuveitanda** var bætt við gluggann **Breyta starfsreynslu** fyrir færslu umsækjanda. |
| 525957 | **Staða umsækjanda** uppfærist ekki hjá innri umsækjendum þegar flutningi lýkur. | Þegar flutningi lýkur (hnappurinn **Breyta stöðu** eða **Halda áfram** er valinn á síðunni **Flytja starfsmann í nýtt stöðuverkefni**) verður **Staða** umsækjandafærslunnar að breytast í **Ráðin(n)**. |
| 537051 | Gjaldmiðilstákn fyrir indverska rúpíu og tyrkneska líru samstillast ekki á réttan hátt við Dataverse | Tákn fyrir indverska rúpíu og tyrkneska líru samstillast á réttan hátt við Dataverse. |
| 534846 | Ráðningartöflur verða að vera virkjaðar fyrir gagnastjórnun. | Nýju töflurnar sem búnar voru til fyrir ráðningarbeiðnir og umsækjendur eru nú virkar fyrir gagnastjórnun. Þetta gerir kleift að virkja breytingarrakningu fyrir töflurnar, virkjar OData-breytingarrakningu í sýndartöflu Dataverse. |
| 533474 | Laga vöntun á tilvísun í Microsoft.SqlServer.XEvent.dll. | Undantekningar samsetningarhleðslu fyrir Microsoft.SqlServer.XEvent.dll lokuðu fyrir að sýndartöflur Dataverse yrðu uppsettar í sumum umhverfum. |
| 481122 | Vinnusvæðið **Einstaklingar** sýnir stöður þar sem hætt hefur verið störfum. | Stöður þar sem hætt hefur verið störfum birtust sem opnar stöður á vinnusvæðinu **Einstaklingar**. Stöður þar sem hætt hefur verið störfum sjást ekki lengur. | 
| 541978 | Bæta aðalnetfangi við einingu BaseWorker. | Þessi breyting bætti aðalnetfangi starfsmanns við HcmWorkerBaseEntity. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Human Resources-forritið í Microsoft Teams | [Viðmót fyrir leyfi og fjarvistir starfsmanns í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md)<br>[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md) |
| Samþætting við LinkedIn Talent Hub | [Samþætting við LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Samþætta við LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks | [Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Grunnstilla færibreytur leyfis og fjarvista](./hr-leave-and-absence-parameters.md) |
|Veita frekari innsýn í leyfisstöðu| [Veita frekari innsýn í leyfisstöðu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Stjórna leyfi starfsmanns](./hr-leave-and-absence-manage-employee-leave.md) |
| Stjórnendur geta sent ráðningarbeiðnir fyrir stöður | [Stjórnendur geta sent inn ráðningarbeiðni fyrir opnar stöður](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Bæta við ráðningarbeiðni](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Auknar notandaupplýsingar umsækjanda í starfsmannastjórnun | [Auknar notandaupplýsingar umsækjanda í starfsmannastjórnun](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Bæta við eða breyta notandaupplýsingum umsækjanda](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Virkja einfaldar samþættingar með ráðningaraðilum | [Virkja einfaldar samþættingar með ráðningaraðilum](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Ráða umsækjendur](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Væntanlegt
| Eiginleiki | Upplýsingar |
| --- | --- |
| Staðfesting í tölvupósti um fríðindaskráningu | Þessi eiginleiki býður upp á valkost til að senda staðfestingu í tölvupósti til starfsmanna þegar þeir skrá sig úr upplifunum fríðindaskráningar í sjálfsafgreiðslu starfsmanns. Frekari upplýsingar er að finna í [Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki](hr-benefits-setup-parameters-per-company.md). |
| Hæfni sem yfirmaður færir inn fyrir starfsmenn sína getur verið sjálfkrafa samþykkt af verkferlinu | Væntanlegt. |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2020 losunarbylgju 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Uppfærsla hugtaka fyrir Microsoft Dataverse

Tekur gildi í nóvember 2020, Common Data Service hefur verið endurnefnt [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Frekari upplýsingar er að finna í [opinberri tilkynningu](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) á Power Apps blogginu. Í samhengi við þessa nafnabreytingu hafa nokkur hugtök í Dataverse verið uppfærð. Sem dæmi er *eining* núna *tafla* og *svæði* er núna *dálkur*. Frekari upplýsingar eru í [Uppfærslur hugtaka](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Í þessari útgáfu hafa hugtök sem tengjast samþættingu Dynamics 365 Human Resources við Dataverse verið uppfærð í öllu forritinu til að endurspegla þessar breytingar. Til dæmis er skjámyndin **Common Data Service samþætting** orðin **Microsoft Dataverse samþætting**.

Frekari upplýsingar um samþættingu Dynamics 365 Human Resources við Microsoft Dataverse er að finna í [Grunnstilla Microsoft Dataverse samþættingu](./hr-admin-integration-common-data-service.md) og [Grunnstilla Microsoft Dataverse sýndartöflur](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2020 losunarbylgju 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
