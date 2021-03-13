---
title: Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 1 - Stofna snið)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að telja og gera samantekt sem byggist á gögnum fyrir þegar myndað úttak texta. (Hluti 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a3639b5ac28f8a571642e983906d658dabf05b1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093023"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="f4fc4-104">Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 1 - Stofna snið)</span><span class="sxs-lookup"><span data-stu-id="f4fc4-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4fc4-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="f4fc4-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f4fc4-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="f4fc4-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="f4fc4-109">Fá aðgang að lista yfir skilgreiningar sem Microsoft veitir</span><span class="sxs-lookup"><span data-stu-id="f4fc4-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f4fc4-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f4fc4-111">Gakktu úr skugga um að „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="f4fc4-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="f4fc4-112">veitandi sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="f4fc4-113">Veldu „Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="f4fc4-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="f4fc4-114">veita.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-114">provider.</span></span>
3. <span data-ttu-id="f4fc4-115">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-115">Click Repositories.</span></span>
    * <span data-ttu-id="f4fc4-116">Sleppa önnur þrep í núverandi undirverki ef gagnasafn af gerð 'Rekstrartilföngum' er þegar til.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="f4fc4-117">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="f4fc4-118">Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".</span><span class="sxs-lookup"><span data-stu-id="f4fc4-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="f4fc4-119">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-119">Click Create repository.</span></span>
7. <span data-ttu-id="f4fc4-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="f4fc4-121">Sækja Intrastat-skilgreiningar sem Microsoft veitir</span><span class="sxs-lookup"><span data-stu-id="f4fc4-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f4fc4-122">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-122">Click Open.</span></span>
2. <span data-ttu-id="f4fc4-123">Í trénu skal velja 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="f4fc4-124">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-124">Click Import.</span></span>
    * <span data-ttu-id="f4fc4-125">Smelltu á innflutning fyrir útgáfu 1.1 fyrir valda skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="f4fc4-126">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-126">Click Yes.</span></span>
5. <span data-ttu-id="f4fc4-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-127">Close the page.</span></span>
6. <span data-ttu-id="f4fc4-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-128">Close the page.</span></span>
7. <span data-ttu-id="f4fc4-129">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="f4fc4-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="f4fc4-130">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="f4fc4-131">Í trénu skal velja 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

