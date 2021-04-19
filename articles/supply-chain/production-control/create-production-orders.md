---
title: Yfirlit yfir líftíma framleiðslupöntunar
description: Þegar framleiðslupöntun er stofnuð er send beiðni um að hefja framleiðslu vöru. Framleiðslupöntunin inniheldur upplýsingar um það hvað verður framleitt, hversu mikið magn og áætluðu lokadagsetninguna. Hann inniheldur einnig upplýsingar um hvaða efni á að nota og hvaða ferli skuli fylgja til að framleiða vöruna.
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df773cf13b8ccd9ee4f861955b1a4321af38a150
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811799"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="36803-105">Yfirlit yfir líftíma framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="36803-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36803-106">Þegar framleiðslupöntun er stofnuð er send beiðni um að hefja framleiðslu vöru.</span><span class="sxs-lookup"><span data-stu-id="36803-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="36803-107">Framleiðslupöntunin inniheldur upplýsingar um það hvað verður framleitt, hversu mikið magn og áætluðu lokadagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="36803-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="36803-108">Hann inniheldur einnig upplýsingar um hvaða efni á að nota og hvaða ferli skuli fylgja til að framleiða vöruna.</span><span class="sxs-lookup"><span data-stu-id="36803-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="36803-109">Framleiðslupöntun gengur í gegnum stig framleiðsluferlisins.</span><span class="sxs-lookup"><span data-stu-id="36803-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="36803-110">Þegar pöntun er stofnuð er henni úthlutað stöðunni **Stofnuð**.</span><span class="sxs-lookup"><span data-stu-id="36803-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="36803-111">Þegar pöntun er lokið er henni úthlutað stöðunni **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="36803-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="36803-112">Færibreytustilling í hverju°stigi heimilar notandanum að skilgreina hvert°skref.</span><span class="sxs-lookup"><span data-stu-id="36803-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="36803-113">Stillingin getur verið stillt fyrir°einn notanda°eða fyrir alla notendur.</span><span class="sxs-lookup"><span data-stu-id="36803-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="36803-114">Framleiðsluuppskrift og leið í framleiðslu eru aðal einingar framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="36803-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="36803-115">Þær eru afritaðar í framleiðslupöntunina byggt á völdu vörunni og magni sem á að framleiða.</span><span class="sxs-lookup"><span data-stu-id="36803-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="36803-116">Áður en framleiðslupöntun er ræst, er hægt að breyta framleiðsluuppskrift og leið.</span><span class="sxs-lookup"><span data-stu-id="36803-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="36803-117">Hægt er að stofna framleiðslupöntun við eftirfarandi kringumstæður:</span><span class="sxs-lookup"><span data-stu-id="36803-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="36803-118">Stofnað með framkvæmd aðaláætlunar byggt á eftirspurn efnis.</span><span class="sxs-lookup"><span data-stu-id="36803-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="36803-119">Stofnuð beint úr sölupöntunarlínu eða þegar framleiðslupöntun á hærra stigi er stofnuð og metin (fest framboð).</span><span class="sxs-lookup"><span data-stu-id="36803-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="36803-120">Stofnaðar handvirkt.</span><span class="sxs-lookup"><span data-stu-id="36803-120">Created manually.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]