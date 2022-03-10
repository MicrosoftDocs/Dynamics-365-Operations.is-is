---
title: Leiðbeinigar fyrir uppsetningu tvöfaldra skrifa
description: Þetta efni lýsir atburðarásum sem eru studdar fyrir tvískipt skrifun.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6de449b14bcdd82336e3e255bf62ad069d3daaf5
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061605"
---
# <a name="guidance-for-dual-write-setup"></a>Leiðbeinigar fyrir uppsetningu tvöfaldra skrifa

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Þú getur sett upp tvískrifaða tengingu milli Finance and Operations umhverfi og a Dataverse umhverfi.

+ A **Fjármál og rekstrarumhverfi** veitir undirliggjandi vettvang fyrir **Fjármála- og rekstrarforrit** (td Microsoft Dynamics 365 Finance,Dynamics 365 Supply Chain Management,Dynamics 365 Commerce, og Dynamics 365 Human Resources).
+ **Dataverse Umhverfi** veitir undirliggjandi verkvang fyrir **forrit viðskiptavina** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Mannauðseiningin í Dynamics 365 Finance styður tengingu tvískiptra skrifa, en Dynamics 365 Human Resources-forritið gerir það ekki.

Uppsetningarkerfi er breytilegt, allt eftir áskrift þinni og umhverfi:

+ Fyrir ný tilvik af Finance and Operations forritum hefst uppsetning tvískrifaðrar tengingar í Microsoft Dynamics Lífsferilsþjónusta (LCS). Ef þú ert með leyfi fyrir Microsoft Power Platform geturðu fengið nýtt umhverfi Dataverse ef leigjandi þinn hefur ekki slíkt.
+ Fyrir núverandi tilvik Finance and Operations forrit hefst uppsetning tvískrifaðrar tengingar í Finance and Operations umhverfinu.

Áður en þú byrjar tvískrift á einingu geturðu keyrt fyrstu samstillingu til að meðhöndla núverandi gögn á báða bóga: Fjármála- og rekstrarforrit og öpp fyrir þátttöku viðskiptavina. Hægt er að sleppa upphaflegu samstillingunni ef ekki þarf að samstilla gögn á milli umhverfanna tveggja.

Upphafleg samstilling gerir notanda kleift að afrita fyrirliggjandi gögn úr einu forriti í annað. Nokkrar uppsetningaraðstæður eru til staðar, allt eftir því umhverfi sem er þegar til staðar og gerð gagna í þeim.

Eftirfarandi uppsetningaraðstæður eru studdar:

