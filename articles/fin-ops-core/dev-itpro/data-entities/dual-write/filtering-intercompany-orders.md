---
title: Sía pantanir innan samstæðu til að komast hjá því að samstilla pantanir og pöntunarlínur
description: Í þessu efnisatriði er því lýst hvernig pantanir eru síaðar innan samstæðu til að komast hjá því að samstilla pantanir og pöntunarlínur.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701034"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Sía pantanir innan samstæðu til að komast hjá því að samstilla pantanir og pöntunarlínur

[!include [banner](../../includes/banner.md)]

Hægt er að sía pantanir innan samstæðu til að komast hjá því að samstilla **Pantanir** og **Pöntunarlínur** einingar. Í sumum aðstæðum eru upplýsingar um pöntun innan samstæðu ekki nauðsynlegar í forriti viðskiptavinar.

Hver stöðluð Common Data Service -eining er útvíkkuð með tilvísunum í svæðið **IntercompanyOrder** og tvöföldu skráningunni er breytt til að vísa í viðbótarsvæði í síunum. Niðurstaðan er sú að samstæðupantanir eru ekki lengur samstilltar. Þetta ferli forðast óþarfa gögn í forriti viðskiptavinar.

1. Bætið við tilvísun í **IntercompanyOrder** í **Hausar CDS-sölupöntunar**. Aðeins er fyllt út í pöntun innan samstæðu. Reiturinn **IntercompanyOrder** er tiltækur í **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Varpa sviðsetningu á mark, SalesOrderHeader":::
    
2. Þegar **Hausar CDS-sölupöntunar** er útvíkkað er svæðið **IntercompanyOrder** aðgengilegt í vörpuninni. Nota skal síu með `INTERCOMPANYORDER == ""` sem fyrirspurnarstreng.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Hausar sölupöntunar, breyta fyrirspurn":::

3. Bætið við tilvísun í **IntercompanyInventTransId** í **Hausar CDS-sölupöntunar**.  Aðeins er fyllt út í pöntun innan samstæðu. Reiturinn **InterCompanyInventTransID** er tiltækur í **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Varpa sviðsetningu á mark, SalesOrderLine":::

4. Þegar **CDS-sölupöntunarlínur** er útvíkkað er svæðið **IntercompanyInventTransId** aðgengilegt í vörpuninni. Nota skal síu með `INTERCOMPANYINVENTTRANSID == ""` sem fyrirspurnarstreng.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Sölupöntunarlínur, breyta fyrirspurn":::

5. Framlengið **Sölureikningshaus V2** og **Sölureikningslínur V2** á sama hátt og Common Data Service-einingarnar í skrefum 1 og 2 voru framlengdar. Bættu síðan við síufyrirspurnum. Síustrengurinn fyrir **Sölureikningshaus V2** er `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Síustrengurinn fyrir **Sölureikningslínur V2** er `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Varpa sviðsetningu á mark, sölureikningshausar":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Sölureikningshausar, breyta fyrirspurn":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Sölureikningslínur, breyta fyrirspurn":::

6. Einingin **Tilboð** er ekki með samstæðuvensl. Ef einhver stofnar tilboð fyrir einn af samstæðuviðskiptavinunum er hægt að setja alla þessa viðskiptavini í einn viðskiptavinaflokk með því að nota svæðið **CustGroup**.  Hægt er að framlengja haus og línur til að bæta við svæðinu **CustGroup** og sía svo flokkinn út.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Varpa sviðsetningu á mark, sölutilboðshaus":::

7. Eftir að einingin **Tilboð** hefur verið framlengd skaltu nota síu með `CUSTGROUP !=  "<company>"` sem fyrirspurnarstreng.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Sölutilboðshaus, breyta fyrirspurn":::
