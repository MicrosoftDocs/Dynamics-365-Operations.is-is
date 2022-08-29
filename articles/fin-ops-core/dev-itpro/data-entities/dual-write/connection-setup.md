---
title: Leiðbeinigar fyrir uppsetningu tvöfaldra skrifa
description: Þessi grein lýsir þeim atburðarásum sem eru studdar fyrir tvískrifa uppsetningu.
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b27cabf495448fcd82edd374bb59e6e5a664c7e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289745"
---
# <a name="guidance-for-dual-write-setup"></a>Leiðbeinigar fyrir uppsetningu tvöfaldra skrifa

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Hægt er að setja upp tvískrifaða tengingu milli fjármála- og rekstrarumhverfis og a Dataverse umhverfi.

+ A **fjármála- og rekstrarumhverfi** veitir undirliggjandi vettvang fyrir **fjármála- og rekstrarforrit** (til dæmis,Microsoft Dynamics 365 Fjármál,Dynamics 365 Supply Chain Management,Dynamics 365 Commerce, og Dynamics 365 Human Resources).
+ **Dataverse Umhverfi** veitir undirliggjandi verkvang fyrir **forrit viðskiptavina** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).


> [!IMPORTANT]
> Mannauðseiningin í Dynamics 365 Finance styður tvískrifa tengingar, en Dynamics 365 Human Resources app gerir það ekki.

Uppsetningarkerfi er breytilegt, allt eftir áskrift þinni og umhverfi:

+ Fyrir ný tilvik af fjármála- og rekstrarforritum hefst uppsetning tvískrifaðrar tengingar í Microsoft Dynamics Lífsferilsþjónusta (LCS). Ef þú ert með leyfi fyrir Microsoft Power Platform geturðu fengið nýtt umhverfi Dataverse ef leigjandi þinn hefur ekki slíkt.
+ Fyrir núverandi tilvik fjármála- og rekstrarforrit hefst uppsetning tvískrifaðrar tengingar í fjármála- og rekstrarumhverfinu.

Áður en þú byrjar tvískrift á einingu geturðu keyrt fyrstu samstillingu til að meðhöndla núverandi gögn á báða bóga: Fjármála- og rekstrarforrit og öpp fyrir þátttöku viðskiptavina. Hægt er að sleppa upphaflegu samstillingunni ef ekki þarf að samstilla gögn á milli umhverfanna tveggja.

Upphafleg samstilling gerir notanda kleift að afrita fyrirliggjandi gögn úr einu forriti í annað. Nokkrar uppsetningaraðstæður eru til staðar, allt eftir því umhverfi sem er þegar til staðar og gerð gagna í þeim.

Eftirfarandi uppsetningaraðstæður eru studdar:

