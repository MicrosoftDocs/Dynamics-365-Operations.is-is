---
title: Leiðbeinigar fyrir uppsetningu tvöfaldra skrifa
description: Þessi grein lýsir atburðarásum sem eru studdar fyrir uppsetningu tvískiptra skrifa.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289745"
---
# <a name="guidance-for-dual-write-setup"></a>Leiðbeinigar fyrir uppsetningu tvöfaldra skrifa

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Þú getur sett upp tvískipt samband milli umhverfis fjármála- og reksturs og Dataverse umhverfis.

+ **Umhverfi fjármála- og reksturs** veitir undirstöðuvettvang fyrir **forrit fjármála- og reksturs** (til dæmis, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources).
+ **Dataverse Umhverfi** veitir undirliggjandi verkvang fyrir **forrit viðskiptavina** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).


> [!IMPORTANT]
> Mannauðseiningin í Dynamics 365 Finance styður tengingu tvískiptra skrifa, en Dynamics 365 Human Resources-forritið gerir það ekki.

Uppsetningarkerfi er breytilegt, allt eftir áskrift þinni og umhverfi:

+ Fyrir ný tilvik af forritum fjármála- og reksturs hefst uppsetningin á tvískiptri tengingu í Microsoft Dynamics Lifecycle Services (LCS). Ef þú ert með leyfi fyrir Microsoft Power Platform geturðu fengið nýtt umhverfi Dataverse ef leigjandi þinn hefur ekki slíkt.
+ Fyrir núverandi tilvik forrita fjármála- og reksturs hefst uppsetning tvískiptrar tengingar í umhverfi fjármála- og reksturs.

Áður en þú ræsir tvírita í einingu er hægt að keyra fyrstu samstillingu til að meðhöndla fyrirliggjandi gögn á báðum hliðum forrita fjármála- og reksturs og Customer Engagement-forrita. Hægt er að sleppa upphaflegu samstillingunni ef ekki þarf að samstilla gögn á milli umhverfanna tveggja.

Upphafleg samstilling gerir notanda kleift að afrita fyrirliggjandi gögn úr einu forriti í annað. Nokkrar uppsetningaraðstæður eru til staðar, allt eftir því umhverfi sem er þegar til staðar og gerð gagna í þeim.

Eftirfarandi uppsetningaraðstæður eru studdar:

