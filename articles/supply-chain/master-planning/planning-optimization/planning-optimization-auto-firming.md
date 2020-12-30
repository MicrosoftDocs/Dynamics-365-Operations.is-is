---
title: Sjálfvirk staðfesting með fínstillingu skipulagningar
description: Þetta efni útskýrir hvernig á að nota sjálfvirka styrkingu með fínstillingu skipulagsins.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 61e9e6aa660bc0828645c6bf1f2655539804831a
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594527"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="00d70-103">Sjálfvirk staðfesting með fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="00d70-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00d70-104">Sjálfvirk styrking gerir þér kleift að festa (það er að losa) fyrirhugaðar pantanir sem hluta af ferli aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="00d70-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="00d70-105">Þegar fyrirhugaðar pantanir eru styrktar er þeim breytt í raunverulegar innkaupapantanir, millifærslupantanir eða framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="00d70-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="00d70-106">Þegar fínstilling skipulags er notuð eru skipulagðar pantanir styrktar meðan á aðaláætlunargerð stendur þegar pöntunardagsetningin (það er upphafsdagsetningin) er innan tímamarka.</span><span class="sxs-lookup"><span data-stu-id="00d70-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="00d70-107">Sjálfvirk staðfesting áætlaðrar innkaupapöntunar getur aðeins farið fram ef varan er tengd lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="00d70-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="00d70-108">Kveikja á sjálfvirkri staðfestingu</span><span class="sxs-lookup"><span data-stu-id="00d70-108">Turn on autofirming</span></span>

<span data-ttu-id="00d70-109">Til að kveikja á sjálfvirkri staðsetningu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="00d70-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="00d70-110">Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Nýtt**, velurðu **Sjálfvirk styrking með fínstillingu skipulags** á listanum.</span><span class="sxs-lookup"><span data-stu-id="00d70-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="00d70-111">Ef eiginleikinn birtist ekki á flipanum **Nýtt** skaltu líta á flipana **Ekki gert virkt** og **Allt**.</span><span class="sxs-lookup"><span data-stu-id="00d70-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="00d70-112">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="00d70-112">Select **Enable now**.</span></span> <span data-ttu-id="00d70-113">Að öðrum kosti velurðu **Áætlun** og velur síðan tímann þegar kveikt skal á aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="00d70-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="00d70-114">Setja upp tímamörk staðfestingar</span><span class="sxs-lookup"><span data-stu-id="00d70-114">Set up the firming time fence</span></span>

