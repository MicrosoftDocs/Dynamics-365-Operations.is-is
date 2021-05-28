---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources 22. mars 2021
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 22. mars 2021.
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 609b70fb2dfa3f3b2a1746392984108d7ac195c4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019275"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Hvað er nýtt eða breytt í Dynamics 365 Human Resources 22. mars 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er lýst nýjum, breyttum eða væntanlegum eiginleikum í Dynamics 365 Human Resources.

Frekari upplýsingar um uppfærsluferlið okkar og áætlun er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).

Frekari upplýsingar um nýja eiginleika og hvenær þeir verða aðgengilegir almenningi er að finna í [Yfirlit yfir Dynamics 365 Human Resources Losunarbylgju 1 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Í þessari útgáfu

Þessi útgáfa felur í sér eftirfarandi nýja eiginleika og villuleiðréttingar. Breytingar eiga við um byggingarnúmer 8.1.4049.

### <a name="new-features"></a>Nýjar aðgerðir

Eftirfarandi eiginleikar eru almennt aðgengilegur með þessari útgáfu.

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Valkostur til að þvinga afturköllun og endurstilla fasta runuvinnslu (560976) | NA | [Endurstilla fastar runuvinnslur](./hr-admin-troubleshooting-batch-execution.md) |
| Minniháttar UX-uppfærslur til að búa til nýja fríðindaáætlun (419941) | NA | [Búa til fríðindaáætlun](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Villuleiðréttingar

Eftirfarandi villuleiðréttingar eru innifaldar í þessari útgáfu.

> [!NOTE]
> Markmiðið okkar er að koma þessum upplýsingum til þín eins fljótt og auðið er. Við gætum uppfært þetta efnisatriði til að hafa með leiðréttingar á villum sem slæddust með smíðinni eftir að þetta efnisatriði var gefið út upphaflega.

| Númer úthreyfingar | Úthreyfing |  lýsing |
| --- | --- | --- |
| 554239 | Afkastaumbætur fyrir einingar sem tengjast **BusinessProcessTaskAssignment** töflunni | Bætt afköst eininga sem tengjast **BusinessProcessTaskAssignment** töflunni með því að bæta við tillögum að atriðaskrá við töfluna. |
| 566061 | Fjarlægja V2 varakóða eininga úr samstillingu að næturlagi | Fjarlægja V2 varakóða eininga úr Dataverse samstillingu að næturlagi. Varakóðinn er ekki lengur nauðsynlegur og kemur í veg fyrir því að síaðar samstillingar virki sem skyldi. Breytingin eykur samræmi við Dataverse samstillingu gagna. |
| 538024 | Fríðindaáætlanir starfskrafts > Fjarlægja villu við útskráningu | Lagfærði villu við að fjarlægja greiðsluferil fyrir valkost fríðindaáætlunar í eyðublaði fyrir fríðindi starfskrafts. |
| 557965 | **Fríðindi** vinnusvæði: **Virkir viðburðir** ætti alltaf að vera sýnilegur í **Tenglar** hlutanum | Lagfært vandamál þþegar **Virkir viðburðir** tengill var sýnilegur í **Tenglar** hlutanum en villa kom upp þegar reynt var að skoða ef valkosturinn **(Forskoðun) Vinnusvæði fríðindastjórnunar** var ekki virkur. Frekari upplýsingar um virkjun vinnusvæðis má finna í [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md). |
| 556672 | Ekki er hægt að vinna úr uppsöfnun fyrir starfsmann sem er hættur þegar **Einföld starfsmannafærsla** er virk í eiginleikastjórnun | Valkostinum til að safna upp leyfi og fjarvistum hefur verið bætt við **Fleiri valkostir** undir **Starfsferill** fyrir starfsmenn þegar **Einföld starfsmannafærsla** er virk í eiginleikastjórnun. |
| 562656 | **SysRecordChangeLogValidTimeState** valmyndaratriðið ætti að vera innifalið í öryggisréttindum og viðbót við **SystemExternalBasicMaintain** öryggisregluna | Stjórnandahlutverkum sem ekki eru með kerfisstjórnun vantaði í **Skoða breytingar** hnappinn á skjámyndum gagnastjórnanda. |
| 505989 | Úrvinnsla virkra viðburða: Breyting á réttindum birtist ekki rétt vegna notaðrar dagsetningar | Lagfærði vandamál þar sem breyting á vinnslu réttinda var háð upphafsdegi stöðu og ekki eingöngu núverandi stöðu. |
| 562286 | Uppsögn starfskrafts sendir margar uppfærslur til Dataverse | Þegar starfskrafti er sagt upp er fleiri en ein uppfærsluaðgerð send til Dataverse, sem leiðir til tveggja uppfærslutilkynninga fyrir sömu breytinguna. Þetta getur valdið mörgum kveikjum ef Power Automate flæðið er stillt á að kveikja á því úr aðgerðinni. |
| 527340 | „Unrepresentable DateTime“ villa birtist þegar leyfi og fjarvistir eru opnaðar | Þegar leyfi og fjarvistarskráning er valin birtist villan ekki lengur. |
| 561663 | Auka biðtímabil fyrir úthlutun til klasa | Bættur stöðugleiki og úthlutun með uppfærslum á úthlutun til klasa. |
| 486129 | Ekki er hægt að breyta sérsniðnum reitum í **Stöður > Stjórna breytingum** | Lagfærði vandamál þar sem ekki var hægt að breyta sérsniðnum reitum í **Hafa umsjón með breytingum** flipanum **Stöður**. |

## <a name="in-preview"></a>Í kynningarútgáfu

Eftirfarandi nýir eiginleikar eru í kynningarútgáfu. Nánari upplýsingar um hvernig eigi að kveikja og slökkva á eiginleikum er að finna í [Stjórna eiginleikum](hr-admin-manage-features.md).

| Eiginleiki | Útgáfuáætlun | Fylgiskjöl |
| --- | --- | --- |
| Vinnusvæði fríðindastjórnunar | [Vinnusvæði fríðindastjórnunar (forskoðun)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Vinnusvæði fríðindastjórnunar](hr-benefits-management-workspace.md) |
| Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum fyrirtækis | [Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum fyrirtækis](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Takmörkun á breytingu persónuupplýsinga](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Væntanlegt

| Eiginleiki | Upplýsingar |
| --- | --- |
| Hæfni sem yfirmaður færir inn fyrir starfsmenn sína getur verið sjálfkrafa samþykkt af verkferlinu | Væntanlegt. |

Fyrir ítarlegan lista yfir áætlaða eiginleika og áætlaðar útgáfur þeirra skal skoða [Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Sjá einnig

[Nýjungar eða breytingar í Mannauði](hr-admin-whats-new.md)</br>
[Yfirlit yfir Dynamics 365 Human Resources 2021 losunarbylgju 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Uppfærsluferli](hr-admin-setup-update-process.md)</br>
[Vinna með eiginleika](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]