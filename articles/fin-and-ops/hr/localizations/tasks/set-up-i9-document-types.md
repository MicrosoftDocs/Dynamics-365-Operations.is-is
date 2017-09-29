--- 
title: "Setja upp I-9 skjalagerðir"
description: "Þessi ferli sýnir hvernig á að skoða og setja upp skjalagerðir sem eru notaðar til að staðfesta I-9."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="981af-103">Setja upp I-9 skjalagerðir</span><span class="sxs-lookup"><span data-stu-id="981af-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="981af-104">Þessi ferli sýnir hvernig á að skoða og setja upp skjalagerðir sem eru notaðar til að staðfesta I-9.</span><span class="sxs-lookup"><span data-stu-id="981af-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="981af-105">Áður en að setja upp skjalagerðir I-9, þarf einnig að setja upp útgáfuaðila og gerð auðkennis.</span><span class="sxs-lookup"><span data-stu-id="981af-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="981af-106">Sýnigögn gögn fyrirtækisins til að stofna þetta ferli er USMF, þar á meðal eru dæmi um útgáfuaðila og gerð auðkennis sem þarf til að ljúka ferlinu.</span><span class="sxs-lookup"><span data-stu-id="981af-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="981af-107">Farið í Mannauður > Starfsmenn > I-9 > I-9 skjalagerðir.</span><span class="sxs-lookup"><span data-stu-id="981af-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="981af-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="981af-108">Click New.</span></span>
3. <span data-ttu-id="981af-109">Í reitinn Gerð I-9 skjals skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="981af-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="981af-110">Dæmi: Skólakenni</span><span class="sxs-lookup"><span data-stu-id="981af-110">Example: School ID.</span></span>  
4. <span data-ttu-id="981af-111">Veldu gerð auðkennis.</span><span class="sxs-lookup"><span data-stu-id="981af-111">Select the identification type.</span></span>  <span data-ttu-id="981af-112">Dæmi: Skólakenni</span><span class="sxs-lookup"><span data-stu-id="981af-112">Example:  School ID</span></span>
    * <span data-ttu-id="981af-113">Dæmi um gerðir auðkenna er kennitala (SSN), númer vegabréfsáritunar, Kenni passa, eða ökuskírteini.</span><span class="sxs-lookup"><span data-stu-id="981af-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="981af-114">Veljið I-9 skjalalista sem notaður er fyrir gerð skjals.</span><span class="sxs-lookup"><span data-stu-id="981af-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="981af-115">Hluti af ferlinu I-9 er að starfsmenn verður að veita fylgiskjal sem sýnir vinnuveitanda þeirra auðkenni og heimild til ráðningar.</span><span class="sxs-lookup"><span data-stu-id="981af-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="981af-116">Vefsvæðið fyrir Ríkisborgararétt í BNA og innflytjendaþjónustu inniheldur upplýsingar um hvaða skjöl eru viðunandi og hvaða lista þeir tilheyra.</span><span class="sxs-lookup"><span data-stu-id="981af-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="981af-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="981af-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="981af-118">Í reitnum Eyðublað er færður inn kóði fyrir gerð skjals.</span><span class="sxs-lookup"><span data-stu-id="981af-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="981af-119">Dæmi: Skólakenni</span><span class="sxs-lookup"><span data-stu-id="981af-119">Example: School ID.</span></span>
    * <span data-ttu-id="981af-120">Opinber Númer eyðublaðanna má finna á vefsíðu ríkisborgararéttar BNA og innflytjendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="981af-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="981af-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="981af-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="981af-122">Merkið eða afmerkið reitinn Virkur.</span><span class="sxs-lookup"><span data-stu-id="981af-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="981af-123">Í svæðinu Rennur út, setja dagsetningu á ' 2019 10 27'.</span><span class="sxs-lookup"><span data-stu-id="981af-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="981af-124">Lokadagur er valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="981af-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="981af-125">Velja útgáfuaðilinn sem gaf út gerð skjals.</span><span class="sxs-lookup"><span data-stu-id="981af-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="981af-126">Dæmi: fylki/umdæmi</span><span class="sxs-lookup"><span data-stu-id="981af-126">Example: Province/territory</span></span>
10. <span data-ttu-id="981af-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="981af-127">Click Save.</span></span>


