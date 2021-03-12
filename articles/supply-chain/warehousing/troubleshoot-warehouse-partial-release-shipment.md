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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 33323a8aed44cf19db6c2c937abcb09f7e05b6c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993953"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="f455d-103">Úrræðaleit fyrir losun að hluta og hlutaafhendingar</span><span class="sxs-lookup"><span data-stu-id="f455d-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f455d-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með hlutalosanir og hlutaafhendingar í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f455d-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="f455d-105">Losunarstaða sölupöntunar er áfram Losuð að hluta eftir að sölupöntunin hefur verið reikningsfærð.</span><span class="sxs-lookup"><span data-stu-id="f455d-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f455d-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="f455d-106">Issue description</span></span>

<span data-ttu-id="f455d-107">Sölupöntun er afhendingarpöntun en ein eða fleiri vörur á henni hafa annan flutningsmáta.</span><span class="sxs-lookup"><span data-stu-id="f455d-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="f455d-108">Þegar pöntunin hefur verið reikningsfærð er hún enn með útgáfustöðu *Losað að hluta*.</span><span class="sxs-lookup"><span data-stu-id="f455d-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="f455d-109">Til dæmis er sölupöntun með tvær vörur: eina fyrir afhendingu og eina fyrir tiltekt.</span><span class="sxs-lookup"><span data-stu-id="f455d-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="f455d-110">Bæði afhendingum og tiltekt hefur verið lokið.</span><span class="sxs-lookup"><span data-stu-id="f455d-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="f455d-111">Báðar línur hafa verið reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="f455d-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="f455d-112">Útgáfustaðan er hins vegar enn sýnd sem *Losað að hluta*, sem er villandi.</span><span class="sxs-lookup"><span data-stu-id="f455d-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f455d-113">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="f455d-113">Issue resolution</span></span>

<span data-ttu-id="f455d-114">Losunarstaðan á aðeins við um pöntunarlínur þar sem vörurnar eru virkjaðar fyrir vöruhúsastjórnun.</span><span class="sxs-lookup"><span data-stu-id="f455d-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="f455d-115">Þess vegna er útgáfustaðan enn *Losað að hluta* í þessum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="f455d-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="f455d-116">Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika.</span><span class="sxs-lookup"><span data-stu-id="f455d-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="f455d-117">Hægt er að bæta við viðbót sem hluta af fylgiseðli og reikningsfærsluferli til að uppfæra útgáfustöðu.</span><span class="sxs-lookup"><span data-stu-id="f455d-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