<span data-ttu-id="00d70-115">Staðfestingartímamörkin eru framreiknuð frá keyrsludagsetningu aðaláætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="00d70-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="00d70-116">Þau eru skilgreind af fjölda daga sem eru færð inn.</span><span class="sxs-lookup"><span data-stu-id="00d70-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="00d70-117">Þú getur stjórnað tímamörkum staðfestingar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="00d70-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="00d70-118">Til að skilgreina sjálfgefinn girðingartíma girðingar fyrir umfjöllunarhóp ferðu í **Aðaláætlunargerð** \> **Uppsetning** \> **Þekja** \> **Þekjuhópar** og veldu þekjuhóp.</span><span class="sxs-lookup"><span data-stu-id="00d70-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="00d70-119">Síðan, á flýtiflipanum **Annað**, í reitinn **Sjálfvirk tímamörk staðfestinga (dagar)**, sláðu inn fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="00d70-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="00d70-120">Til að skrifa yfir tímamörk staðfestingar sem eru skilgreind fyrir þekjuflokkinn fyrir tiltekna vöru er farið í **Afurðarupplýsingastjórnun** \> **Útgefnar afurðir**, síðan á aðgerðasvæðinu er valið **Áætlun** og síðan valið **Vöruþekja**.</span><span class="sxs-lookup"><span data-stu-id="00d70-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="00d70-121">Síðan, á flipanum **Almennt** velurðu **Hnekkja tímamörkum** og í reitinn **Sjálfvirk tímamörk staðfestinga (dagar)** slærðu inn fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="00d70-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="00d70-122">Til að skrifa yfir þau tímamörk staðfestingar sem eru skilgreind fyrir þekjuhópinn og vöruþekju fyrir tiltekið aðalskipulag **Aðaláætlunargerð** \> **Uppsetning** \> **Aðaláætlanir** og velur aðalskipulag.</span><span class="sxs-lookup"><span data-stu-id="00d70-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="00d70-123">Síðan, á **Tímamörk í dögum** flipanum, skal stilla **Staðfesting** á **Já** og slá inn dagafjöldann.</span><span class="sxs-lookup"><span data-stu-id="00d70-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="00d70-124">Ef kveikt er á sjálfvirkri staðfestingu fyrir keyrslu aðaláætlanagerðar sem notar fínstillingu skipulagningar er ferli sjálfvirkrar staðfestingar lokið samkvæmt uppsetningu sjálfsvirkrar staðfestingar.</span><span class="sxs-lookup"><span data-stu-id="00d70-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="00d70-125">Ef ekki er kveikt á sjálfvirkri staðfestingu eða ef áætlun er ræst af síðunni **Nettóþarfir** er samþykki sjálfvirkrar staðfestingar sleppt.</span><span class="sxs-lookup"><span data-stu-id="00d70-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="00d70-126">Fínstilling skipulags vs. innbyggða áætlunarvélin Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="00d70-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="00d70-127">Hægt er að nota bæði fínstillingu skipulagningar og áætlunarvélina sem er byggð inn í Microsoft Dynamics 365 Supply Chain Management til að staðfesta áætlaðar pantanir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="00d70-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="00d70-128">Þó er til staðar mikilvægur munur.</span><span class="sxs-lookup"><span data-stu-id="00d70-128">However, there are some important differences.</span></span> <span data-ttu-id="00d70-129">Til dæmis, meðan fínstilling skipulagsins notar pöntunardaginn (þ.e.a.s. upphafsdaginn) til að ákvarða hvaða fyrirhugaðar pantanir verða festar, þá notar innbyggða skipulagsvélin fyrir Supply Chain Management dagsetninguna (þ.e.a.s. lokadagsetningin).</span><span class="sxs-lookup"><span data-stu-id="00d70-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="00d70-130">Hér er yfirlit yfir mismuninn.</span><span class="sxs-lookup"><span data-stu-id="00d70-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="00d70-131">**Fínstilling áætlanagerðar**</span><span class="sxs-lookup"><span data-stu-id="00d70-131">**Planning Optimization**</span></span>

- <span data-ttu-id="00d70-132">Sjálfvirk staðfesting er byggð á pöntunardagsetningu (upphafsdegi).</span><span class="sxs-lookup"><span data-stu-id="00d70-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="00d70-133">Vegna þess að pöntunardagsetningin (upphafsdagsetningin) kallar á staðfestingu þarftu ekki að líta á afhendingartímann sem hluta af tímamörkum staðfestingar.</span><span class="sxs-lookup"><span data-stu-id="00d70-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="00d70-134">Ef þú vilt staðfesta allar pantanir sem verða að byrja í þessari viku, verða tímamörk staðfestingar að vera ein vika.</span><span class="sxs-lookup"><span data-stu-id="00d70-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="00d70-135">**Innbyggð áætlunarvél í Supply Chain Management**</span><span class="sxs-lookup"><span data-stu-id="00d70-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="00d70-136">Sjálfvirk staðfesting er byggð á þarfadagsetningu (lokadegi).</span><span class="sxs-lookup"><span data-stu-id="00d70-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="00d70-137">Til að hjálpa til við að tryggja að pantanir séu staðfestar á réttum tíma verða tímamörk staðfestingar að vera lengri en afhendingartíminn.</span><span class="sxs-lookup"><span data-stu-id="00d70-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="00d70-138">Ef þú vilt staðfesta allar pantanir sem verða að byrja í þessari viku, verða tímamörk staðfestingar að vera afhendingartíminn plús ein vika.</span><span class="sxs-lookup"><span data-stu-id="00d70-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
