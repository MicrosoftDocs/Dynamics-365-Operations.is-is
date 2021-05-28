---
title: Hætta með skilgreiningar í altækri geymslu RCS
description: Þetta efnisatriði lýsir hvernig á að hætta að nota skilgreiningar í altækri geymslu RCS.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018734"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="54968-103">Hætta með skilgreiningar í altækri geymslu RCS</span><span class="sxs-lookup"><span data-stu-id="54968-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54968-104">Þetta efnisatriði lýsir hvernig á að hætta að nota skilgreiningu í altækri geymslu RCS.</span><span class="sxs-lookup"><span data-stu-id="54968-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="54968-105">Áður var aðeins hægt að eyða skilgreiningum sem ekki þurfti að nota lengur.</span><span class="sxs-lookup"><span data-stu-id="54968-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="54968-106">Nú er hins vegar hægt að merkja útgefna skilgreiningu sem **Hætt að nota** í altækri geymslu RCS.</span><span class="sxs-lookup"><span data-stu-id="54968-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="54968-107">Með þessari aðgerð er einnig hægt að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="54968-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="54968-108">Bjóða upp á tilkynningar fyrirfram þegar áformað er að hætta að nota skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="54968-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="54968-109">Hafa með viðeigandi upplýsingar um skilgreininguna sem kemur í staðinn.</span><span class="sxs-lookup"><span data-stu-id="54968-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="54968-110">Setja á dagsetningu fyrir **Stutt fram til** fyrir tiltekna skilgreiningu til að láta notandann vita hvenær hætt verður að nota hana.</span><span class="sxs-lookup"><span data-stu-id="54968-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="54968-111">Þegar hætt verður að nota útgáfu skilgreiningar er hægt að tilgreina eftirfarandi valfrjálsar upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="54968-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="54968-112">**Skilgreining sem kemur í staðinn**</span><span class="sxs-lookup"><span data-stu-id="54968-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="54968-113">**Útgáfa skilgreiningar sem kemur í staðinn**</span><span class="sxs-lookup"><span data-stu-id="54968-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="54968-114">**Athugasemd með frjálsum texta**: Notið þennan reiti til að gefa upp tengla eða tilvísanir í fylgigögn</span><span class="sxs-lookup"><span data-stu-id="54968-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="54968-115">**Stutt fram til**: Þessi reitur gefur upp framlagða dagsetningu sem núverandi skilgreining/útgáfa verður studd fram að.</span><span class="sxs-lookup"><span data-stu-id="54968-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="54968-116">Þessa dagsetningu þarf að uppfæra handvirkt.</span><span class="sxs-lookup"><span data-stu-id="54968-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="54968-117">Til að hætta að nota skilgreininguna skal ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="54968-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="54968-118">Veljið hvort eigi að hætta að nota eina útgáfu eða allar útgáfur með sömu stillingunum í einni aðgerð með því að stilla **Allar útgáfur** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="54968-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="54968-119">Stillið færibreytuna **Hætta að nota** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="54968-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="54968-120">Veljið **Í lagi** til að hætta að nota skilgreiningarnar.</span><span class="sxs-lookup"><span data-stu-id="54968-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="54968-121">Fyllt verður í reitinn **Dagsetning niðurfellingar** þegar breytingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="54968-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Upplýsingar um niðurfellingu skilgreiningar](media/Discontinue-details-2.png)
  
<span data-ttu-id="54968-123">Hægt er að snúa skilgreiningu aftur í **Samnýtt** eða breyta upplýsingum um niðurfellingu hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="54968-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="54968-124">Ef skilgreining er samnýtt skal tilgreina dagsetningu fyrir **Stutt fram til** og allar aðrar upplýsingar sem tengjast niðufrfellingunni til að gefa til kynna áform um niðurfellingar í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="54968-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="54968-125">Ef ætlunin er að deila upplýsingum um áætlaða niðurfellingu, áður en skilgreiningin verður felld niður, þá er hægt að fylla fyrirfram í alla reiti sem tengjast skiptingu en skilja eftir færibreytuna **Hætta að nota** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="54968-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="54968-126">Niðurfelling takmarkar ekki aðgerðir á skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="54968-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="54968-127">Áfram verður hægt að flytja inn, keyra eða hafa upp á skilgreiningum, þessir reitir eru til upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="54968-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="54968-128">Finance styður við upplýsingagjöfina frá og með útgáfu 10.0.14</span><span class="sxs-lookup"><span data-stu-id="54968-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="54968-129">Frá og með útgáfu 10.0.14 mun Dynamics 365 Finance styðja við upplýsingagjöf um niðurfellingu.</span><span class="sxs-lookup"><span data-stu-id="54968-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="54968-130">Á síðunni **Altæk geymsla** er hægt að skoða uppfærðar upplýsingar sem tengjast niðurfellingu.</span><span class="sxs-lookup"><span data-stu-id="54968-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="54968-131">Skilgreiningar sem hætt er að nota eru sjálfgefið síaðar frá.</span><span class="sxs-lookup"><span data-stu-id="54968-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="54968-132">Síðan **Innfluttar skilgreiningar** (ERSolutionTable) sýnir skilgreiningar sem var hætt að nota áður en þær voru fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="54968-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="54968-133">Fyrir þær skilgreiningar sem hætt var að nota eftir innflutning, er hægt að samstilla upplýsingar um niðurfellingu með því að keyra vinnsluna **Uppfærslur á innflutningi skilgreininga**.</span><span class="sxs-lookup"><span data-stu-id="54968-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


