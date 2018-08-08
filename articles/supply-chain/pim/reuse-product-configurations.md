---
title: "Endurnota afurðarafbrigði"
description: "Hægt er að tilgreina að sjálfkrafa eigi að nota aftur fyrirliggjandi afbrigði fyrir vöru. Síðan, þegar notandi hefur lokið skilgreinarlotu athugar kerfið hvort skilgreining sem samsvarar vali notanda er þegar til. Ef samsvarandi skilgreiningu finnst er auðkenni Skilgreiningar, samsvarandi uppskrift (BOM), og leið endurnotuð."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 18a3e5fb583ed620c825164f2628a26b6b0cb469
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="reuse-product-configurations"></a><span data-ttu-id="89856-105">Endurnota afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="89856-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89856-106">Hægt er að tilgreina að sjálfkrafa eigi að nota aftur fyrirliggjandi afbrigði fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="89856-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="89856-107">Síðan, þegar notandi hefur lokið skilgreinarlotu athugar kerfið hvort skilgreining sem samsvarar vali notanda er þegar til.</span><span class="sxs-lookup"><span data-stu-id="89856-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="89856-108">Ef samsvarandi skilgreiningu finnst er auðkenni Skilgreiningar, samsvarandi uppskrift (BOM), og leið endurnotuð.</span><span class="sxs-lookup"><span data-stu-id="89856-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="89856-109">Skilyrði til að geta endurnotað afbrigði</span><span class="sxs-lookup"><span data-stu-id="89856-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="89856-110">Til að geta látið endurnota afurður, verður að tilgreina eftirfarandi upplýsingar um íhluti og eigindir í síðunni **upplýsingar um afbrigðalíkan afurðar** :</span><span class="sxs-lookup"><span data-stu-id="89856-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="89856-111">**Íhlutir og undiríhlutir** - á flipanum **almennt** í reitnum **endurnota afbrigði**, veldu **já**.</span><span class="sxs-lookup"><span data-stu-id="89856-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="89856-112">**Eigind** – Á **Eigind** flýtiflipi, veldu **Hafa með í endurnotkun** valkost.</span><span class="sxs-lookup"><span data-stu-id="89856-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="89856-113">Þessi valkostur er aðeins tiltækur þegar tengdur íhlutur er virkjaður fyrir endurnotkun.</span><span class="sxs-lookup"><span data-stu-id="89856-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="89856-114">Ef þú velur engin eigindi til endurnotkunar, er afbrigðið alltaf endurnotað, óháð vali notandans á meðan verið var að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="89856-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="89856-115">Eigindagildi á fyrirliggjandi skilgreiningu verða passa við vali notanda.</span><span class="sxs-lookup"><span data-stu-id="89856-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="89856-116">Til dæmis, ef notandinn velur **blár** sem lit á meðan á skilgreiningu stendur, athugar kerfið hvort fyrirliggjandi afbrigði íhlutar hafi litinn bláan.</span><span class="sxs-lookup"><span data-stu-id="89856-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="89856-117">Endurstilling endurnotkun skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="89856-117">Resetting configuration reuse</span></span>
<span data-ttu-id="89856-118">Þegar þú endurstillir endurnotkun skilgreiningar, er ekki lengur tekið tillit til áður stofnaðra skilgreininga.</span><span class="sxs-lookup"><span data-stu-id="89856-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="89856-119">Þú gætir viðjal endurstilla endurnotkun skilgreiningar ef uppskriftin eða leiðin var breytt, en ekki var breytt tengdar eigindir.</span><span class="sxs-lookup"><span data-stu-id="89856-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="89856-120">Þú endurstillir endurnotkun skilgreiningar á flipanum **Almennt** fyrir íhlut.</span><span class="sxs-lookup"><span data-stu-id="89856-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>