+ [Nýtt Finance and Operations app tilvik og nýtt tilvik viðskiptavina þátttöku app](#new-new)
+ [Nýtt Finance and Operations app tilvik og núverandi tilvik viðskiptavina þátttöku app](#new-existing)
+ [Nýtt Finance and Operations app tilvik sem hefur gögn og nýtt tilvik viðskiptavina þátttöku app](#new-data-new)
+ [Nýtt Finance and Operations forritatilvik sem hefur gögn og núverandi forrit fyrir þátttöku viðskiptavina](#new-data-existing)
+ [Fyrirliggjandi Finance and Operations app tilvik og nýtt tilvik viðskiptavina þátttöku app](#existing-new)
+ [Fyrirliggjandi Finance and Operations app tilvik og núverandi forrit fyrir þátttöku viðskiptavina](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Nýtt Finance and Operations app tilvik og nýtt tilvik viðskiptavina þátttöku app

Til að setja upp tvískrifaða tengingu á milli nýs tilviks af Finance and Operations forriti sem hefur engin gögn og nýs tilviks af viðskiptaforriti, fylgdu skrefunum í [Dual-write uppsetning frá Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingar er lokið eiga eftirfarandi aðgerðir sér stað sjálfkrafa:

- Nýtt tómt fjármála- og rekstrarumhverfi er útvegað.
- Nýju, auðu tilviki af forriti viðskiptavinar er úthlutað, þar sem CRM úrvalslausnin er uppsett.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Töflukort eru virkjuð fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Nýtt Finance and Operations app tilvik og núverandi tilvik viðskiptavina þátttöku app

Til að setja upp tvískrifaða tengingu á milli nýs tilviks af Finance and Operations forriti sem hefur engin gögn og núverandi tilviks af forriti fyrir þátttöku viðskiptavina skaltu fylgja skrefunum í [Dual-write uppsetning frá Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingar er lokið eiga eftirfarandi aðgerðir sér stað sjálfkrafa:

- Nýtt tómt fjármála- og rekstrarumhverfi er útvegað.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Töflukort eru virkjuð fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

Til að samstilla núverandi Dataverse gögnum í Finance and Operations appið, fylgdu þessum skrefum.

1. Búðu til nýtt fyrirtæki í Finance and Operations appinu.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Dataverse-gögnin með því að nota þriggja stafa fyrirtækjakóða Alþjóðlegu staðlastofnunarinnar (ISO).
4. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example) síðar í þessu efnisatriði.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Nýtt Finance and Operations app tilvik sem hefur gögn og nýtt tilvik viðskiptavina þátttöku app

Til að setja upp tvískrifaða tengingu á milli nýs tilviks af Finance and Operations forriti sem hefur gögn og nýs tilviks af samskiptaforriti viðskiptavina, skaltu fylgja skrefunum í [Nýtt Finance and Operations app tilvik og nýtt tilvik viðskiptavina þátttöku app](#new-new) kafla fyrr í þessu efni. Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.

1. Opnaðu Finance and Operations appið frá LCS síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrifa**.
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Nýtt Finance and Operations forritatilvik sem hefur gögn og núverandi forrit fyrir þátttöku viðskiptavina

Til að setja upp tvískrifaða tengingu á milli nýs tilviks af Finance and Operations forriti sem hefur gögn og núverandi tilviks af samskiptaforriti viðskiptavina, skaltu fylgja skrefunum í [Nýtt Finance and Operations app tilvik og núverandi tilvik viðskiptavina þátttöku app](#new-existing) kafla fyrr í þessu efni. Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.

1. Opnaðu Finance and Operations appið frá LCS síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrifa**.
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Til að samstilla núverandi Dataverse gögnum í Finance and Operations appið, fylgdu þessum skrefum.

1. Búðu til nýtt fyrirtæki í Finance and Operations appinu.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Dataverse-gögnin með því að nota þriggja stafa fyrirtækjakóða ISO.
4. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Fyrirliggjandi Finance and Operations app tilvik og nýtt tilvik viðskiptavina þátttöku app

Uppsetning tvískrifaðrar tengingar á milli núverandi tilviks af Finance and Operations appi og nýs tilviks af viðskiptasamskiptaforriti á sér stað í Finance and Operation umhverfinu.

1. [Settu upp tenginguna úr Finance and Operations appinu](enable-dual-write.md).
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Fyrirliggjandi Finance and Operations app tilvik og núverandi forrit fyrir þátttöku viðskiptavina

Uppsetning tvískrifaðrar tengingar á milli núverandi tilviks af Finance and Operations appi og núverandi tilviks af viðskiptasamskiptaforriti á sér stað í Finance and Operation umhverfinu.

1. [Settu upp tenginguna úr Finance and Operations appinu](enable-dual-write.md).
2. Til að samstilla núverandi Dataverse gögn í Finance and Operations appið, [stígvél](bootstrap-company-data.md) the Dataverse gögn með því að nota þriggja stafa ISO fyrirtækjakóða.
3. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="example"></a>Dæmi

Sjá til dæmis [Virkjun viðskiptavina v3 — Töflukort tengiliða](enable-entity-map.md#enable-table-map)

Ef um er að ræða aðra nálgun sem byggir á gagnamagni í hverri einingu sem þarf að keyra upphaflega samstillingu, sjá [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]