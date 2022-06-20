---
title: PowerBI.com lausn fjárhagslegrar frammistöðu
description: Þessi grein lýsir fjárhagslegri afkomu PowerBI.com lausninni.
author: kweekley
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcbe41d113ee41734020546388851afb7fc27bbf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910416"
---
# <a name="financial-performance-powerbicom-solution"></a>PowerBI.com lausn fjárhagslegrar frammistöðu

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Þessi PowerBI.com lausn hefur verið úrelt eins og skjalfest er í [Fjarlægðir eða úreltir eiginleikar fyrir Finance and Operations](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Þessi grein lýsir **Fjárhagsleg afkoma** PowerBI.com lausn. Það útskýrir yfirlitið og skýrslurnar sem eru með og veitir upplýsingar um gagnalíkanið og einingarnar sem voru notaðar til að smíða lausnina.

## <a name="main-account-setup"></a>Uppsetning aðallykils
Þar sem fyrr vilja upphæðir skulda og tekjur að birtast sem jákvætt upphæðir í skýrslur er uppsetning aðallykla mikilvæg. Til að þessir aðallyklar birtast sem jákvætt upphæðir verður aðallykilgerð að vera stillt á **Skuldir** eða **Tekjur**. Þegar þessar gerð lykils er notað verður skýrslugerð í gegnum Power BI snúa við merkjum og sýna upphæðir sem jákvætt.

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a>Yfirlit og skýrslur sem eru í PowerBI.com lausninni
Mælaborð inniheldur samantekna gagnareiti sem byggjast á undirliggjandi skýrslum. Hver reitur inniheldur samanteknar upplýsingar fyrir núverandi ár yfir öll fyrirtæki í samstæðu. Hér eru sum af reitir:

- Innlausn
- Heildartekjur á þessu ári
- Heildarkostnaður á þessu ári
- Nettótekjur þessa árs
- Lausafjárhlutfall
- Heildarkostnaður á þessu ári eftir tegund
- Veltufjárhlutfall
- Skuld heildareigna
- Raunverulegt miðað við spáðar Tekjur
- Reikningsfærðar tekjur á þessu ári
- Hlutfall rekstrargjalda á þessu ári
- Hagnaðarhlutfall þessa árs
- Rauntölur kostnaðar samanb. v. áætlun - öll fyrirtæki

Hver reitir fá stuðning frá skýrslu. Þessar skýrslur innihalda bæði gröf og töflur sem veita frekari upplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                      | Í skýrslunni koma fram eftirfarandi upplýsingar: |
|-----------------------------|--------------------------------------|
| Greining reiðufés               | Reiðufé eftir lögaðila, reiðufé eftir fjórðungi, samtals reiðufé, og reiðufé eftir lyklum<blockquote>[!NOTE] Reiðufé eftir fjórðungi upplýsingar innihalda ekki upphafsstöður á samtölu fyrir fyrsta ársfjórðung. Hún sýnir samtala nýrra færsla sem er bóka í hverjum fjórðungi.</blockquote> |
| Greining veltufjárhlutfalls      | Veltufjárhlutfall eftir lögaðila, veltufjárhlutfall eftir ársfjórðungi, og stöður fyrir veltufjármuni og skammtímaskuldir |
| Greining lausafjárhlutfalls        | Lausafjárhlutfall eftir lögaðila, lausafjárhlutfall eftir ársfjórðungi, og stöður fyrir reiðufé, viðskiptakröfur og skammtímaskuldir |
| Greining kostnaður seldra vara | Kostnaður seldra vara (COGS) eftir lögaðila, kostnaður seldra vara þessa árs og síðasta árs eftir ársfjórðungi, COGS gagnvart sölu eftir lögaðila, heildar COGS, og COGS gagnvart söluhlutfalli. |
| Greining veltufés    | Veltufé eftir lögaðila, veltufé eftir ársfjórðungi, veltufjármunir, skammtímaskuldir, og heildar veltufé. |
| Greining eigna og skulda     | Ávöxtun heildareigna og skuldir gagnvart heildareignum eftir lögaðila, skuld gagnvart heildareignum og ávöxtun heildareigna yfirstandandi ársfjórðungs, eignir og skuldir. |
| Greining hagnaðarhlutfalls      | Raunverulegt og áætlað hagnaðarhlutfall eftir lögaðila, hagnaðarhlutfall eftir ársfjórðingi, prósenta hagnaðarhlutfalls, og hagnaðarhlutfall. |
| Greining hreinna tekja         | Raunverulegar á áætlaðar hreinar tekjur eftir lögaðila, hreinar tekjur þessa og síðasta árs og útgjöld gagnvart prósentu hreinna tekja |
| Greining hagnaðar           | Raunverluegar og áætlaðar tekjur fyrir vexti og skatta (EBIT) eftir lögaðila, Rekstrarhagnaður (EBIT) þessa árs og síðasta árs, útgjöld gagnvart tekjuhlutfalli, og raunverulegur og áætlaðar kostnaðar gagnvart tekjum. |
| Greining tekja            | Heildartekjur, raunverulegar og áætlaðar heildartekjur eftir lögaðila, heildartekjur þessa árs og síðasta árs, fjárhagsfrávik eftir lögaðila og heildartekjur þessa tímabils og síðasta tímabils. |
| Greining kostnaðar            | Heildarupphæð kostnaðar, raunveruleg áætlun heildarkostnaðar eftir lögaðila, raunveruleg og áætluð heildarkostnaður eftir ársfjórðingu, heildarútgjöld eftir tegund lykils, og hlutfall rekstrargjalda. |
| Greining reikningsfærðra tekja     | Heildarviðskiptakröfur, heildarviðskiptakröfur eftir lögaðila, heildarviðskiptakröfur eftir ársfjórðungi, og stöður fyrir lykla viðskiptakrafna.<blockquote>[!NOTE] Upplýsingarnar innihalda ekki upphafsstöður fyrir fjárhagslykla viðskiptakrafna. Þær sýnir samtala nýrra færsla sem er bóka viðskiptakröfur.</blockquote> |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Eftirfarandi einingar voru notaðar sem grunnurinn á PowerBI.com lausn **Fjárhagslegrar frammistöðu**:

**Einingar samantekinna gagna**

- **GeneralLedgerActivities** – Þessi eining leggur saman fjárhagsstöður eftir tegund lykla.
- **BudgetActivities** – Þessi eining leggur saman staða fjárhagsáætlunar eftir tegund lykla.

**Gagnaeiningar**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Fjárhagur
- ChartofAccounts

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Reiknaðar mælieiningar eru notaðar til að stofna reiknaðar ráðstafanir til að reikna út afkastavísar (KPI ) og skýrslur sem eru notaðar í efninu. Sjálfgefið er að efnið færir inn gögn fyrir síðustu þrjú árin og eitt komandi ár. Til að hafa viðbótarútreikning með á skýrslur og mælaborð er hægt að breyta [Microsoft Excel vinnubók](/dynamics/s-e/). Þessi vinnubók er sjálfgefið gagnalíkan sem var notað til að stofna efnið.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]