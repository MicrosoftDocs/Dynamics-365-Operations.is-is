---
title: Búa til og tengja afgreiðslukassa
description: Þetta ferli sýnir hvernig á að stofna Afgreiðslukassi á sölustað (POS).
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ac75d390b8bbb94c6e039b374b51462d348e355
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057166"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="15811-103">Búa til og tengja afgreiðslukassa</span><span class="sxs-lookup"><span data-stu-id="15811-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="15811-104">Þetta ferli sýnir hvernig á að stofna Afgreiðslukassi á sölustað (POS).</span><span class="sxs-lookup"><span data-stu-id="15811-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="15811-105">Þessi aðferð notar sýnifyrirtækið USRT.</span><span class="sxs-lookup"><span data-stu-id="15811-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="15811-106">Fara í Retail og Commerce > Uppsetning rásar > Uppsetning smásölustaðar > Afgreiðslukassar.</span><span class="sxs-lookup"><span data-stu-id="15811-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="15811-107">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="15811-107">Click New.</span></span>
3. <span data-ttu-id="15811-108">Í reitnum númer afgreiðslukassa er fært inn kenni fyrir nýja afgreiðslukassann.</span><span class="sxs-lookup"><span data-stu-id="15811-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="15811-109">Kenni afgreiðslukassa inniheldur yfirleitt kóða sem hjálpa að varpa afgreiðslukassa í verslun sem hann tilheyrir, og staðsetningu innan verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="15811-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="15811-110">Færið inn lýsandi heiti fyrir afgreiðslukassann í svæðið Heiti.</span><span class="sxs-lookup"><span data-stu-id="15811-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="15811-111">Í reitinn verslunarnúmer skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="15811-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="15811-112">Sláið inn eða veldu gildi í reitnum vélbúnaður.</span><span class="sxs-lookup"><span data-stu-id="15811-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="15811-113">Vélbúnaðarreglur eru notaðar til að tilgreina jaðartæki sem munu tengjast afgreiðslukassa, svo sem peningaskúffuna og kvittanaprentarann.</span><span class="sxs-lookup"><span data-stu-id="15811-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="15811-114">Sláið inn eða veldu gildi í reitnum sjónræn forstilling.</span><span class="sxs-lookup"><span data-stu-id="15811-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="15811-115">Sjónrænar reglur eru notaðir til að tilgreina myndir í POS-bakgrunninum og innskráningarsíðunni, auk þema fyrir Sölustað.</span><span class="sxs-lookup"><span data-stu-id="15811-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="15811-116">Í reitnum kortamillifærslunúmer afgreiðslukassa skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="15811-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="15811-117">Kortamillifærslunúmer Afgreiðslukassa er notað til að upplýsa greiðsluvinnslu um það hvaða greiðslustaður er að senda beiðnir um heimild.</span><span class="sxs-lookup"><span data-stu-id="15811-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="15811-118">Þetta gildi er oft kallað "Kenni afgreiðslustöðvar" eða "TID".</span><span class="sxs-lookup"><span data-stu-id="15811-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="15811-119">Yfirleitt má finna TID á límmiða á greiðslutækinu.</span><span class="sxs-lookup"><span data-stu-id="15811-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="15811-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="15811-120">Click Save.</span></span>
