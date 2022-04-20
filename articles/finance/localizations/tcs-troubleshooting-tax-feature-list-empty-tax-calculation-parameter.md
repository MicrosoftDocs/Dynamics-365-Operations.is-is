---
title: Auður listi yfir skattaeiginleika í færibreytum skattaútreiknings
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem listi yfir skatteiginleika á síðunni Skattreikningsfæribreytur er tómur.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: ef8158c2ada18e7d132eebbedef559b3f80ab19f
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612290"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Auður listi yfir skattaeiginleika í færibreytum skattaútreiknings

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>Einkenni

Þú hefur birt eiginleika í Regulatory Configuration Service (RCS), svo að þú getir notað hann í Microsoft Dynamics 365 Fjármál. Hins vegar, þegar þú opnar Finance, farðu til **Skattur** \> **Uppsetning** \> **Skattstilling** \> **Skattreikningsbreytur**, og reyndu að velja gildi í **Heiti eiginleikauppsetningar** reitinn er gildislistinn tómur.

## <a name="reason"></a>Ástæða

Þetta vandamál kemur venjulega upp vegna þess að fjármálaumhverfið þitt og RCS umhverfið eru ekki undir sama leigjanda.

### <a name="rcs-tenant"></a>RCS leigjandi

Fylgdu þessum skrefum til að finna auðkenni RCS leigjanda þíns.

1. Afritaðu RCS vefslóðina í heild sinni. Til dæmis gæti vefslóðin verið `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Opnaðu InPrivate vafraglugga, límdu RCS vefslóðina inn í heimilisfangastikuna og veldu síðan **Koma inn**. Þér er vísað á innskráningarsíðuna, þar sem þú getur fundið auðkenni RCS leigjanda. Til dæmis, ef slóð innskráningarsíðunnar er`https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d`, leigjanda auðkenni eru upplýsingarnar sem birtast á eftir`https://login.microsoftonline.com/`, eða **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Auðkenni leigjanda í fjármálaumhverfi

Til að finna auðkenni leigjanda fyrir fjármálaumhverfið þitt skaltu fylgja sömu skrefum og þú fylgdir til að finna RCS leigjanda. Hins vegar, afritaðu og límdu alla vefslóð fjármálaumhverfisins þíns í stað RCS vefslóðarinnar í heild sinni.

## <a name="resolution"></a>Upplausn

Ef auðkenni leigjenda tveggja eru ólík, ertu að lenda í því vandamáli sem lýst er í þessu efni. Ef þau eru þau sömu ertu að lenda í ótengt vandamáli. Í þessu tilviki mælum við með því að þú hafir samband við þjónustudeild Microsoft.

### <a name="solution-1"></a>Lausn 1

Skráðu RCS umhverfið þitt inn á sama leigjanda og fjármálaumhverfið þitt er skráð inn á. Búðu síðan til og birtu skattaeiginleikann.

### <a name="solution-2"></a>Lausn 2

Deildu skattaeiginleikanum með Finance leigjanda í RCS.

1. Í RCS, farðu til **Hnattvæðingareiginleikar** \> **Skattútreikningur**.
2. Veldu eiginleikann sem á að deila og síðan á **Samtök** flipa, veldu **Deila með**.
3. Í **Lén stofnunarinnar** reit, sláðu inn nafn. Til dæmis, slá inn **contoso.onmicrosoft.com**.
4. Veldu **Deila**.

![Deila með ytri stofnun fellivalglugga.](media/ShareTaxFeature.png)
