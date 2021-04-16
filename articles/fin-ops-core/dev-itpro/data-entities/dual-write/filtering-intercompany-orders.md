---
title: Sía pantanir innan samstæðu til að komast hjá samstillingu pantana og pöntunarlína
description: Þetta efnisatriði útskýrir hvernig á að sía pantanir innan samstæðu þannig að einingar pöntunar og pöntunarlína samstillist ekki.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 123427db61782490d348489c23e0eaf5f8b513c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748642"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="65d8d-103">Sía pantanir innan samstæðu til að komast hjá samstillingu pantana og pöntunarlína</span><span class="sxs-lookup"><span data-stu-id="65d8d-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65d8d-104">Hægt er að sía pantanir innan samstæðu þannig að töflurnar **Pantanir** og **Pöntunarlínur** samstillist ekki.</span><span class="sxs-lookup"><span data-stu-id="65d8d-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="65d8d-105">Í sumum aðstæðum eru upplýsingar um pöntun innan samstæðu ekki nauðsynlegar í forriti viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="65d8d-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="65d8d-106">Hver stöðluð Dataverse-tafla er útvíkkuð með tilvísunum í dálkinn **IntercompanyOrder** og vörpunum tvöfaldrar skráningar er breytt þannig að þær vísa í viðbótardálkana í síunum.</span><span class="sxs-lookup"><span data-stu-id="65d8d-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="65d8d-107">Þess vegna eru samstæðupantanir ekki lengur samstilltar.</span><span class="sxs-lookup"><span data-stu-id="65d8d-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="65d8d-108">Þetta ferli kemur í veg fyrir ónauðsynleg gögn í forriti viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="65d8d-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="65d8d-109">Útvíkka skal töfluna **Hausar CDS-sölupöntunar** með því að bæta tilvísun við dálkinn **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="65d8d-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="65d8d-110">Þessi dálkur er aðeins fylltur út í samstæðupöntunum.</span><span class="sxs-lookup"><span data-stu-id="65d8d-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="65d8d-111">Dálkurinn **IntercompanyOrder** er í boði í töflunni **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="65d8d-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Varpa sviðsetningu á marksíðu fyrir hausa CDS-sölupöntunar":::

2. <span data-ttu-id="65d8d-113">Þegar **Hausar CDS-sölupöntunar** er útvíkkað er dálkurinn **IntercompanyOrder** aðgengilegur í vörpuninni.</span><span class="sxs-lookup"><span data-stu-id="65d8d-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="65d8d-114">Nota skal síu sem er með `INTERCOMPANYORDER == ""` sem fyrirspurnarstreng.</span><span class="sxs-lookup"><span data-stu-id="65d8d-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Breyta svarglugga fyrirspurnar fyrir hausa CDS-sölupantana":::

3. <span data-ttu-id="65d8d-116">Útvíkka skal töfluna **Hausar CDS-sölupöntunar** með því að bæta tilvísun við dálkinn **IIntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="65d8d-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="65d8d-117">Þessi dálkur er aðeins fylltur út í samstæðupöntunum.</span><span class="sxs-lookup"><span data-stu-id="65d8d-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="65d8d-118">Dálkurinn **InterCompanyInventTransId** er í boði í töflunni **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="65d8d-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Varpa sviðsetningu á marksíðu fyrir línur CDS-sölupöntunar":::

4. <span data-ttu-id="65d8d-120">Þegar **CDS-sölupöntunarlínur** er útvíkkað er dálkurinn **IntercompanyInventTransId** aðgengilegur í vörpuninni.</span><span class="sxs-lookup"><span data-stu-id="65d8d-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="65d8d-121">Nota skal síu sem er með `INTERCOMPANYINVENTTRANSID == ""` sem fyrirspurnarstreng.</span><span class="sxs-lookup"><span data-stu-id="65d8d-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Breyta svarglugga fyrirspurnar fyrir línur CDS-sölupantana":::

5. <span data-ttu-id="65d8d-123">Endurtakið skref 1 og 2 til að víkka út töfluna **Sölureikningshaus V2** og bæta við síufyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="65d8d-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="65d8d-124">Í þessu tilviki skal nota `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` sem fyrirspurnarstreng fyrir síuna.</span><span class="sxs-lookup"><span data-stu-id="65d8d-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Varpa sviðsetningu á marksíðu fyrir sölureikningshaus V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Breyta svarglugga fyrirspurnar fyrir sölureikningshaus v2":::

6. <span data-ttu-id="65d8d-127">Endurtakið skref 3 og 4 til að víkka út töfluna **Sölureikningshaus V2** og bæta við síufyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="65d8d-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="65d8d-128">Í þessu tilviki skal nota `INTERCOMPANYINVENTTRANSID == ""` sem fyrirspurnarstreng fyrir síuna.</span><span class="sxs-lookup"><span data-stu-id="65d8d-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Breyta svarglugga fyrirspurnar fyrir sölureikningslínur V2":::

7. <span data-ttu-id="65d8d-130">Taflan **Tilboð** er ekki með vensl innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="65d8d-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="65d8d-131">Ef einhver stofnar tilboð fyrir einn af viðskiptavinum innan samstæðu er hægt dálkinn **CustGroup** til að setja alla þessa viðskiptavini í einn viðskiptavinaflokk.</span><span class="sxs-lookup"><span data-stu-id="65d8d-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="65d8d-132">Hægt er að víkka út hausinn og línurnar með því að bæta við dálkinum **CustGroup** og síðan sía þannig að flokkurinn sé ekki tekinn með.</span><span class="sxs-lookup"><span data-stu-id="65d8d-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Varpa sviðsetningu á marksíðu fyrir CDS-sölutilboðshaus":::

8. <span data-ttu-id="65d8d-134">Þegar **Tilboð** hafa verið víkkuð út skal nota síu sem er með `CUSTGROUP != "<company>"` sem fyrirspurnarstreng.</span><span class="sxs-lookup"><span data-stu-id="65d8d-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Breyta svarglugga fyrirspurnar fyrir CDS-sölutilboðshaus":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]