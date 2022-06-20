---
title: Uppsetning öryggis fyrir Power BI-efni kostnaðarbókhaldsgreiningar
description: Þessi grein útskýrir hvernig þú getur útbreitt aðgangsstigsöryggið í Kostnaðarbókhaldi yfir í línustigsöryggi í Microsoft Power BI.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc4d72fb688733b9c1547346c520dd9d77a3b12f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883687"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Uppsetning öryggis fyrir Power BI-efni kostnaðarbókhaldsgreiningar

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig þú getur útbreitt aðgangsstigsöryggið í Kostnaðarbókhaldi yfir í línustigsöryggi í Microsoft Power BI. Þessi virkni hjálpar til við að tryggja að notendur sjá aðeins Power BI gögn sem þeir fá aðgang að.

## <a name="overview"></a>Yfirlit

**Greining á kostnaðarbókhaldi**  Microsoft Power BI efni notar Power BI öryggi á línustigi til að takmarka aðgang notenda. Öryggi er byggt á aðgangsstigi stigveldis fyrirtækis sem eru sett upp í færibreytum kostnaðarbókhalds. Nánari upplýsingar um **Greiningu á kostnaðarbókhaldi** Power BI innihald er að finna í [Power BI-efni greiningar á kostnaðarbókhaldi](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Uppsetning
Til að yfirfæra öryggi á aðgangsstigi til Power BI þarf eigandi Power BI efnis að fylgja eftirfarandi skrefum.

> [!NOTE]
> Notandinn sem gefur út **Greiningar á kostnaðarbókhaldi** Power BI-efni verður sjálfvirkt eigandi. Aðeins eigandi getur sett upp öryggi í Power BI. Þar að auki, þar til að eigandi bætir við öðrum notendum á PowerBI.com getur enginn nema eigandinn séð hvaða gögn í **Greiningar á kostnaðarbókhaldi** Power BI efni.

1. Birta Power BI í skilgreiningarskránni.
2. Skráðu þig inn á PowerBI.com.
3. Finna gagnamengi fyrir **Greiningar á kostnaðarbókhaldi** Power BI efni.
4. Opnaðu öryggissíðuna.

    ![Opna öryggissíðuna.](./media/CA-picture-1.png)

5. Hlutverkið **Stjórnborð kostnaðarhlutar** er þegar stofnað. Bæta við öðrum aðilum sem eru hluti af stigveldisskipan aðgangsstigs kostnaðarbókhalds.

    ![Bæta við meðlimum.](./media/CA-picture-2.png)

Notendur sem er bætt við hlutverkið **Stjórnborð kostnaðarhlutar** sjá aðeins gögnin sem þeir hafa heimild til að sjá, samkvæmt skilgreiningu í stigveldisskipan aðgangsstigs kostnaðarbókhalds.

> [!NOTE]
> Athugasemd: Öryggi á línustigi gildir í reitum og skýrslum sem eru innfelld úr Power BI.

## <a name="updating-security"></a>Uppfæri öryggi
Ef uppfærslur eru gerðar á öryggi á aðgangsstigi í kostnaðarbókhaldi, og þú vilt að Power BI endurspegli þessar uppfærslur, þarf að uppfæra einingaverslun fyrir **Greiningar á kostnaðarbókhaldi** Power BI efni. Eftir að þú lýkur uppfærslu á einingaverslun verður að uppfæra gervingar á PowerBI.com. Nánari upplýsingar um hvernig á að gera uppfærslu á einingaverslun í [Power BI samþætting við einingaverslun](power-bi-integration-entity-store.md#update-entity-store). Eigandi **Greining kostnaðarbókhalds** Power BI-efnis verður einnig að gera uppfærslu einingaverslunar ef nýir notendur fá aðgang að stigveldisskipan. Þar að auki verður eigandi að bæta við nýjum notendum við hlutverk **Stjórnborð kostnaðarhlutar** á PowerBI.com, svo að öryggi á línustigi sé notað fyrir þá.

## <a name="disabling-security"></a>Afvirkjun öryggis
Gerum ráð fyrir að fyrirtækið vilji takmarka gagnaaðgengi. Ef af einhverri ástæðu, öryggi færibreyturnar verður óvirkt þegar kostnaðarbókhald er keyrt, verður eigandinn að bæta notendum við í hlutverkið **Kostnaðarbókari** í Power BI í staðinn. Ef öryggislyklinum er breytt úr virkri stöðu í óvirka stöðu, er góð hugmynd að fjarlægja notendur úr hlutverkinu **Stjórnborð kostnaðarhlutar**. Og öfugt ef þú endurvirkjar öryggisstillingar. Notendur geta tilheyrt báðum hlutverkum. Sameiginlegar aðgangur er sameining beggja hlutverka. Í tilfelli **Greining á kostnaðarbókhaldi** Power BI efnis hafa notendur með sameiginlegan aðgang óheftan gagnaaðgang. Ef markmiðið er að nota takmarkaðan aðgang verður að úthluta notendum eingöngu á hlutverk **Stjórnborð kostnaðarhlutar**. Þessar uppfærslur á öryggi á línustigi taka strax gildi. Notendur sem verða fyrir áhrifum ættu að endurræsa vafra sína.

## <a name="additional-resources"></a>Frekari upplýsingar
Til að fræðast nánar um Power BI öryggi á línustigi, sjá [Stjórna öryggi líkansins í Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]