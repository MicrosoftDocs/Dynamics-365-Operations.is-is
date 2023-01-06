---
title: Staðgreiðsluskattskýrsla fyrir Indónesíu
description: Þessi grein útskýrir hvernig á að skilgreina og mynda staðgreiðsluskattsskýrslu fyrir Indónesíu.
author: AdamTrukawka
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.search.scope: ''
ms.openlocfilehash: 732db563532ebc46c7b9fc69c2aaa128640084f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282436"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Staðgreiðsluskattskýrsla fyrir Indónesíu (ID-00005)

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að setja upp og búa til PPH staðgreiðsluskattsskrá sem lögaðilar í Indónesíu nota til að tilkynna staðgreiðslufærslur í e-Bupot forritinu.

Skattyfirvöld í Indónesíu (DGT) ákveða að skattskyldir frumkvöðlar (PKP) sem skráðir eru hjá KPP Pratama sem skattvörsluaðilar/innheimtuaðilar tekjuskatts (PPh) samkvæmt 23. og/eða 26. gr. verði að tilkynna rafrænt um tekjuskattskil samkvæmt 23. og 26. gr. með því að nota forritið e-Bupot. 

- **23. grein** – Skýrslan inniheldur allar staðgreiðslufærslur frá lánardrottnum þar sem lands-/svæðiskóði aðalaðsetursins er kóði fyrir Indónesíu.
- **26. grein** – Skýrslan inniheldur allar staðgreiðslufærslur frá lánardrottnum þar sem lands-/svæðiskóði aðalaðsetursins er ekki kóði fyrir Indónesíu.

## <a name="prerequisites"></a>Forkröfur

- Aðalaðsetur lögaðilans verður að vera í Indónesíu.
- Á vinnusvæðinu **Eiginleikastjórnun** þarf að virkja eiginleikann **Altækur staðgreiðsluskattur**. Nánari upplýsingar um hvernig á að virkja eiginleika er að finna í [Yfirlit eiginleikastjórnunar.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="download-electronic-reporting-configurations"></a>Hlaða niður skilgreiningum rafrænnar skýrslugerðar

Gerð innflutningsskráar byggir á skilgreiningum rafrænnar skýrslugerðar. Frekari upplýsingar um möguleika og hugmyndir á bak við stillanlega skýrslugerð er að finna í [Rafræn skýrslugerð](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Fyrir umhverfi framleiðslu og samþykkisprófun notanda skal fylgja leiðbeiningum í [Hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Til að búa til innflutningsskrána, hladdu upp eftirfarandi stillingum úr geymslunni:

- **Skattskýrsla model.version.93.xml** eða nýrri útgáfa
- **Skattskýrslulíkan mapping.version.93.153.xml** eða nýrri útgáfa
- **WHT PPh skemainnflutningur (ID).version.93.14** eða nýrri útgáfa

## <a name="set-up-general-ledger-parameters"></a>Setja upp færibreytur fyrir Fjárhag

1. Farið í **Skattur** \> **Uppsetning** \> **Færibreytur fjárhags**.
2. Í flipanum **Staðgreiðsluskattur**, í reitnum **Vörpun skýrslusniðs fyrir WHT**, skal velja **WHT PPh skemainnflutning (ID)**. 
3. Farðu í **Skattur** \> **Uppsetning** \> **Staðgreiðsluskattur** \> **Tekjugerðir staðgreiðsluskatts** til að setja upp tekjugerðina **Kode Bukti Potong** fyrir staðgreiðsluskatt og síðan úthlutað kóðum á tengda staðgreiðsluskattflokka vöru. Kóðarnir eru nauðsynlegir til að búa til samþættingarskrá með því að nota e-Bupot forritið. 

## <a name="generate-the-withholding-import-file"></a>Útbúa innflutningsskrá staðgreiðslu

Ferlið við að undirbúa og senda inn e-Bupot skrána fyrir tiltekið tímabil er byggt á staðgreiðsluskattsfærslum sem bókaðar voru við uppgjörs- eða bókunarvinnu skattgreiðslu.

Fylgdu þessum skrefum til að útbúa skrána:

1. Farðu í **Skattur** \> **Skýrslur** \> **Staðgreiðsluskattur** \> **PPH-innflutningsskrá e-bupot 23 og 26**.
2. Veldu „frá“ dagsetningu og „til“ dagsetningu fyrir skýrsluna og veldu síðan jöfnunartímabilið.
3. Færið inn færsludagsetningu og veljið svo **Í lagi**.
4. Veljið tungumálið. Allar skýrslur eru þýddar á bandaríska ensku (**en-us**) og indónesísku (**id**).
5. Veljið tegund viðskipta og sláið svo inn ávísun og skjalanúmer. 
6. Athugaðu hvort stjórnandinn hafi undirritað skýrsluna. Þessar upplýsingar birtast í skránni. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
