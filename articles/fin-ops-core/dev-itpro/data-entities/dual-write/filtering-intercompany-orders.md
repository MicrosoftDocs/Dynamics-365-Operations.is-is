---
title: Sía pantanir innan samstæðu til að komast hjá samstillingu pantana og pöntunarlína
description: Þetta efnisatriði útskýrir hvernig á að sía pantanir innan samstæðu þannig að einingar pöntunar og pöntunarlína samstillist ekki.
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e09f2037645609d5b5b5d05f27bc5f094287ef03
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416954"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Sía pantanir innan samstæðu til að komast hjá samstillingu pantana og pöntunarlína

[!include [banner](../../includes/banner.md)]

Hægt er að sía pantanir innan samstæðu þannig að töflurnar **Pantanir** og **Pöntunarlínur** samstillist ekki. Í sumum aðstæðum eru upplýsingar um pöntun innan samstæðu ekki nauðsynlegar í forriti viðskiptavina.

Hver stöðluð Dataverse-tafla er útvíkkuð með tilvísunum í dálkinn **IntercompanyOrder** og vörpunum tvöfaldrar skráningar er breytt þannig að þær vísa í viðbótardálkana í síunum. Þess vegna eru samstæðupantanir ekki lengur samstilltar. Þetta ferli kemur í veg fyrir ónauðsynleg gögn í forriti viðskiptavinar.

1. Útvíkka skal töfluna **Hausar CDS-sölupöntunar** með því að bæta tilvísun við dálkinn **IntercompanyOrder**. Þessi dálkur er aðeins fylltur út í samstæðupöntunum. Dálkurinn **IntercompanyOrder** er í boði í töflunni **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Varpa sviðsetningu á marksíðu fyrir hausa CDS-sölupöntunar.":::

2. Þegar **Hausar CDS-sölupöntunar** er útvíkkað er dálkurinn **IntercompanyOrder** aðgengilegur í vörpuninni. Nota skal síu sem er með `INTERCOMPANYORDER == ""` sem fyrirspurnarstreng.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Breyta svarglugga fyrirspurnar fyrir hausa CDS-sölupantana.":::

3. Útvíkka skal töfluna **Hausar CDS-sölupöntunar** með því að bæta tilvísun við dálkinn **IIntercompanyInventTransId**. Þessi dálkur er aðeins fylltur út í samstæðupöntunum. Dálkurinn **InterCompanyInventTransId** er í boði í töflunni **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Varpa sviðsetningu á marksíðu fyrir línur CDS-sölupöntunar.":::

4. Þegar **CDS-sölupöntunarlínur** er útvíkkað er dálkurinn **IntercompanyInventTransId** aðgengilegur í vörpuninni. Nota skal síu sem er með `INTERCOMPANYINVENTTRANSID == ""` sem fyrirspurnarstreng.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Breyta svarglugga fyrirspurnar fyrir línur CDS-sölupantana.":::

5. Endurtakið skref 1 og 2 til að víkka út töfluna **Sölureikningshaus V2** og bæta við síufyrirspurn. Í þessu tilviki skal nota `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` sem fyrirspurnarstreng fyrir síuna.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Varpa sviðsetningu á marksíðu fyrir sölureikningshaus V2.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Breyta svarglugga fyrirspurnar fyrir sölureikningshaus V2.":::

6. Endurtakið skref 3 og 4 til að víkka út töfluna **Sölureikningshaus V2** og bæta við síufyrirspurn. Í þessu tilviki skal nota `INTERCOMPANYINVENTTRANSID == ""` sem fyrirspurnarstreng fyrir síuna.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Breyta svarglugga fyrirspurnar fyrir sölureikningslínur V2.":::

7. Taflan **Tilboð** er ekki með vensl innan samstæðu. Ef einhver stofnar tilboð fyrir einn af viðskiptavinum innan samstæðu er hægt dálkinn **CustGroup** til að setja alla þessa viðskiptavini í einn viðskiptavinaflokk. Hægt er að víkka út hausinn og línurnar með því að bæta við dálkinum **CustGroup** og síðan sía þannig að flokkurinn sé ekki tekinn með.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Varpa sviðsetningu á marksíðu fyrir CDS-sölutilboðshaus.":::

8. Þegar **Tilboð** hafa verið víkkuð út skal nota síu sem er með `CUSTGROUP != "<company>"` sem fyrirspurnarstreng.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Breyta svarglugga fyrirspurnar fyrir CDS-sölutilboðshaus.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]