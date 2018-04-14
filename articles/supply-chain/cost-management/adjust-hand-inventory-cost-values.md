---
title: "Leiðrétta kostnaðarvirði lagerbirgða"
description: "Hægt er að nota síðuna Leiðrétting á lagermagni til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokun vinnslu er keyrð."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 121b5e15912b9ecbf26f8831fdaef7637390cdd0
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="db258-103">Leiðrétta kostnaðarvirði lagerbirgða</span><span class="sxs-lookup"><span data-stu-id="db258-103">Adjust on-hand inventory cost values</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="db258-104">Hægt er að nota síðuna Leiðrétting á lagermagni til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokun vinnslu er keyrð.</span><span class="sxs-lookup"><span data-stu-id="db258-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="db258-105">Hægt er að nota **Leiðrétting á lagerbirgðum** síðuna til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokunarvinnsla er keyrð.</span><span class="sxs-lookup"><span data-stu-id="db258-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="db258-106">**Ábending:** til Að opna síðuna **Leiðrétting á lagerbirgðum** veljið skýrsluna um lokið birgðalokunarferli á síðunni **Lokun og leiðrétting** og smellið síðan á **Leiðrétting** &gt; **Lager**.</span><span class="sxs-lookup"><span data-stu-id="db258-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="db258-107">**Dæmi:**Eftirfarandi færslur eru í febrúar:</span><span class="sxs-lookup"><span data-stu-id="db258-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="db258-108">1. febrúar: Fjárhagsleg innhreyfing birgða með magninu 2 á verðinu USD 10,00.</span><span class="sxs-lookup"><span data-stu-id="db258-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="db258-109">5. febrúar: Fjárhagsleg innhreyfing birgða með magninu 1 á verðinu USD 13,00.</span><span class="sxs-lookup"><span data-stu-id="db258-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="db258-110">19. febrúar: Fjárhagsleg úthreyfing birgða með magninu 1 á meðalkostnaðarverðinu USD 11,00.</span><span class="sxs-lookup"><span data-stu-id="db258-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="db258-111">Þessi vara var sett upp með birgðalíkaninu Fyrst inn, fyrst út (FIFO), og birgðalokunin var framkvæmd frá og með 28. febrúar.</span><span class="sxs-lookup"><span data-stu-id="db258-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="db258-112">Fjárhagsleg úthreyfingarfærsla upp á 11.00 USD verður jöfnuð við fjárhagslegu innhreyfinguna þann 1. febrúar og gerð verður jöfnun upp á 1,00 USD.</span><span class="sxs-lookup"><span data-stu-id="db258-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="db258-113">Eftirfarandi birgðainnhreyfingar munu þá innihalda opið birgðamagn:</span><span class="sxs-lookup"><span data-stu-id="db258-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="db258-114">1. febrúar: Magnið 1 á verðinu 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="db258-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="db258-115">5. febrúar: Magnið 1 á verðinu 13.00 USD</span><span class="sxs-lookup"><span data-stu-id="db258-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="db258-116">Ef stilla á kostnað þessara tveggja vara á USD 15.00 skal nota valkostinn um leiðréttingu lagerbirgða til að leiðrétta opna lagerbirgðamagnið frá síðasta birgðalokunartímabili.</span><span class="sxs-lookup"><span data-stu-id="db258-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="db258-117">**Ábending:**Bókunardagsetning lagerbirgðaleiðréttingarfærslunnar verður dagsetning síðustu birgðalokunar.</span><span class="sxs-lookup"><span data-stu-id="db258-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="db258-118">Ekki er hægt að breyta þessari dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="db258-118">This date can't be modified.</span></span>

