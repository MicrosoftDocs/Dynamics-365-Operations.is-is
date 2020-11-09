---
title: Leiðsögn fyrir uppsetningu tvöfaldra skrifa
description: Þetta efni lýsir atburðarásum sem eru studdar fyrir tvískipt skrifun.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088507"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a>Leiðsögn fyrir uppsetningu tvöfaldra skrifa

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Þú getur sett upp tvískipt samband milli Finance and Operations umhverfis og Common Data Service umhverfis.

+ **Finance and Operations umhverfi** býður upp á undirliggjandi verkvanginn fyrir **Finance and Operations forrit** (til dæmis Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Retail).
+ **Common Data Service Umhverfi** veitir undirliggjandi verkvang fyrir **forrit viðskiptavina** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Mannauður í Finance and Operations styður tengingu tvískiptra skrifa, en Dynamics 365 Human Resources-forritið gerir það ekki.

Skipulagið er mismunandi eftir áskrift og umhverfi.

+ Fyrir ný tilvik af forrit Finance and Operations hefst uppsetningin á tvískiptri tengingu í Microsoft Dynamics Lifecycle Services (LCS). Ef þú ert með leyfi fyrir Power Platform geturðu fengið nýtt umhverfi Common Data Service ef leigjandi þinn hefur ekki slíkt.
+ Fyrir núverandi tilvik forrita Finance and Operations hefst uppsetning tvískiptrar tengingar í umhverfi Finance and Operations.

Áður en þú ræsir tvírita í einingu er hægt að keyra fyrstu samstillingu til að meðhöndla fyrirliggjandi gögn á báðum hliðum Finance and Operations -forrita og Customer Engagement-forrita. Hægt er að sleppa upphaflegu samkeyrslunni ef ekki þarf að samstilla gögn á milli tveggja umhverfa.

Upphafleg samstilling gerir notanda kleift að afrita fyrirliggjandi gögn úr einu forriti í annað. Ýmsar mismunandi uppsetningaráætlanir eru eftir því hvaða umhverfi er þegar til staðar og hvaða gerð gagna er í umhverfi.

Eftirfarandi uppsetningaraðstæður eru studdar:

+ [Nýtt Finance and Operations -forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar](#new-new)
+ [Nýtt Finance and Operations -forritatilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar](#new-existing)
+ [Nýtt Finance and Operations -forritstilvik sem inniheldur gögn og nýtt tilvik fyrir forrit viðskiptavinar](#new-data-new)
+ [Nýtt Finance and Operations -forritstilvik sem inniheldur gögn og fyrirliggjandi tilvik fyrir forrit viðskiptavinar](#new-data-existing)
+ [Fyrirliggjandi Finance and Operations -forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar](#existing-new)
+ [Fyrirliggjandi Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Nýtt Finance and Operations forritstilvik og nýtt tilvik fyrir forrit viðskiptavinar

Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations -forriti sem inniheldur engin gögn og nýs tilviks um þjónsforrit skal fylgja skrefunum í [Uppsetning tvöfaldra skrifa úr Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingarinnar er lokið fara eftirfarandi aðgerðir sjálfkrafa fram:

- Nýtt, tómt umhverfi Finance and Operations er veitt.
- Nýju, auðu tilviki af forriti viðskiptavinar er úthlutað, þar sem CRM úrvalslausnin er uppsett.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Einingakort eru virk fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Nýtt Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar

Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations -forriti sem inniheldur engin gögn og fyrirliggjandi tilvik um þjónsforrit skal fylgja skrefunum í [Uppsetning tvöfaldra skrifa úr Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingarinnar er lokið fara eftirfarandi aðgerðir sjálfkrafa fram:

- Nýtt, tómt umhverfi Finance and Operations er veitt.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Einingakort eru virk fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

Til að samstilla fyrirliggjandi gögn Common Data Service við forrit Finance and Operations fylgirðu þessum skrefum.

1. Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Common Data Service-gögnin með því að nota þriggja stafa fyrirtækjakóða Alþjóðlegu staðlastofnunarinnar (ISO).
4. Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.

Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Nýtt Finance and Operations forritstilvik sem inniheldur gögn og nýtt tilvik fyrir forrit viðskiptavinar

Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations forriti sem inniheldur gögn og nýtt tilvik fyrir þátt viðskiptaþjónsforrits skal fylgja skrefunum í [Nýtt Finance and Operations forritstilviks og nýtt tilvik fyrir forrit viðskiptavinar](#new-new) í fyrri hluta þessa efnisatriðis. Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.

1. Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.
2. Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.

Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Nýtt Finance and Operations hugbúnaðartilvik þar sem gögn og fyrirliggjandi forrit fyrir forrit viðskiptavinar

Til að setja upp tvískrifstengingu á milli nýs tilviks af Finance and Operations forriti sem inniheldur gögn og fyrirliggjandi tilvik um þátt viðskiptaþjónsforrits skal fylgja skrefunum í [Nýtt Finance and Operations forritstilvik og núverandi tilvik viðskiptaforritstilviks](#new-existing) kaflanum fyrr í þessu efnisatriði. Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.

1. Opnaðu forritið Finance and Operations af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.
2. Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.

Til að samstilla fyrirliggjandi gögn Common Data Service við forrit Finance and Operations fylgirðu þessum skrefum.

1. Stofnaðu nýtt fyrirtæki í forriti Finance and Operations.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Common Data Service-gögnin með því að nota þriggja stafa fyrirtækjakóða ISO.
4. Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.

Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Fyrirliggjandi Finance and Operations forritstilviks og nýtt tilvik fyrir forrit viðskiptavinar

Uppsetning á tvískrifstengingu á milli nýs tilviks Finance and Operations forritsins og fyrirliggjandi tilviks fyrir Customer Engagement forrit Finance and Operation-umhverfi.

1. [Setja upp tenginguna úr Finance and Operations forritinu](enable-dual-write.md).
2. Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.

Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Fyrirliggjandi Finance and Operations -hugbúnaðartilvik og fyrirliggjandi tilvik fyrir forrit viðskiptavinar

Uppsetning á tvískrifstengingu á milli núverandi tilviks Finance and Operations forritsins og fyrirliggjandi tilviks fyrir Customer Engagement forrit Finance and Operation-umhverfi.

1. Settu upp tenginguna úr forriti Finance and Operations.
2. Til að samstilla núverandi Common Data Service-gögn við forrit Finance and Operations, [skaltu ræsa](bootstrap-company-data.md) Common Data Service-gögnin með þriggja stafa ISO fyrirtækjakóða.
3. Keyrðu virknina **Upphafssamstilling** fyrir þær einingar sem þú vilt samstilla gögn fyrir.

Fyrir dæmi og aðra nálgun, sjá [Dæmi](#example).

## <a name="example"></a>Dæmi

Til dæmis [Virkjun viðskiptavina v3 — einingakort tengiliða](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)

Ef um er að ræða aðra nálgun sem byggist á gagnamagni í hverri einingu sem þarf að keyra upphaflega samstillingu, sjá [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).
