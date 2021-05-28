---
title: Ekki er hægt að fjarlægja vídd eftirspurnarspár vöruhúss úr spárlínum.
description: Ekki er hægt að fjarlægja vídd eftirspurnarspár vöruhúss úr spárlínum.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026612"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="3012f-103">Ekki er hægt að fjarlægja vídd eftirspurnarspár vöruhúss úr spárlínum.</span><span class="sxs-lookup"><span data-stu-id="3012f-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="3012f-104">KB númer: 4614408</span><span class="sxs-lookup"><span data-stu-id="3012f-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="3012f-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="3012f-105">Symptoms</span></span>

<span data-ttu-id="3012f-106">Þetta vandamál kemur upp þegar víddin **Vöruhús** er ekki úthlutuð á flipanum **Spávíddir** á síðunni **færibreyta Eftirspurnarspár**.</span><span class="sxs-lookup"><span data-stu-id="3012f-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="3012f-107">Engu að síður er dálkurinn **Vöruhús** sýndur á **Eftirspurnarspá** síðunni (**Aðaláætlanagerð \> Spá \> Handvirk spáeining \> Eftirspurnarspárlínur**).</span><span class="sxs-lookup"><span data-stu-id="3012f-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="3012f-108">Upplausn</span><span class="sxs-lookup"><span data-stu-id="3012f-108">Resolution</span></span>

<span data-ttu-id="3012f-109">Stillingarnar á flipanum **Spávíddir** á síðunni **Færibreyta eftirspurnarspár** hafa ekki áhrif á síðuna **Eftirspurnarspá**.</span><span class="sxs-lookup"><span data-stu-id="3012f-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="3012f-110">Þeir stjórna grunnspánni sem myndast og kemur fram í leiðréttu eftirspurnarspánni.</span><span class="sxs-lookup"><span data-stu-id="3012f-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="3012f-111">Hins vegar stjórna þeir ekki víddum sem krafist er fyrir „raunverulega“ eftirspurnarspá.</span><span class="sxs-lookup"><span data-stu-id="3012f-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="3012f-112">Með því að heimila færslurnar sem birtast á síðunni **Leiðrétt eftirspurnarspá** getur þú breytt þeim í „raunverulegar“ spárfærslur fyrir spárlíkan.</span><span class="sxs-lookup"><span data-stu-id="3012f-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="3012f-113">Það líkan er síðan hægt að nota í aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="3012f-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="3012f-114">Á síðunni **Eftirspurnarspá** eru víddirnar fyrir „raunverulega“ spá sem birtar eru á eftirspurnarspálínunum hluti af birgðavíddum.</span><span class="sxs-lookup"><span data-stu-id="3012f-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="3012f-115">(Þessi hegðun líkist hegðun sölupöntunarlína.) Ef kerfið er ekki sett upp til að nota **Vöruhús** sem skylduvídd fyrir birgðir er hægt að sérstilla síðuna til að fela dálkinn.</span><span class="sxs-lookup"><span data-stu-id="3012f-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