+ [Nýtt tilvik fjármála- og rekstrarforrits og nýtt forrit fyrir þátttöku viðskiptavina](#new-new)
+ [Nýtt tilvik um fjármála- og rekstrarapp og núverandi forrit fyrir þátttöku viðskiptavina](#new-existing)
+ [Nýtt tilvik fjármála- og rekstrarforrita sem hefur gögn og nýtt forrit fyrir þátttöku viðskiptavina](#new-data-new)
+ [Nýtt tilvik fjármála- og rekstrarforrita sem hefur gögn og núverandi forrit fyrir þátttöku viðskiptavina](#new-data-existing)
+ [Fyrirliggjandi tilvik um fjármála- og rekstrarapp og nýtt tilvik um þátttöku viðskiptavina](#existing-new)
+ [Fyrirliggjandi tilvik um fjármála- og rekstrarforrit og fyrirliggjandi forrit fyrir þátttöku viðskiptavina](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Nýtt tilvik fjármála- og rekstrarforrits og nýtt forrit fyrir þátttöku viðskiptavina

Til að setja upp tvískrifaða tengingu á milli nýs tilviks af fjármála- og rekstrarforriti sem hefur engin gögn og nýs tilviks viðskiptaforrits, fylgdu skrefunum í [Dual-write uppsetning frá Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingar er lokið eiga eftirfarandi aðgerðir sér stað sjálfkrafa:

- Nýtt tómt fjármála- og rekstrarumhverfi er útvegað.
- Nýju, auðu tilviki af forriti viðskiptavinar er úthlutað, þar sem CRM úrvalslausnin er uppsett.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Töflukort eru virkjuð fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Nýtt tilvik um fjármála- og rekstrarapp og núverandi forrit fyrir þátttöku viðskiptavina

Til að setja upp tvískrifaða tengingu á milli nýs tilviks af fjármála- og rekstrarforriti sem hefur engin gögn og núverandi tilviks af samskiptaforriti viðskiptavina, skaltu fylgja skrefunum í [Dual-write uppsetning frá Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingar er lokið eiga eftirfarandi aðgerðir sér stað sjálfkrafa:

- Nýtt tómt fjármála- og rekstrarumhverfi er útvegað.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Töflukort eru virkjuð fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

Til að samstilla núverandi Dataverse gögnum í fjármála- og rekstrarappið skaltu fylgja þessum skrefum.

1. Búðu til nýtt fyrirtæki í fjármála- og rekstrarappinu.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Dataverse-gögnin með því að nota þriggja stafa fyrirtækjakóða Alþjóðlegu staðlastofnunarinnar (ISO).
4. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Sjá tengla á dæmi og aðra nálgun [Dæmi](#example) kafla síðar í þessari grein.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Nýtt tilvik fjármála- og rekstrarforrita sem hefur gögn og nýtt forrit fyrir þátttöku viðskiptavina

Til að setja upp tvískrifaða tengingu á milli nýs tilviks af fjármála- og rekstrarforriti sem hefur gögn og nýs tilviks af samskiptaforriti viðskiptavina, skaltu fylgja skrefunum í [Nýtt tilvik fjármála- og rekstrarforrits og nýtt forrit fyrir þátttöku viðskiptavina](#new-new) kafla fyrr í þessari grein. Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.

1. Opnaðu fjármála- og rekstrarappið af LCS síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrifa**.
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Nýtt tilvik fjármála- og rekstrarforrita sem hefur gögn og núverandi forrit fyrir þátttöku viðskiptavina

Til að setja upp tvískrifaða tengingu á milli nýs tilviks af fjármála- og rekstrarforriti sem hefur gögn og núverandi tilviks viðskiptaforrits, fylgdu skrefunum í [Nýtt tilvik um fjármála- og rekstrarapp og núverandi forrit fyrir þátttöku viðskiptavina](#new-existing) kafla fyrr í þessari grein. Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.

1. Opnaðu fjármála- og rekstrarappið af LCS síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrifa**.
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Til að samstilla núverandi Dataverse gögnum í fjármála- og rekstrarappið skaltu fylgja þessum skrefum.

1. Búðu til nýtt fyrirtæki í fjármála- og rekstrarappinu.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Dataverse-gögnin með því að nota þriggja stafa fyrirtækjakóða ISO.
4. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Fyrirliggjandi tilvik um fjármála- og rekstrarapp og nýtt tilvik um þátttöku viðskiptavina

Uppsetning tvískrifaðrar tengingar milli núverandi tilviks af fjármála- og rekstrarforriti og nýs tilviks viðskiptaforrits á sér stað í fjármála- og rekstrarumhverfinu.

1. [Settu upp tenginguna úr fjármála- og rekstrarappinu](enable-dual-write.md).
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Fyrirliggjandi tilvik um fjármála- og rekstrarforrit og fyrirliggjandi forrit fyrir þátttöku viðskiptavina

Uppsetning tvískrifaðrar tengingar á milli núverandi tilviks af fjármála- og rekstrarforriti og núverandi tilviks viðskiptaforrits á sér stað í fjármála- og rekstrarumhverfinu.

1. [Settu upp tenginguna úr fjármála- og rekstrarappinu](enable-dual-write.md).
2. Til að samstilla núverandi Dataverse gögn í fjármála- og rekstrarappið, [stígvél](bootstrap-company-data.md) the Dataverse gögn með því að nota þriggja stafa ISO fyrirtækjakóða.
3. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="example"></a>Dæmi

Sjá til dæmis [Virkjun viðskiptavina v3 — Töflukort tengiliða](enable-entity-map.md#enable-table-map)

Ef um er að ræða aðra nálgun sem byggir á gagnamagni í hverri einingu sem þarf að keyra upphaflega samstillingu, sjá [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
