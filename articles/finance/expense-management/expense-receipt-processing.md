---
title: Vinnsla á kostnaðarinnhreyfingum
description: Þetta efni veitir upplýsingar um vinnslu á ljósstafalínu (OCR) fyrir innhreyfingar. Þessi eiginleiki er hannaður til að bæta upplifun notenda þegar kostnaðarskýrslur eru búnar til í Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378232"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="a9277-104">Úrvinnsla kostnaðarkvittunar</span><span class="sxs-lookup"><span data-stu-id="a9277-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9277-105">Útgjaldafærsla hefur verið aukin með tilkomu vinnslu á ljósstafalínu (OCR) fyrir innhreyfingar.</span><span class="sxs-lookup"><span data-stu-id="a9277-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="a9277-106">Þessi eiginleiki er hannaður til að bæta upplifun notenda þegar kostnaðarskýrslur eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="a9277-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="a9277-107">Lykileiginleikar</span><span class="sxs-lookup"><span data-stu-id="a9277-107">Key features</span></span>

- <span data-ttu-id="a9277-108">Nafn söluaðila, dagsetning og heildarupphæð er dregin út úr innhreyfingum.</span><span class="sxs-lookup"><span data-stu-id="a9277-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="a9277-109">Aðgerðin reynir að samsvara óbundnum kvittunum við óbundin kostnaðarfærslna.</span><span class="sxs-lookup"><span data-stu-id="a9277-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="a9277-110">Notendur geta búið til handvirkt færð kostnaðarfærslur úr innhreyfingum.</span><span class="sxs-lookup"><span data-stu-id="a9277-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="a9277-111">Dæmi um notkun</span><span class="sxs-lookup"><span data-stu-id="a9277-111">Usage examples</span></span>

<span data-ttu-id="a9277-112">Til að tengja sjálfkrafa innhreyfingar sem innihalda kreditkortafærslur þegar kostnaðarskýrsla er stofnuð skal gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="a9277-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="a9277-113">Opnaðu vinnusvæðið **Kostnaðarstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="a9277-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="a9277-114">Á flipanum **Innhreyfingar** staðfestirðu að óviðhengdar innhreyfingar séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="a9277-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="a9277-115">Þú getur líka hlaðið inn innhreyfingum á flipann **Innhreyfingar**.</span><span class="sxs-lookup"><span data-stu-id="a9277-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="a9277-116">Á flipanum **Kostnaður** staðfestirðu að óviðhengdur kostnaður sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="a9277-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="a9277-117">Venjulega flytur kostnaðarstjórinn inn þennan kostnað frá kreditkortafyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="a9277-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="a9277-118">Veldu **Nýja kostnaðarskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="a9277-118">Select **New expense report**.</span></span> <span data-ttu-id="a9277-119">Taktu eftir að þú getur líka haft kostnað og innhreyfingar þegar þú býrð til kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="a9277-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="a9277-120">Ef þú bætir bæði við kostnaði og innhreyfingum er sjálfvirk samsvörun innhreyfinga gagnvart kostnaðinum sett af stað.</span><span class="sxs-lookup"><span data-stu-id="a9277-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="a9277-121">Til að stofna kostnað, eða jafna kostnað úr kvittun, skal gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="a9277-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="a9277-122">Í kostnaðarskýrslu, á flipanum **Innhreyfingar**, festirðu innhreyfingu við með því að velja **Bæta við innhreyfingum**.</span><span class="sxs-lookup"><span data-stu-id="a9277-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="a9277-123">Undir upphlaðinni mynd af innhreyfingunni skaltu taka eftir valkostunum **Stofna** og **Jafna**.</span><span class="sxs-lookup"><span data-stu-id="a9277-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="a9277-124">Veldu **Stofna** til að búa til handvirkt færðar kostnaðarfærslur og fylla út gildin sem eru dregin út úr innhreyfingunni.</span><span class="sxs-lookup"><span data-stu-id="a9277-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="a9277-125">Ef þú velur **Jafna** reynir kerfið að passa núverandi kostnað við innhreyfinguna.</span><span class="sxs-lookup"><span data-stu-id="a9277-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="a9277-126">Uppsetning</span><span class="sxs-lookup"><span data-stu-id="a9277-126">Installation</span></span>

