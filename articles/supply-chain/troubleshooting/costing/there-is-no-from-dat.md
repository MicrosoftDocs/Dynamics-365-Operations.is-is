---
title: Engin frá-dagsetning er í flipa virkra verða á síðu vöruverðs.
description: Engin frá-dagsetning er í flipa virkra verða á síðu vöruverðs.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026624"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="b7768-103">Engin frá-dagsetning er í flipa virkra verða á síðu vöruverðs.</span><span class="sxs-lookup"><span data-stu-id="b7768-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="b7768-104">KB númer: 4613548</span><span class="sxs-lookup"><span data-stu-id="b7768-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="b7768-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="b7768-105">Symptoms</span></span>

<span data-ttu-id="b7768-106">Ekkert **Frá-dagsetning** gildi er í flipa **Virkra verða** á síðu **Vöruverðs**.</span><span class="sxs-lookup"><span data-stu-id="b7768-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="b7768-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="b7768-107">Resolution</span></span>

<span data-ttu-id="b7768-108">Gildið **Frá dagsetningu** (gildistími) sem er stillt á biðverðinu færist ekki yfir á virka verðið.</span><span class="sxs-lookup"><span data-stu-id="b7768-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="b7768-109">Þegar kostnaðarfærsla vöru er upphaflega færð inn hefur hún stöðuna *Í biðstöðu* og ætlaða upphafsdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="b7768-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="b7768-110">Þegar kostnaðarfærsla vöru er virkjuð uppfærist staðan í *Virk* og gildisdagsetningin er uppfærð í virkjunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="b7768-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="b7768-111">Því er virkjunardagsetning virks verðs alltaf raundagsetning virkjunarinnar.</span><span class="sxs-lookup"><span data-stu-id="b7768-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="b7768-112">Frekari upplýsingar eru í [Yfirlit kostnaðarútgáfa](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="b7768-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
