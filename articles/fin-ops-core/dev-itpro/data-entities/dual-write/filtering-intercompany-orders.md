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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="f9d25-103">Sía pantanir innan samstæðu til að komast hjá því að samstilla pantanir og pöntunarlínur</span><span class="sxs-lookup"><span data-stu-id="f9d25-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9d25-104">Hægt er að sía pantanir innan samstæðu til að komast hjá því að samstilla **Pantanir** og **Pöntunarlínur** einingar.</span><span class="sxs-lookup"><span data-stu-id="f9d25-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="f9d25-105">Í sumum aðstæðum eru upplýsingar um pöntun innan samstæðu ekki nauðsynlegar í forriti viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="f9d25-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="f9d25-106">Hver stöðluð Common Data Service -eining er útvíkkuð með tilvísunum í svæðið **IntercompanyOrder** og tvöföldu skráningunni er breytt til að vísa í viðbótarsvæði í síunum.</span><span class="sxs-lookup"><span data-stu-id="f9d25-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="f9d25-107">Niðurstaðan er sú að samstæðupantanir eru ekki lengur samstilltar.</span><span class="sxs-lookup"><span data-stu-id="f9d25-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="f9d25-108">Þetta ferli forðast óþarfa gögn í forriti viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="f9d25-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="f9d25-109">Bætið við tilvísun í **IntercompanyOrder** í **Hausar CDS-sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="f9d25-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="f9d25-110">Aðeins er fyllt út í pöntun innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="f9d25-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="f9d25-111">Reiturinn **IntercompanyOrder** er tiltækur í **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="f9d25-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Varpa sviðsetningu á mark, SalesOrderHeader":::
    
2. <span data-ttu-id="f9d25-113">Þegar **Hausar CDS-sölupöntunar** er útvíkkað er svæðið **IntercompanyOrder** aðgengilegt í vörpuninni.</span><span class="sxs-lookup"><span data-stu-id="f9d25-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="f9d25-114">Nota skal síu með `INTERCOMPANYORDER == ""` sem fyrirspurnarstreng.</span><span class="sxs-lookup"><span data-stu-id="f9d25-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Hausar sölupöntunar, breyta fyrirspurn":::

3. <span data-ttu-id="f9d25-116">Bætið við tilvísun í **IntercompanyInventTransId** í **Hausar CDS-sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="f9d25-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="f9d25-117">Aðeins er fyllt út í pöntun innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="f9d25-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="f9d25-118">Reiturinn **InterCompanyInventTransID** er tiltækur í **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="f9d25-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Varpa sviðsetningu á mark, SalesOrderLine":::

4. <span data-ttu-id="f9d25-120">Þegar **CDS-sölupöntunarlínur** er útvíkkað er svæðið **IntercompanyInventTransId** aðgengilegt í vörpuninni.</span><span class="sxs-lookup"><span data-stu-id="f9d25-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="f9d25-121">Nota skal síu með `INTERCOMPANYINVENTTRANSID == ""` sem fyrirspurnarstreng.</span><span class="sxs-lookup"><span data-stu-id="f9d25-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Sölupöntunarlínur, breyta fyrirspurn":::

5. <span data-ttu-id="f9d25-123">Framlengið **Sölureikningshaus V2** og **Sölureikningslínur V2** á sama hátt og Common Data Service-einingarnar í skrefum 1 og 2 voru framlengdar.</span><span class="sxs-lookup"><span data-stu-id="f9d25-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="f9d25-124">Bættu síðan við síufyrirspurnum.</span><span class="sxs-lookup"><span data-stu-id="f9d25-124">Then add the filter queries.</span></span> <span data-ttu-id="f9d25-125">Síustrengurinn fyrir **Sölureikningshaus V2** er `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="f9d25-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="f9d25-126">Síustrengurinn fyrir **Sölureikningslínur V2** er `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="f9d25-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Varpa sviðsetningu á mark, sölureikningshausar":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Sölureikningshausar, breyta fyrirspurn":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Sölureikningslínur, breyta fyrirspurn":::

6. <span data-ttu-id="f9d25-130">Einingin **Tilboð** er ekki með samstæðuvensl.</span><span class="sxs-lookup"><span data-stu-id="f9d25-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="f9d25-131">Ef einhver stofnar tilboð fyrir einn af samstæðuviðskiptavinunum er hægt að setja alla þessa viðskiptavini í einn viðskiptavinaflokk með því að nota svæðið **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="f9d25-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="f9d25-132">Hægt er að framlengja haus og línur til að bæta við svæðinu **CustGroup** og sía svo flokkinn út.</span><span class="sxs-lookup"><span data-stu-id="f9d25-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Varpa sviðsetningu á mark, sölutilboðshaus":::

7. <span data-ttu-id="f9d25-134">Eftir að einingin **Tilboð** hefur verið framlengd skaltu nota síu með `CUSTGROUP !=  "<company>"` sem fyrirspurnarstreng.</span><span class="sxs-lookup"><span data-stu-id="f9d25-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Sölutilboðshaus, breyta fyrirspurn":::
