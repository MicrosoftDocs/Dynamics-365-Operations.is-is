---
title: Áætlaðar verkbeiðnir viðhaldsvinnsla
description: Þetta efni útskýrir tímasettar verkbeiðnir um viðhaldsverk í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b3cc32d6ff263967c1ee843702c28968219ac33
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887183"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="13c7c-103">Áætlaðar verkbeiðnir viðhaldsvinnsla</span><span class="sxs-lookup"><span data-stu-id="13c7c-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="13c7c-104">Síðan **Skipulögð viðhaldsverk verkbeiðna** er notuð til að fá yfirlit yfir verkbeiðnir sem úthlutað er á tilföng.</span><span class="sxs-lookup"><span data-stu-id="13c7c-104">The **Scheduled work order maintenance jobs** page is used to get an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="13c7c-105">Verkbeiðnir sem nota tilfangagerðirnar „Mannauður“, „Verkfæri“ og „Vél“ eru sýndar á listanum.</span><span class="sxs-lookup"><span data-stu-id="13c7c-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown in the list.</span></span> <span data-ttu-id="13c7c-106">Hægt er að nota listann til að fá yfirsýn yfir verkbeiðnir sem úthlutaðar eru á tiltekin tilföng.</span><span class="sxs-lookup"><span data-stu-id="13c7c-106">The list can be used to get an overview of work orders allocated to a specific resource.</span></span> <span data-ttu-id="13c7c-107">Þú getur líka notað það til að finna fljótt verkbeiðni sem er úthlutað til viðhaldsstarfsmanns sem til dæmis tilkynnti sig veikan í morgun og úthluta síðan öðrum viðhaldsstarfsmanni til verksins fljótt.</span><span class="sxs-lookup"><span data-stu-id="13c7c-107">You can also use it to quickly find a work order allocated to a maintenance worker who, for example, called in sick this morning, and then quickly allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="13c7c-108">Skoða áætlaðar verkbeiðnir viðhaldsvinnsla</span><span class="sxs-lookup"><span data-stu-id="13c7c-108">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="13c7c-109">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Skipulagðar verkbeiðnir um viðhaldsverk**.</span><span class="sxs-lookup"><span data-stu-id="13c7c-109">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="13c7c-110">Þú sérð lista yfir allar verkbeiðnir sem eru stilltar á líftímastöðu verkbeiðni „Skipulögð“ eða „Í vinnslu“.</span><span class="sxs-lookup"><span data-stu-id="13c7c-110">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="13c7c-111">Þú getur flokkað listann, til dæmis eftir viðhaldsstarfsmanni.</span><span class="sxs-lookup"><span data-stu-id="13c7c-111">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="13c7c-112">Þú getur líka notað síuna til að takmarka listann til að birta verkbeiðnir sem eru úthlutaðar á tiltekin tilföng eða viðhaldsstarfsmann.</span><span class="sxs-lookup"><span data-stu-id="13c7c-112">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="13c7c-113">Þú getur séð minnispunkta um verkbeiðnina og, ef þörf krefur, bætt við nýjum athugasemdum með því að velja verkbeiðniverkin á listanum og smella á **Minnispunktar**.</span><span class="sxs-lookup"><span data-stu-id="13c7c-113">You can see notes on the work order and, if required, add new notes by selecting the work order job in the list and clicking **Notes**.</span></span>

4. <span data-ttu-id="13c7c-114">Ef þú vilt úthluta einum viðhaldsstarfsmanni á verkbeiðni skaltu velja verkbeiðnina á listanum og smella á **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="13c7c-114">If you want to allocate one maintenance worker to a work order, select the work order in the list, and click **Work order**.</span></span>

5. <span data-ttu-id="13c7c-115">Síðan **Verkbeiðni** opnast.</span><span class="sxs-lookup"><span data-stu-id="13c7c-115">The **Work order** page opens.</span></span> <span data-ttu-id="13c7c-116">Smelltu á **Senda** til að skipuleggja verkbeiðnina til ákveðins viðhaldsstarfsmanns.</span><span class="sxs-lookup"><span data-stu-id="13c7c-116">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="13c7c-117">Lestu meira um tímasetningu nokkurra verkbeiðna eða einnar verkbeiðni í [Skipuleggja verkbeiðnir](../work-order-scheduling/schedule-work-orders.md) og [Senda vinnu röð](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="13c7c-117">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="13c7c-118">Myndin hér að neðan sýnir dæmi um síðuna **Skipulögð viðhaldsverk verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="13c7c-118">The figure below shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![Mynd 1](media/07-work-order-scheduling.png)

