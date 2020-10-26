---
title: Aðferð við hálfsársafskriftir
description: Þetta efnisatriði lýsir aðferðinni sem eignir nota til að reikna út afskriftir með hálfs ár reglu, sem reiknar út sex mánaða afskrift á fyrsta og síðasta þjónustuári eignarinnar.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55fb03cf08d8ec042aa8fb37fd1fb858d98279b1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977240"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="900d5-103">Aðferð við hálfsársafskriftir</span><span class="sxs-lookup"><span data-stu-id="900d5-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="900d5-104">Þetta efnisatriði lýsir aðferðinni sem er notuð í eignum til að reikna afskriftir með hálfs árs reglu.</span><span class="sxs-lookup"><span data-stu-id="900d5-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="900d5-105">Hálfs ára regla reiknar út sex mánaða afskrift á fyrsta og síðasta þjónustuári eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="900d5-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="900d5-106">Frekari upplýsingar um afskriftarreglur eru í [Afskriftaaðferðir og hefðir](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="900d5-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="900d5-107">Þegar þú notar sex mánaða afskriftarreglu notar kerfið kaupár eða það ár sem eignin var sett í þjónustu og reiknar síðan út fimm ára afskrift frá því ári og bætir svo við sex mánuðum..</span><span class="sxs-lookup"><span data-stu-id="900d5-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="900d5-108">Til að skýra þetta ferli skaltu ímynda þér eign sem var keypt fyrir 50.000 og sett í þjónustu í apríl 2020.</span><span class="sxs-lookup"><span data-stu-id="900d5-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="900d5-109">Einnig skal gera ráð fyrir að eignin sé með fimm ára þjónustutíma.</span><span class="sxs-lookup"><span data-stu-id="900d5-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="900d5-110">Fyrsta þjónustuári lýkur í desember 2020, sem þýðir að lok fimm ára líftíma eignarinnar verða í desember 2024.</span><span class="sxs-lookup"><span data-stu-id="900d5-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="900d5-111">Hálfs árs afskriftarregla bætir sex mánuði við líftíma eignarinnar, sem þýðir að líftíma hennar lýkur í júní 2025.</span><span class="sxs-lookup"><span data-stu-id="900d5-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="900d5-112">Árleg afskrift 50.000/5 = 10.000 mánaðarleg afskrift 10.000/12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="900d5-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="900d5-113">Fyrsta ársafskrift 10.000/2 = 5.000 og síðari mánaðarleg afskrift 5.000/9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="900d5-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="900d5-114">[![Afskriftaráætlun fyrir hálfs ára afskriftarreglu](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="900d5-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="900d5-115">Útvíkkuð afskriftartímabil sem er bætt við með hálfs ára reglu bjóða upp á nákvæmari úthlutanir afskrifta.</span><span class="sxs-lookup"><span data-stu-id="900d5-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="900d5-116">Sex mánaða reglan endurspeglar jafnari afskriftarkostnað, sem er gagnlegt fyrir skýrslugerð í rekstraryfirliti.</span><span class="sxs-lookup"><span data-stu-id="900d5-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