<span data-ttu-id="a9277-127">Þessi aðgerð virkar ásamt eiginleikanum **Kostnaðarskýrslur endurhugsaðar** til að auðvelda kostnaðarupplifunina.</span><span class="sxs-lookup"><span data-stu-id="a9277-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="a9277-128">Þessi eiginleiki er aðeins í boði fyrir lagið Tier 2+ umhverfi sem er Sandkassi og Framleiðsla.</span><span class="sxs-lookup"><span data-stu-id="a9277-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="a9277-129">Til að nota þessa ítarlegu kostnaðarmöguleika skaltu setja upp innbótina Þjónusta kostnaðarstýringar fyrir Microsoft Dynamics 365 Finance og kveikja á aðgerðum í þínu tilviki.</span><span class="sxs-lookup"><span data-stu-id="a9277-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="a9277-130">Þú getur fengið aðgang að viðbótinni frá verkefninu í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a9277-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="a9277-131">Skráðu þig inn á LCS og opnaðu viðkomandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="a9277-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="a9277-132">Farðu í **Fullar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="a9277-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="a9277-133">Veldu **Viðhalda** eða skrunaðu niður að flýtiflipanum **Umhverfisinnbætur**.</span><span class="sxs-lookup"><span data-stu-id="a9277-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="a9277-134">Veldu **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="a9277-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="a9277-135">Veldu **Kostnaðarstjórnunarþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="a9277-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="a9277-136">Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="a9277-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="a9277-137">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="a9277-137">Select **Install**.</span></span>

<span data-ttu-id="a9277-138">Í vinnusvæðinu **Stjórnun eiginleika** kveikirðu á eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="a9277-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="a9277-139">Kostnaðarskýrslur endurhugsaðar</span><span class="sxs-lookup"><span data-stu-id="a9277-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="a9277-140">Sjálfvirk samsvörun og kostnaður vegna kvittunar búinn til</span><span class="sxs-lookup"><span data-stu-id="a9277-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="a9277-141">Þegar kveikt er á þessum eiginleikum gerast eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="a9277-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="a9277-142">Núverandi vinnusvæði **Kostnaðarstjórnunar** er skipt út fyrir nýja vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="a9277-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="a9277-143">Nýtt valmyndaratriði fyrir sýnileika kostnaðarreits er bætt við.</span><span class="sxs-lookup"><span data-stu-id="a9277-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="a9277-144">Þú getur samt opnað fyrri síðuna **Kostnaðarskýrslur** með því að fara í **Kostnaðarstjórnun > Minn kostnaður > Kostnaðarskýrslur**.</span><span class="sxs-lookup"><span data-stu-id="a9277-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="a9277-145">Verkflæði og allar samþykktir leiða þig ennþá að núverandi síðu fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="a9277-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="a9277-146">Innhreyfingar verða unnar í gegnum Microsoft Azure Cognitive Services og lýsigögn verða dregin út og bætt við.</span><span class="sxs-lookup"><span data-stu-id="a9277-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="a9277-147">Bætt er við valkosti sem gerir þér kleift að búa til kostnaðarskýrslu sem inniheldur samsvarandi ótengdar innhreyfingar.</span><span class="sxs-lookup"><span data-stu-id="a9277-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="a9277-148">Valkostur sem er bætt við kostnaðarskýrslur gerir þér kleift að búa til kostnaðarlínu úr innhreyfingu eða reyna að jafna núverandi innhreyfingu við núverandi kostnaðarlínu.</span><span class="sxs-lookup"><span data-stu-id="a9277-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="a9277-149">Fyrir frekari upplýsingar um eiginleikan Kostnaðarskýrslur endurhugsaðar er að finna í [Kostnaðarskýrslur endurskoðaðar](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="a9277-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a9277-150">Algengar spurningar</span><span class="sxs-lookup"><span data-stu-id="a9277-150">Frequently asked questions</span></span>

<span data-ttu-id="a9277-151">**Notar Microsoft gögnin mín fyrir gerðir sínar?**</span><span class="sxs-lookup"><span data-stu-id="a9277-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="a9277-152">Nei, Microsoft hefur smíðað almennt vélanámslíkan fyrir innhreyfingavinnsluþjónustu sína.</span><span class="sxs-lookup"><span data-stu-id="a9277-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="a9277-153">Þetta líkan er ekki byggð á innhreyfingum sem þú hleður upp.</span><span class="sxs-lookup"><span data-stu-id="a9277-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="a9277-154">**Hvar er þessi eiginleiki tiltækur og afgreiddur?**</span><span class="sxs-lookup"><span data-stu-id="a9277-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="a9277-155">Sem stendur eru Bandaríkin studd.</span><span class="sxs-lookup"><span data-stu-id="a9277-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="a9277-156">**Hvert fara innhreyfingarnar mínar?**</span><span class="sxs-lookup"><span data-stu-id="a9277-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="a9277-157">Finance mun hafa samband við Cognitive Services til að vinna úr gögnum svæðisins.</span><span class="sxs-lookup"><span data-stu-id="a9277-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="a9277-158">Cognitive Services mun geyma afrit af innhreyfingunni í allt að sólarhring meðan vinnsla á sér stað.</span><span class="sxs-lookup"><span data-stu-id="a9277-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="a9277-159">Eftir að vinnslu er lokið mun Cognitive Services fjarlægja innhreyfinguna.</span><span class="sxs-lookup"><span data-stu-id="a9277-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="a9277-160">Innhreyfingar eru enn geymdar í Finance.</span><span class="sxs-lookup"><span data-stu-id="a9277-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="a9277-161">Fyrir frekari upplýsingar, sjá [Virkja skilning á kvittun með nýrri getu Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="a9277-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
