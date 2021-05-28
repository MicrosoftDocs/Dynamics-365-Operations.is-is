---
title: Kerfisstjórar geta ekki aflétt biðstöðu pöntunar vegna þess að þeir hafa ekki heimild til þess
description: Kerfisstjórar geta ekki aflétt biðstöðu pöntunar vegna þess að þeir hafa ekki heimild til þess.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026626"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="e0f3e-103">Kerfisstjórar geta ekki aflétt biðstöðu pöntunar vegna þess að þeir hafa ekki heimild til þess</span><span class="sxs-lookup"><span data-stu-id="e0f3e-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="e0f3e-104">KB númer: 4614642</span><span class="sxs-lookup"><span data-stu-id="e0f3e-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="e0f3e-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="e0f3e-105">Symptoms</span></span>

<span data-ttu-id="e0f3e-106">Kerfisstjórnendur geta ekki hreinsað sölupantanir í bið nema þeir séu í því hlutverki sem er úthlutað í biðpöntunarkóðanum.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="e0f3e-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="e0f3e-107">Resolution</span></span>

<span data-ttu-id="e0f3e-108">Aðgangur að sumum aðgerðum, svo sem að hreinsa bið sölupöntunar, er drifinn af uppsetningu viðskiptastefnu.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="e0f3e-109">Kerfisstjórar hafa yfirleitt ekki heimild til að framkvæma aðgerðir af þessari gerð.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="e0f3e-110">Oftar fer aðgangur að ákveðnu verkefni eftir viðskiptastefnum og einungis tilteknir aðilar í fyrirtæki eru samþykktir til að framkvæma það verkefni.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="e0f3e-111">Sem dæmi má nefna samþykki sem eru afleiðing vinnuflæðisamþykktar og sérstök verkefni sem eru afleiðing vinnuflæðistillingar.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="e0f3e-112">Þrátt fyrir að ekkert vinnuflæði sé tengt við pöntun er aðferðin svipuð.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="e0f3e-113">Viðeigandi hlutverk tilnefnir þann tiltekna hóp fólks í fyrirtækjum sem hefur rétt á að hreinsa pantanir í bið.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="e0f3e-114">Þennan rétt ætti ekki endilega að veita öllum stjórnendum því sú nálgun brýtur í bága við skilgreinda viðskiptastefnu.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
