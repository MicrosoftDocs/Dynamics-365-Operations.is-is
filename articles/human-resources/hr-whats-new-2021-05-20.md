---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 20. maí 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 20. maí 2021.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4519e90e19d0652f855999d1a73ca64777b53b53465d6065987afc1cf2494187
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731938"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 20. maí 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4189.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Verkvangsuppfærsla 10.0.18 (42) | -- | [Verkvangsuppfærslur fyrir útgáfu 10.0.18 á Finance and Operations forritum (maí 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Forrit Human Resources fyrir Microsoft Teams styður nú skilgreiningar á hálfum degi og möguleika á skiptingu dags. | -- | [Stjórna leyfisbeiðnum í Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Gefa út |  lýsing |
| --- | --- | --- |
| 583776 | Fjöldaskráning starfsmanna í leyfisáætlanir veldur villu vegna afritunar á færslu | Þessi villa hefur verið lagfærð í nýjustu útgáfu og skráningar í leyfisáætlanir ættu að ganga vel. |
| 582263 | Ekki er hægt að keyra lífsviðburði fyrir alla starfskrafta í einu | Þegar reiturinn **Starfsmaður** er skilinn eftir auður fyrir úrvinnslu á viðburði verður unnið úr öllum starfsmönnum. |
| 558383 | Aðalrétthafi ekki merktur sem 100% ef sjálfgefinn fulltrúi er ekki valinn | Villa hefur verið lagfærð þannig að notandi þarf aðeins að velja víxlhnapp aðalrétthafa.|
| 509404 | Greining á starfsmannafjölda deildar tekur ekki tillit til hreyfingar starfsmanna milli deilda |Greiningar hafa verið uppfærðar þannig að þær fela í sér tilfærslur starfsmanna milli deilda.|
| 579420 | Ekki ætti enn að vera hægt að frysta dálka í neteiginleikum | Eiginleikinn **Dálkar festir í hnitanetum**, sem er ekki í boði í Human Resources, var sýndur sem tiltækur í eiginleikastjórnun. Eiginleikinn var fjarlægður af listanum yfir eiginleika til að virkja. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Stuðningur við sérstillta reiti í hæfnireglum fríðindastjórnunar | [Stuðningur við sérstillta reiti fyrir vinnslu á hæfni](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Stilla hæfnisreglur](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Viðbætur á upplifun verkflæðis fyrir leyfi og fjarvistir | [Viðbætur á upplifun verkflæðis fyrir leyfi og fjarvistir](https://go.microsoft.com/fwlink/?linkid=2147528) | [Biðja um frí](hr-employee-self-service-request-time-off.md)|
| Virkja einfalda launasamþættingu (API fyrir launasamþættingu) | [Virkja einfalda samþættingu við launaveitu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Launasamþættingar-API](hr-admin-integration-payroll-api-introduction.md)|
| Endurskoðun færslu fyrir uppsafnað leyfi | - | [Endurskoðun færslu fyrir uppsafnað leyfi](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
|  Virkja fjarvistarstjóra til að stjórna fríi | [Virkja fjarvistarstjóra til að stjórna fríi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
