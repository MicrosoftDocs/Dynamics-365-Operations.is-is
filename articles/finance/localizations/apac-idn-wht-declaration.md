---
title: Staðgreiðsluskattskýrsla fyrir Indónesíu
description: Þessi grein útskýrir hvernig á að stilla og búa til staðgreiðsluskýrslu fyrir Indónesíu.
author: sndray
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8acd9442ff4f0b7c19e3b4fcf211acce002e43d5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883182"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Staðgreiðsluskýrsla fyrir Indónesíu (ID-00005)

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp og búa til PPH staðgreiðsluskrána sem lögaðilar í Indónesíu nota til að tilkynna staðgreiðsluviðskipti í e-Bupot forritinu.

Skattyfirvöld í Indónesíu (DGT) ákvarðar að skattskyldir frumkvöðlar (PKP) sem eru skráðir hjá KPP Pratama sem staðgreiðendur/innheimtufé tekjuskatts (PPh) 23. gr. og/eða 26. gr., verða að tilkynna tekjuskattsskýrslu greinar 23 og 26 rafrænt með því að nota e-Bupot forritið. 

- **23. gr** – Skýrslan inniheldur allar staðgreiðslufærslur frá söluaðilum þar sem lands-/svæðiskóði aðal heimilisfangs er kóði fyrir Indónesíu.
- **26. gr** – Skýrslan inniheldur allar staðgreiðslufærslur frá söluaðilum þar sem lands-/svæðiskóði aðal heimilisfangs er ekki kóðinn fyrir Indónesíu.

## <a name="prerequisites"></a>Forkröfur

- Aðal heimilisfang lögaðilans verður að vera í Indónesíu.
- Í **Eiginleikastjórnun** vinnurými, the **Alþjóðleg staðgreiðsluskattur** eiginleiki verður að vera virkur. Nánari upplýsingar um hvernig á að virkja eiginleika er að finna í [Yfirlit eiginleikastjórnunar.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="download-electronic-reporting-configurations"></a>Hlaða niður skilgreiningum rafrænnar skýrslugerðar

Myndun innflutningsskrár er byggð á rafrænum skýrslum (ER) stillingum. Frekari upplýsingar um möguleika og hugmyndir á bak við stillanlega skýrslugerð er að finna í [Rafræn skýrslugerð](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Fyrir framleiðslu- og notendaviðurkenningarprófun (UAT) umhverfi skaltu fylgja leiðbeiningunum í [Hladdu niður rafrænum skýrslustillingum frá Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Til að búa til innflutningsskrána skaltu hlaða upp eftirfarandi stillingum úr geymslunni:

- **Skattframtalslíkan.version.93.xml** eða síðari útgáfu
- **Skattframtalslíkan mapping.version.93.153.xml** eða síðari útgáfu
- **Hvaða PPh skema innflutningur (ID).version.93.14** eða síðari útgáfu

## <a name="set-up-general-ledger-parameters"></a>Setja upp færibreytur fyrir Fjárhag

1. Fara til **Skattur** \> **Uppsetning** \> **Fjárhagsfæribreytur**.
2. Á **Staðgreiðsla skatts** flipa, í **Hvaða yfirlýsingu snið kortlagning** reit, veldu **Hvaða PPh skema innflutningur (ID)**. 
3. Fara til **Skattur** \> **Uppsetning** \> **Staðgreiðsla skatts** \> **Tekjutegundir staðgreiðsluskatts** að setja upp **Kóði Bukti Potong** tegund staðgreiðslu skatttekju og úthluta síðan kóðunum á tengda staðgreiðsluflokka vöru. Kóðarnir eru nauðsynlegir til að búa til samþættingarskrána með því að nota e-Bupot forritið. 

## <a name="generate-the-withholding-import-file"></a>Búðu til staðgreiðsluinnflutningsskrána

Ferlið við að undirbúa og búa til e-Bupot skrána fyrir tiltekið tímabil byggist á staðgreiðslufærslum sem voru bókaðar við uppgjör eða eftirgreiðslu skattavinnu.

Fylgdu þessum skrefum til að búa til skrána.

1. Fara til **Skattur** \> **Yfirlýsingar** \> **Staðgreiðsla skatts** \> **PPH innflutningsskrá e-bupot 23 og 26**.
2. Veldu „frá“ dagsetningu og „til“ dagsetningu fyrir skýrsluna og veldu síðan uppgjörstímabilið.
3. Sláðu inn færsludagsetningu og veldu síðan **Allt í lagi**.
4. Veljið tungumálið. Allar skýrslur eru þýddar á bandaríska ensku (**en-okkur**) og indónesíska (**kt**).
5. Veldu viðskiptategundina og sláðu síðan inn ávísana- og skjalnúmerið. 
6. Athugaðu hvort skýrslan hafi verið undirrituð af stjórnanda. Þessar upplýsingar koma fram í skránni. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
