--- 
title: "Stofna snið fyrir talningu og samlagningu í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: efdb64fa157af0d96c2ff0e5de3db5a98190bc68
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="5098e-103">Stofna snið fyrir talningu og samlagningu í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="5098e-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5098e-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="5098e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="5098e-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="5098e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5098e-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="5098e-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="5098e-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="5098e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="5098e-108">Fá aðgang að lista yfir skilgreiningar sem Microsoft veitir</span><span class="sxs-lookup"><span data-stu-id="5098e-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="5098e-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="5098e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="5098e-110">Gakktu úr skugga um að „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="5098e-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="5098e-111">veitandi sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="5098e-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="5098e-112">Velja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5098e-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="5098e-113">veita.</span><span class="sxs-lookup"><span data-stu-id="5098e-113">provider.</span></span>
3. <span data-ttu-id="5098e-114">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="5098e-114">Click Repositories.</span></span>
    * <span data-ttu-id="5098e-115">Sleppa önnur þrep í núverandi undirverki ef gagnasafn af gerð 'Rekstrartilföngum' er þegar til.</span><span class="sxs-lookup"><span data-stu-id="5098e-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="5098e-116">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5098e-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="5098e-117">Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".</span><span class="sxs-lookup"><span data-stu-id="5098e-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="5098e-118">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="5098e-118">Click Create repository.</span></span>
7. <span data-ttu-id="5098e-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5098e-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="5098e-120">Sækja Intrastat-skilgreiningar sem Microsoft veitir</span><span class="sxs-lookup"><span data-stu-id="5098e-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="5098e-121">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="5098e-121">Click Open.</span></span>
2. <span data-ttu-id="5098e-122">Í trénu skal velja 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="5098e-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="5098e-123">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="5098e-123">Click Import.</span></span>
    * <span data-ttu-id="5098e-124">Smelltu á innflutning fyrir útgáfu 1.1 fyrir valda skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="5098e-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="5098e-125">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="5098e-125">Click Yes.</span></span>
5. <span data-ttu-id="5098e-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5098e-126">Close the page.</span></span>
6. <span data-ttu-id="5098e-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5098e-127">Close the page.</span></span>
7. <span data-ttu-id="5098e-128">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5098e-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="5098e-129">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="5098e-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="5098e-130">Í trénu skal velja 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="5098e-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


