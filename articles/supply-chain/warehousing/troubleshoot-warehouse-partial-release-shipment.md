---
title: Úrræðaleit fyrir losun að hluta og hlutaafhendingar
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með hlutalosanir og hlutaafhendingar í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645949"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="e7b34-103">Úrræðaleit fyrir losun að hluta og hlutaafhendingar</span><span class="sxs-lookup"><span data-stu-id="e7b34-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7b34-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með hlutalosanir og hlutaafhendingar í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e7b34-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="e7b34-105">Losunarstaða sölupöntunar er áfram Losuð að hluta eftir að sölupöntunin hefur verið reikningsfærð.</span><span class="sxs-lookup"><span data-stu-id="e7b34-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e7b34-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="e7b34-106">Issue description</span></span>

<span data-ttu-id="e7b34-107">Sölupöntun er afhendingarpöntun en ein eða fleiri vörur á henni hafa annan flutningsmáta.</span><span class="sxs-lookup"><span data-stu-id="e7b34-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="e7b34-108">Þegar pöntunin hefur verið reikningsfærð er hún enn með útgáfustöðu *Losað að hluta*.</span><span class="sxs-lookup"><span data-stu-id="e7b34-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="e7b34-109">Til dæmis er sölupöntun með tvær vörur: eina fyrir afhendingu og eina fyrir tiltekt.</span><span class="sxs-lookup"><span data-stu-id="e7b34-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="e7b34-110">Bæði afhendingum og tiltekt hefur verið lokið.</span><span class="sxs-lookup"><span data-stu-id="e7b34-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="e7b34-111">Báðar línur hafa verið reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="e7b34-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="e7b34-112">Útgáfustaðan er hins vegar enn sýnd sem *Losað að hluta*, sem er villandi.</span><span class="sxs-lookup"><span data-stu-id="e7b34-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e7b34-113">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="e7b34-113">Issue resolution</span></span>

<span data-ttu-id="e7b34-114">Losunarstaðan á aðeins við um pöntunarlínur þar sem vörurnar eru virkjaðar fyrir vöruhúsastjórnun.</span><span class="sxs-lookup"><span data-stu-id="e7b34-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="e7b34-115">Þess vegna er útgáfustaðan enn *Losað að hluta* í þessum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="e7b34-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="e7b34-116">Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika.</span><span class="sxs-lookup"><span data-stu-id="e7b34-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="e7b34-117">Hægt er að bæta við viðbót sem hluta af fylgiseðli og reikningsfærsluferli til að uppfæra útgáfustöðu.</span><span class="sxs-lookup"><span data-stu-id="e7b34-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
