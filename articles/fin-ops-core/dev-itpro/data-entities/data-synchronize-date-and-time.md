---
title: Samstilla dagsetningu og tíma í innflutningsvinnslum
description: Notið UTC-tíma í innflutningsverkum til að forðast vandamál varðandi umreikning tímabelta.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748670"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="6aefc-103">Samstilla dagsetningu og tíma í innflutningsvinnslum</span><span class="sxs-lookup"><span data-stu-id="6aefc-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6aefc-104">Mikilvægt er að stilla tímabelti fyrir innflutningsverkið á samræmdan heimstíma (UTC).</span><span class="sxs-lookup"><span data-stu-id="6aefc-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="6aefc-105">Óvæntar dagsetningar og tímar gætu sést í innfluttum gögnum ef önnur stilling er notuð.</span><span class="sxs-lookup"><span data-stu-id="6aefc-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="6aefc-106">Án réttrar stillingar mun innflutningsferlið umbreyta UTC-dagsetningunni í staðbundna sniðið og kerfisstillingarnar umbreyta því síðan aftur.</span><span class="sxs-lookup"><span data-stu-id="6aefc-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="6aefc-107">Þessi tvöfaldi umreikningur veldur því að dagsetningar breytast milli forrita.</span><span class="sxs-lookup"><span data-stu-id="6aefc-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="6aefc-108">Til dæmis gæti tvöfaldur umreikningur valdið því að upphafsdagsetning starfsmanns verði mismunandi á milli Dynamics 365 Human Resources og Dynamics 365 Finance vegna mismunar í staðbundnum tímabeltum.</span><span class="sxs-lookup"><span data-stu-id="6aefc-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="6aefc-109">Að stilla innflutningsverkið á UTC leysir úr þessum vanda.</span><span class="sxs-lookup"><span data-stu-id="6aefc-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="6aefc-110">Í Dynamics 365 Finance and Operations skal velja **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="6aefc-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="6aefc-111">Veljið **Flytja inn verk** og veljið síðan verkið.</span><span class="sxs-lookup"><span data-stu-id="6aefc-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="6aefc-112">Undir **Dagsetningarsnið uppruna** skal velja **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="6aefc-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="6aefc-113">[![Breyta dagsetningarsniði uppruna í UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="6aefc-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="6aefc-114">Breytið **Tímabelti** í **Samræmdan heimstíma** og breytið **Tungumáli** í **En-Us**.</span><span class="sxs-lookup"><span data-stu-id="6aefc-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]