---
title: Auður listi yfir skattaeiginleika í færibreytum skattaútreiknings
description: Í þessari grein er útskýrt hvernig á að úrræðaleita vandamál þar sem listinn yfir skattaeiginleika á færibreytusíðu skattaútreiknings er auður.
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
ms.openlocfilehash: 0d9286ec313a270da86181ff80ddfd690a757c9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869953"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Auður listi yfir skattaeiginleika í færibreytum skattaútreiknings

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>Einkenni

Þú hefur gefið út eiginleika í Regulatory Configuration Service (RCS) svo að þú getir notað hann í Microsoft Dynamics 365 Finance. Þegar þú opnar Finance skaltu hins vegar fara í **Skattur** \> **Uppsetning** \> **Skattaskilgreining** \> **Færibreytur skattaútreiknings** og reyna að velja gildi í reitnum **Uppsetningarheiti eiginleika**, listinn yfir gildi er tómur.

## <a name="reason"></a>Ástæða

Þetta vandamál kemur yfirleitt upp vegna þess að Finance- og RCS-umhverfið eru ekki undir sama leigjanda.

### <a name="rcs-tenant"></a>RCS leigjandi

Fylgdu þessum leiðbeiningum til að finna auðkenni RCS-leigjandans.

1. Afritaðu alla RCS-vefslóðina. Til dæmis gæti vefslóðin verið `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Opna InPrivate-vafraglugga, límdu RCS-vefslóðina í veffangastikuna og veldu **Færslulykilinn**. Þér er vísað á innskráningarsíðuna þar sem finna má auðkenni RCS-leigjanda. Ef vefslóð innskráningarsíðunnar er til dæmis `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` er auðkenni leigjanda upplýsingarnar sem birtast eftir `https://login.microsoftonline.com/` eða **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Leigjandakenni Finance-umhverfis

Fylgdu sömu skrefum og þú fórst eftir til að finna RCS-leigjandann. Hins vegar skaltu afrita og líma alla vefslóð Finance-umhverfisins í staðinn fyrir alla RCS-vefslóðina.

## <a name="resolution"></a>Upplausn

Ef auðkenni leigjandanna tveggja er mismunandi ertu að lenda í vandamálinu sem lýst er í þessari grein. Ef þau eru eins gætir þú lent í ótengdu vandamáli. Í þessu tilfelli mælum við með því að þú hafir samband við þjónustuver Microsoft.

### <a name="solution-1"></a>Lausn 1

Skráðu RCS umhverfið þitt á sama leigutaka og Finance umhverfið þitt er skráð inn til. Síðan skaltu búa til og birta skattaeiginleika.

### <a name="solution-2"></a>Lausn 2

Deildu skattaeiginleikanum með Finance-leigjandanum í RCS.

1. Í RCS skal fara í **Altækir eiginleikar** \> **Skattaútreikningur**.
2. Veldu eiginleikann til að deila og síðan í flipanum **Fyrirtæki** skal velja **Deila með**.
3. Í reitinn **Lénsheiti fyrirtækis** skal færa inn heiti. Til dæmis skal færa inn **contoso.onmicrosoft.com**.
4. Veldu **Deila**.

![Deildu með fellilista utanaðkomandi fyrirtækis.](media/ShareTaxFeature.png)
