---
title: "Rafrænu skýrslugerðarsniði breytt með því að endurnýta Microsoft Excel-sniðmát"
description: "Þetta umræðuefni veitir upplýsingar um hvernig hægt er að breyta sniði rafrænnar skýrslugerðar (ER) sem er notað til að búa til viðskiptaskjöl með því að endurnota breytt Excel-sniðmát."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: eb0a37acebb61c7f4f06724bf0234211072f1e98
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a><span data-ttu-id="1a517-103">Rafrænu skýrslugerðarsniði breytt með því að endurnýta Microsoft Excel-sniðmát</span><span class="sxs-lookup"><span data-stu-id="1a517-103">Modify an Electronic reporting format by reapplying a Microsoft Excel template</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="1a517-104">Rafræn skýrslugerð (ER) tólið er notað til að búa til viðskiptaskjöl á rafrænu formi.</span><span class="sxs-lookup"><span data-stu-id="1a517-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="1a517-105">Til að búa til viðskiptaskjöl verður að búa til ER-snið og nota síðan ER-hönnuður til að skilgreina útlit viðskiptaskjalsins og tilgreina þau gögn sem eiga að vera með í því.</span><span class="sxs-lookup"><span data-stu-id="1a517-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="1a517-106">Þú getur þá keyrt ER-sniðið til að búa til viðskiptaskjalið.</span><span class="sxs-lookup"><span data-stu-id="1a517-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="1a517-107">ER tólið er hægt að nota til að búa til viðskiptaskjöl í formi Microsoft Excel-skráa.</span><span class="sxs-lookup"><span data-stu-id="1a517-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="1a517-108">Hægt er að nota Excel-skjal sem sniðmát fyrir þessi skjöl.</span><span class="sxs-lookup"><span data-stu-id="1a517-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="1a517-109">Til að skilgreina útlit skjalsins í ER hönnuður, er hægt að flytja efni Excel-skjalsins sem þú vilt nota sem sniðmát inn í skilgreint ER sniðið.</span><span class="sxs-lookup"><span data-stu-id="1a517-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="1a517-110">Fyrir frekari upplýsingar og til að æfa þig í þessum aðstæðum,  skaltu spila verkleiðbeiningarnar **ER Hanna skilgreiningu fyrir myndun skýrslna í OPENXML-sniði** (hluti af 7.5.4.3 Acquire/Develop IT service/solution components (10677) viðskiptaferli).</span><span class="sxs-lookup"><span data-stu-id="1a517-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="1a517-111">Ef þú breytir Excel-skjalinu sem er notað sem sniðmát fyrir viðskiptaskjal, gerir ný ER-virkni þér kleift að endurnota uppfært sniðmátið á ER-sniðið.</span><span class="sxs-lookup"><span data-stu-id="1a517-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="1a517-112">ER-sniðið er síðan uppfært þannig að það fylgir uppfærða sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="1a517-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="1a517-113">Til að fá frekari upplýsingar um þessa virkni, skaltu spila verkleiðbeiningarnar **ER Hanna snið með því að endurnota Excel-sniðmát** (hluti af 7.5.5.3 Acquire/Develop IT service/solution components (10683) viðskiptaferli).</span><span class="sxs-lookup"><span data-stu-id="1a517-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="1a517-114">Í skrefinu í verkleiðbeiningunum þar sem þú flytur inn uppfært sniðmát, skaltu nota breytt sniðmát Greiðsluskýrsla Excel-skrárinnar, SampleVendPaymWsReport2, sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="1a517-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

