---
title: Ákvarða uppskriftarútgáfu
description: Á meðan á niðurbroti eftirspurnar stendur, ef vara hefur gerð sjálfgefinnar vöru stillta á framleiðslu finnur áætlunarforritið gilda uppskriftarútgáfu byggða á svæði.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4fd5f28d0ee85c267ea6a86a1452fbacc824620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833618"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="8e089-103">Ákvarða uppskriftarútgáfu</span><span class="sxs-lookup"><span data-stu-id="8e089-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e089-104">Á meðan á niðurbroti eftirspurnar stendur, ef vara hefur gerð sjálfgefinnar vöru stillta á framleiðslu finnur áætlunarforritið gilda uppskriftarútgáfu byggða á svæði.</span><span class="sxs-lookup"><span data-stu-id="8e089-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="8e089-105">Svæðavíddin er alltaf þekkt og er tilgreind í eftirspurnarfærslu.</span><span class="sxs-lookup"><span data-stu-id="8e089-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="8e089-106">Aðferðin við að ákvarða hvaða uppskriftarútgáfu á að nota er sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="8e089-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="8e089-107">Ef uppskriftarútgáfa hefur verið skilgreind fyrir vöruna í eftirspurnarsvæðinu, notar forritið þessa svæðistengdu uppskrift.</span><span class="sxs-lookup"><span data-stu-id="8e089-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="8e089-108">Ef svæðistengd uppskriftarútgáfa hefur ekki verið skilgreind fyrir vöruna í eftirspurnarsvæðinu, notar forritið almenna uppskriftarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="8e089-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="8e089-109">Almenn uppskrift tilgreinir ekki svæði og gildir um mörg svæði.</span><span class="sxs-lookup"><span data-stu-id="8e089-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="8e089-110">Ef til er almenn uppskrift, notar forritið hana.</span><span class="sxs-lookup"><span data-stu-id="8e089-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="8e089-111">Ef engin almenn uppskrift er fyrir hendi, stöðvast niðurbrot eftirspurnar á þessum tímapunkti.</span><span class="sxs-lookup"><span data-stu-id="8e089-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="8e089-112">Gild uppskriftarútgáfa, hvort sem hún er svæðistengd eða almenn, verður að uppfylla nauðsynlegar kröfur varðandi dagsetningu og magn.</span><span class="sxs-lookup"><span data-stu-id="8e089-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]