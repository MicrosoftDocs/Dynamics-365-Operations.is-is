---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 22. febrúar 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 22. febrúar 2021.
author: marcelbf
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61f86cd6168d700a5316768b328466b08d9e8f51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892610"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 22. febrúar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.3988.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Dynamics 365 Human Resources forrit fyrir Microsoft Teams | [Viðmót fyrir leyfi og fjarvistir starfsmanns í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md)<br>[Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Úthreyfing |  lýsing |
| --- | --- | --- |
| 529994 | Breytingar á reitnum **Þekkt sem** í skjámynd **Starfsmanns** ræsir ekki Dataverse-uppfærslu | Vandamál leyst þar sem Dataverse uppfærist ekki þegar reiturinn **Þekkt sem** er uppfærður í skjámynd **Starfsmanns**. |
| 532651 | Skýrsla um PBI-launagreiningu notar ekki umreikning gjaldmiðils þegar mælingar eru reiknaðar út fyrir allt fyrirtækið | Vandamál leyst þar sem skýrsla um PBI-launagreiningu umreiknaði gjaldmiðla ekki á réttan hátt. |
| 552226 | Úrvinnsla viðburðar lokar og enduropnar áætlanir mörgum sinnum fyrir einn viðburð  | Vandamál leyst þar sem starfsmaður er í mörgum lögaðilum og viðburður á sér stað, færsla viðburðar verður til fyrir alla lögaðilana sem starfsmaðurinn er í. Við úrvinnslu á viðburðum verður að velja lögaðilann sem á að vinna. Úrvinnslureglan takmarkar sig hins vegar ekki við þennan lögaðila. Þess í stað sér hún um úrvinnslu fyrir alla lögaðila og lokar og enduropnar áætlanirnar í völdum lögaðila. Þessi aðgerð gerir viðburði kleift að vinna úr viðburði mörgum sinnum í sama lögaðilanum, sem leiðir til þess að hver áætlun sem verður fyrir áhrifum viðburðarins er lokuð/enduropnuð mörgum sinnum. |
| 518064 | Aðeins einn aðili er valinn í gjaldgengri áætlun þegar fleiri en einn er merktur sem sjálfgefinn fulltrúi | Vandamál lagað þar sem margir sjálfgefnir fulltrúar eru sjálfkrafa valdir í gjaldgengum áætlunum. Einnig er hægt að tilnefna aðalrétthafa fyrir persónulegan tengilið. Aðalrétthafi er sýndur sem 100% í gjaldgengri áætlun þegar margir rétthafar eru til staðar. |
| 552365 | BYOD-útflutningsverk takast ekki eftir að uppfært var í verkvangsuppfærslu 40 | Vandamál lagað þar sem BYOD-útflutningar takast ekki eftir að verkvangsuppfærsla 40 er notuð í umhverfinu. |
| 547123 | Takmarka fjölda verka sem spurst er fyrir um í verkefnalista stjórnborðsins | Fjöldi verka sem birtast í verkefnalistanum er takmarkast nú við 15 til að laga vandamál með afköst út af of mörgum verkum sem reynt var að hlaða inn. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks | [Yfirlit stjórnanda milli fyrirtækja um leyfi til starfsfólks](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Grunnstilla færibreytur leyfis og fjarvista](./hr-leave-and-absence-parameters.md) |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum fyrirtækis | [Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum fyrirtækis](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Takmörkun á breytingu persónuupplýsinga](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Hæfni sem yfirmaður færir inn fyrir starfsmenn sína getur verið sjálfkrafa samþykkt af verkferlinu | Væntanlegt. |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Uppfærsla hugtaka fyrir Microsoft Dataverse

Tekur gildi í nóvember 2020, Common Data Service hefur verið endurnefnt [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Frekari upplýsingar er að finna í [opinberri tilkynningu](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) á Power Apps blogginu. Með þessari nafnabreytingu hafa nokkur hugtök í Dataverse verið uppfærð. Sem dæmi er *eining* núna *tafla* og *svæði* er núna *dálkur*. Frekari upplýsingar eru í [Uppfærslur hugtaka](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Í þessari útgáfu hafa hugtök sem tengjast samþættingu Dynamics 365 Human Resources við Dataverse verið uppfærð í öllu forritinu til að endurspegla þessar breytingar. Til dæmis er skjámyndin **Common Data Service samþætting** orðin **Microsoft Dataverse samþætting**.

Frekari upplýsingar um samþættingu Dynamics 365 Human Resources við Microsoft Dataverse er að finna í [Grunnstilla Microsoft Dataverse samþættingu](./hr-admin-integration-common-data-service.md) og [Grunnstilla Microsoft Dataverse sýndartöflur](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Uppfærist í þjónustuuppsetningu

Frá og með 22. febrúar 2021 útgáfunni munum við breyta uppsetningu á uppfærslu fyrir svæðisbundna þjónustu okkar. Breytingarnar fela í sér að snúa röðinni þar sem svæði fá uppfærslur fyrir Human Resources-þjónustuna og leiðréttingar á biðtíma milli uppfærslustiga. Þessar breytingar færa okkur nær öruggum uppsetningaraðferðum (SDP) til að auka stöðugleika, gæði og stuðning við þjónustuna.

Við fylgjumst áfram með tveggja vikna tíðni á uppsetningum. Hins vegar gætu viðskiptavinir tekið eftir því að uppfærslur eru yfirleitt gerðar á umhverfum Human Resources á öðrum degi í tveggja vikna lotunni en í fyrri útgáfum.

Frekari upplýsingar um uppfærsluferlið er að finna í [Uppfærsluferli](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]