---
title: Flytja eign
description: Þessi verkefnaleiðbeiningar fyrir verk flytja fjárhagsupplýsingar fyrir eignabók úr einni fjárhagsvíddasamstæða í nýja fjárhagsvíddasamstæða.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "357198"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="2d2d9-103">Flytja eign</span><span class="sxs-lookup"><span data-stu-id="2d2d9-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d2d9-104">Þessi verkefnaleiðbeiningar fyrir verk flytja fjárhagsupplýsingar fyrir eignabók úr einni fjárhagsvíddasamstæða í nýja fjárhagsvíddasamstæða.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="2d2d9-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="2d2d9-106">Fara í Eignir > Eignir > Eignir.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="2d2d9-107">Finna og velja eign sem á að flytja, á listanum.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="2d2d9-108">Á Aðgerðasvæðinu skal smellt á eign.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="2d2d9-109">Smellt er á Flytja eignir.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="2d2d9-110">Dagsetning er rituð í reitinn Dagsetning millifærslu.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="2d2d9-111">Færa inn athugasemdir til að lýsa flutninginn.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="2d2d9-112">Þessi listi sýnir allar bækur fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="2d2d9-113">Merkja bækur sem á að flytja í nýtt fjárhagsvíddasamstæða.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="2d2d9-114">Listinn sýnir núverandi gildi fjárhagsvídda fyrir valda bók.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="2d2d9-115">Velja fjárhagsvídd til að uppfæra fyrir valda eignabók.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="2d2d9-116">Í reitnum fjárhagsvídd skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="2d2d9-117">Stilla aðra fjárhagsvíddargildi sem viðeigandi.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="2d2d9-118">Öllum fjárhagsvíddargildum breyta þegar flutningur fer fram, hvort sem hefur verið fært inn gildi eða skilið eftir autt.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="2d2d9-119">Til dæmis, ef fært er inn gildi fyrir BusinessUnit (fyrirtækjaeining) og hafðir CostCenter (kostnaðarstað) fjárhagslegar víddir autt.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="2d2d9-120">Ef reikningsskipulagið leyfði auð gildi fyrir CostCenter og Deild, myndi flutningurinn leiða til þess að hvert virðislíkan hefur nýtt gildi fyrir BusinessUnit (fyrirtækjaeining) og tómt gildi fyrir CostCenter og deild.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="2d2d9-121">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-121">Click Update.</span></span>
    * <span data-ttu-id="2d2d9-122">Það verður tækifæri til að forskoða breytingar áður en ljúka flutningi.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="2d2d9-123">Skoða niðurstöður áður en eignabækur fluttar.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="2d2d9-124">Smelltu á Flutningur.</span><span class="sxs-lookup"><span data-stu-id="2d2d9-124">Click Transfer.</span></span>

