---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources 28. janúar 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 28. janúar 2021.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d59e242421b1b86c32f9009ae6ae17e0f161a2e2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689299"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Nýjungar eða breytingar í Dynamics 365 Human Resources 28. janúar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.3906.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Samþætta ástæðukóða fríðinda inn í vinnusvæði **Starfsmannastjórnunar** | -- | [Setja upp ástæðukóða](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.


| Númer úthreyfingar | Úthreyfing |  lýsing |
| --- | --- | --- |
| 539456 | Dagatal sýnir leyfisgerðina í texta yfir bendli þegar færibreytan **Sýna aðeins fjarvistir án upplýsinga** er virkjuð. | Þegar valkosturinn **Sýna aðeins fjarvistir án upplýsinga** er virkjaður birtist dagsetning beiðninnar nú yfir bendlinum. |
| 528907 | Að veita lögaðila aðgang að starfsmannahlutverki leiðir til þess að stjórnendur geti ekki séð aðgerð leyfissöðu fyrir starfsmenn á svæðinu **Teymið mitt** í sjálfsafgreiðslu starfsmanns. |Ef þessi valkostur er stilltur gerir stjórnendum kleift að sjá áfram aðgerð leyfisstöðu. |
| 526280 | Heimildarvilla í HcmWorkerEntity, HcmEmployeeEntity og HcmContractorEntity. | Notendur í öðru hlutverki en kerfisstjóra gátu ekki flutt út birtar einingar sökum heimildarvillu í reitnum NationalityCountryRegion. Notendur þurfa áfram fylgja réttindum til að flytja út þessar upplýsingar: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain og HCMContractorEntityView. |
| 542147 | Reitirnir **Bankareikningsnúmer** og **Leiðarnúmer** eru áskildir þegar bankareikningi er bætt við í gegnum sjálfsafgreiðslu starfsmanns. | Villan hefur verið löguð þar sem starfsmenn þurftu að færa inn **Bankareikningsnúmer** og **Leiðarnúmer** þegar bankareikningsupplýsingum var bætt við. Þessir reitir eru ekki lengur áskildir þegar nýjar bankareikningsupplýsingar eru vistaðar. |
| 543641 | Póstnúmer fyllist ekki út í rafrænni skýrslugerð. | Villa löguð þar sem póstnúmer fylltist ekki út í ACA-tilkynningu fyrir tryggingarkóða L til Q. |
| 545402 | Bætið við breytingu leiðar fyrir skrá UserBranding.js til að fjarlægja 404 villur. | Notandi ætti ekki að sjá lengur villu 404 á stjórnborðinu. |

## <a name="in-preview"></a>Í kynningarútgáfu   

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Human Resources-forritið í Microsoft Teams | [Viðmót fyrir leyfi og fjarvistir starfsmanns í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md)<br>[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md) |
| Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks | [Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Grunnstilla færibreytur leyfis og fjarvista](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Staðfesting í tölvupósti um fríðindaskráningu | Þessi eiginleiki býður upp á valkost til að senda staðfestingu í tölvupósti til starfsmanna þegar þeir skrá sig úr upplifunum fríðindaskráningar í sjálfsafgreiðslu starfsmanns. Þessi eiginleiki verður í boði 1. febrúar. Frekari upplýsingar er að finna í [Grunnstilla færibreytur fríðindastjórnunar eftir fyrirtæki](hr-benefits-setup-parameters-per-company.md). |
| Hæfni sem yfirmaður færir inn fyrir starfsmenn sína getur verið sjálfkrafa samþykkt af verkferlinu | Væntanlegt. |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Uppfærsla hugtaka fyrir Microsoft Dataverse

Tekur gildi í nóvember 2020, Common Data Service hefur verið endurnefnt [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Frekari upplýsingar er að finna í [opinberri tilkynningu](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) á Power Apps blogginu. Í samhengi við þessa nafnabreytingu hafa nokkur hugtök í Dataverse verið uppfærð. Sem dæmi er *eining* núna *tafla* og *svæði* er núna *dálkur*. Frekari upplýsingar eru í [Uppfærslur hugtaka](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Í þessari útgáfu hafa hugtök sem tengjast samþættingu Dynamics 365 Human Resources við Dataverse verið uppfærð í öllu forritinu til að endurspegla þessar breytingar. Til dæmis er skjámyndin **Common Data Service samþætting** orðin **Microsoft Dataverse samþætting**.

Frekari upplýsingar um samþættingu Dynamics 365 Human Resources við Microsoft Dataverse er að finna í [Grunnstilla Microsoft Dataverse samþættingu](./hr-admin-integration-common-data-service.md) og [Grunnstilla Microsoft Dataverse sýndartöflur](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]