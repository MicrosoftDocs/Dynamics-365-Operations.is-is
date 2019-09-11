---
title: Stofna fjárhagsáætlanir viðhalds
description: Þetta efni útskýrir hvernig á að stofna fjárhagsáætlun viðhalds í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d2c748fd230796643f1ed6279743da532e7cb320
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874809"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="1b37a-103">Stofna fjárhagsáætlanir viðhalds</span><span class="sxs-lookup"><span data-stu-id="1b37a-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]



<span data-ttu-id="1b37a-104">Fjárhagsáætlanir viðhalds eru notaðar til að veita yfirsýn yfir væntanlegan kostnað vegna fyrirbyggjandi viðhalds.</span><span class="sxs-lookup"><span data-stu-id="1b37a-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="1b37a-105">Fjárhagsáætlunarlínur eru reiknaðar út frá viðhaldsáætlunarlínum sem hafa áætlaðan upphafsdag á fjárhagsáætlunartímabilinu.</span><span class="sxs-lookup"><span data-stu-id="1b37a-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="1b37a-106">Fjárhagsáætlanir viðhalds eru byggðar á kostnaðargerðum sem notaðar eru í eignastýringu: **Fyrirbyggjandi**, **Leiðréttandi** og **Fjárfesting**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="1b37a-107">Fjárhagsáætlunarkostnaður vegna viðhalds fjárfestinga er innifalinn fyrir virkar eignir sem eiga sér endurnýjunardagsetningu á fjárhagsáætlunartímabilinu og tilheyrandi endurnýjunargildi.</span><span class="sxs-lookup"><span data-stu-id="1b37a-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="1b37a-108">Kostnaður áætlunar vegna viðgerða er innifalinn ef fyrri leiðréttingardagur er innifalinn í útreikningi fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="1b37a-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="1b37a-109">Í því tilfelli er leiðréttingarkostnaður frá fyrra tímabili reiknaður fyrir sama framtíðartímabil og þú reiknar út viðhaldsáætlun fyrir.</span><span class="sxs-lookup"><span data-stu-id="1b37a-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="1b37a-110">Stofna fjárhagsáætlun viðhalds</span><span class="sxs-lookup"><span data-stu-id="1b37a-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="1b37a-111">Veldu **Eignastýring** \> **Fyrirspurnir** \> **Viðhaldsáætlun** \> **Fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="1b37a-112">Veldu **Stofna fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="1b37a-113">Í reitinn **Viðhaldsáætlun** skal slá inn kenni fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="1b37a-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="1b37a-114">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="1b37a-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1b37a-115">Á flýtiflipanum **Tímabil**, í reitunum **Frá dagsetningu** og **Til dagsetningar**, skal slá inn upphafs- og lokadagsetningar fjárhagsáætlunartímabilsins.</span><span class="sxs-lookup"><span data-stu-id="1b37a-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="1b37a-116">Til að fela í sér leiðréttandi kostnað við fjárhagsáætlun sem er reiknaður út á grundvelli raunkostnaðar frá fyrra tímabili skal slá inn upphafsdagsetningu tímabilsins sem þessi kostnaður ætti að vera með frá í reitinn **Leiðrétting frá dagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="1b37a-117">Eftir því hvaða upplýsingastigs er krafist í fjárhagsáætluninni skal stilla viðeigandi valkosti á hinum fimm flýtiflipum **Flokka eftir**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="1b37a-118">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-118">Select **OK**.</span></span>
8. <span data-ttu-id="1b37a-119">Veldu **Fjárhagsáætlunarlínur** til að opna síðuna **Fjárhagsáætlunarlínur viðhalds** þar sem þú getur skoðað allar fjárhagsáætlunarlínur sem hafa verið búnar til á tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="1b37a-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="1b37a-120">Til að samþykkja fjárhagsáætlunina skaltu velja hana á síðunni **Fjárhagsáætlanir viðhalds** og velja síðan **Samþykkja**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="1b37a-121">Síðan, í valmyndinni **Samþykkja fjárhagsáætlun** skaltu velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="1b37a-122">Nafn þitt er slegið inn í reitinn **Samþykkt af** á síðunni **Fjárhagsáætlanir viðhalds**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b37a-123">Þegar þú hefur samþykkt fjárhagsáætlun viðhalds geturðu ekki endurútreiknað eða aðlagað tengdar línur á síðunni **Fjárhagsáætlunarlínur viðhalds** nema að þú fjarlægir samþykkið fyrst.</span><span class="sxs-lookup"><span data-stu-id="1b37a-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="1b37a-124">Til að fjarlægja samþykki á fjárhagsáætlun viðhalds skaltu velja hana á síðunni **Fjárhagsáætlanir viðhalds** og velja síðan **Samþykkja**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="1b37a-125">Síðan, í valmyndinni **Samþykkja fjárhagsáætlun** skaltu velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Mynd 1](media/01-maintenance-budgets.png)

<span data-ttu-id="1b37a-127">Einnig er hægt að stofna nýja fjárhagsáætlun viðhalds með því að afrita fyrirliggjandi fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="1b37a-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="1b37a-128">Á síðunni **Fjárhagsáætlanir viðhalds** velurðu fjárhagsáætlun til að afrita og síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="1b37a-129">Þessi aðferð er gagnleg ef þú hefur til dæmis búið til fjárhagsáætlun í einn mánuð og vilt afrita hana á aðra mánuði.</span><span class="sxs-lookup"><span data-stu-id="1b37a-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="1b37a-130">Viðhaldsfjárhagsáætlunin reiknar aðeins kostnaðaráætlun fjárhagsáætlunar út frá fjárhagsáætlunarlínum viðhalds.</span><span class="sxs-lookup"><span data-stu-id="1b37a-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="1b37a-131">Til að reikna út raunkostnað fyrir sama tímabil er hægt að gera þann útreikning á síðunni **Stýring eignakostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="1b37a-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