+ [Nýtt forritstilvik fjármála- og reksturs og nýtt tilvik fyrir forrit viðskiptavinar](#new-new)
+ [Fyrirliggjandi hugbúnaðartilvik fjármála- og reksturs og fyrirliggjandi tilvik fyrir forrit viðskiptavinar](#new-existing)
+ [Nýtt forritstilvik fjármála- og reksturs sem inniheldur gögn og nýtt tilvik fyrir forrit viðskiptavinar](#new-data-new)
+ [Nýtt hugbúnaðartilvik fjármála- og reksturs þar sem gögn og fyrirliggjandi forrit fyrir forrit viðskiptavinar](#new-data-existing)
+ [Fyrirliggjandi forritstilvik fjármála- og reksturs og nýtt tilvik fyrir forrit viðskiptavinar](#existing-new)
+ [Fyrirliggjandi hugbúnaðartilvik fjármála- og reksturs og fyrirliggjandi tilvik fyrir forrit viðskiptavinar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Nýtt forritstilvik fjármála- og reksturs og nýtt tilvik fyrir forrit viðskiptavinar

Til að setja upp tvískrifstengingu á milli nýs tilviks forrits fjármála- og reksturs sem inniheldur engin gögn og nýs tilviks um þjónsforrit skal fylgja skrefunum í [Uppsetning tvöfaldra skrifa úr Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingar er lokið eiga eftirfarandi aðgerðir sér stað sjálfkrafa:

- Nýtt, tómt umhverfi fjármála- og reksturs er veitt.
- Nýju, auðu tilviki af forriti viðskiptavinar er úthlutað, þar sem CRM úrvalslausnin er uppsett.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Töflukort eru virkjuð fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Fyrirliggjandi hugbúnaðartilvik fjármála- og reksturs og fyrirliggjandi tilvik fyrir forrit viðskiptavinar

Til að setja upp tvískrifstengingu á milli nýs tilviks af forriti fjármála- og reksturs sem inniheldur engin gögn og fyrirliggjandi tilvik um þjónsforrit skal fylgja skrefunum í [Uppsetning tvöfaldra skrifa úr Lifecycle Services](lcs-setup.md). Þegar uppsetningu tengingar er lokið eiga eftirfarandi aðgerðir sér stað sjálfkrafa:

- Nýtt, tómt umhverfi fjármála- og reksturs er veitt.
- Tvískiptri tengingu er komið á fyrir DAT-gögn fyrirtækja.
- Töflukort eru virkjuð fyrir samstillingu í beinni.

Bæði umhverfin eru síðan tilbúin fyrir samstillingu á gögnum í rauntíma.

Til að samstilla fyrirliggjandi gögn Dataverse við forrit fjármála- og reksturs fylgirðu þessum skrefum.

1. Stofnaðu nýtt fyrirtæki í forriti fjármála- og reksturs.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Dataverse-gögnin með því að nota þriggja stafa fyrirtækjakóða Alþjóðlegu staðlastofnunarinnar (ISO).
4. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example) síðar í þessari grein.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Nýtt forritstilvik fjármála- og reksturs sem inniheldur gögn og nýtt tilvik fyrir forrit viðskiptavinar

Til að setja upp tvískrifstengingu á milli nýs tilviks forrits fjármála- og reksturs sem inniheldur gögn og nýtt tilvik fyrir þátt viðskiptaþjónsforrits skal fylgja skrefunum í [Nýtt forritstilviks fjármála- og reksturs og nýtt tilvik fyrir forrit viðskiptavinar](#new-new) í fyrri hluta þessarar greinar. Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.

1. Opnaðu forrit fjármála- og reksturs af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Nýtt hugbúnaðartilvik fjármála- og reksturs þar sem gögn og fyrirliggjandi forrit fyrir forrit viðskiptavinar

Til að setja upp tvískrifstengingu á milli nýs tilviks forrits fjármála- og reksturs sem inniheldur gögn og fyrirliggjandi tilvik um þátt viðskiptaþjónsforrits skal fylgja skrefunum í [Nýtt forritstilvik fjármála- og reksturs og núverandi tilvik viðskiptaforritstilviks](#new-existing) kaflanum fyrr í þessari grein. Þegar uppsetningu tengingar er lokið, ef samstilla á gögnin við viðskiptaforrit fyrir Customer Engagement skal fylgja þessum skrefum.

1. Opnaðu forrit fjármála- og reksturs af LCS-síðunni, skráðu þig inn og farðu síðan á **Gagnastjórnun \> Tvöfalt skrif**.
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Til að samstilla fyrirliggjandi gögn Dataverse við forrit fjármála- og reksturs fylgirðu þessum skrefum.

1. Stofnaðu nýtt fyrirtæki í forriti fjármála- og reksturs.
2. Bættu fyrirtækinu við tvískiptu tengingaruppsetninguna.
3. [Ræstu](bootstrap-company-data.md) Dataverse-gögnin með því að nota þriggja stafa fyrirtækjakóða ISO.
4. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Fyrirliggjandi forritstilvik fjármála- og reksturs og nýtt tilvik fyrir forrit viðskiptavinar

Uppsetning á tvískrifstengingu á milli nýs tilviks forrits fjármála- og reksturs og fyrirliggjandi tilviks fyrir Customer Engagement forrit í umhverfi fjármála- og reksturs.

1. [Setja upp tenginguna úr forriti fjármála- og reksturs](enable-dual-write.md).
2. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Fyrirliggjandi hugbúnaðartilvik fjármála- og reksturs og fyrirliggjandi tilvik fyrir forrit viðskiptavinar

Uppsetning á tvískrifstengingu á milli núverandi tilviks forrits fjármála- og reksturs og fyrirliggjandi tilviks fyrir Customer Engagement forrits fyrir umhverfi fjármála- og reksturs.

1. [Setja upp tenginguna úr forriti fjármála- og reksturs](enable-dual-write.md).
2. Til að samstilla núverandi Dataverse-gögn við forrit fjármála- og reksturs, [skaltu ræsa](bootstrap-company-data.md) Dataverse-gögnin með þriggja stafa ISO fyrirtækjakóða.
3. Keyrið virknina **Upphafleg samstilling** fyrir töflurnar sem á að samstilla gögn fyrir.

Tengla í dæmi og aðra nálgun má finna í hlutanum [Dæmi](#example).

## <a name="example"></a>Dæmi

Sjá til dæmis [Virkjun viðskiptavina v3 — Töflukort tengiliða](enable-entity-map.md#enable-table-map)

Ef um er að ræða aðra nálgun sem byggir á gagnamagni í hverri einingu sem þarf að keyra upphaflega samstillingu, sjá [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
