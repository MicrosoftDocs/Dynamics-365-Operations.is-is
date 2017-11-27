---
title: "Vinnsla almennrar færslubókar"
description: "Þessi grein lýsir eiginleikum í Microsoft Dynamics 365 Finance and Operations, Enterprise edition sem geta hjálpað við að gera vinnslu almennrar færslubókar auðveldari, sem og að tryggja að rétt gögn séu tekin og að innri stýring sé ekki í hættu."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 76386f7ab8033075f9db4cadc697f3a2a997163e
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="general-journal-processing"></a><span data-ttu-id="1191f-103">Vinnsla almennrar færslubókar</span><span class="sxs-lookup"><span data-stu-id="1191f-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1191f-104">Þessi grein lýsir eiginleikum í Microsoft Dynamics 365 Finance and Operations, Enterprise edition sem geta hjálpað við að gera vinnslu almennrar færslubókar auðveldari, sem og að tryggja að rétt gögn séu tekin og að innri stýring sé ekki í hættu.</span><span class="sxs-lookup"><span data-stu-id="1191f-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="1191f-105">Færslubókanöfn</span><span class="sxs-lookup"><span data-stu-id="1191f-105">Journal names</span></span>

<span data-ttu-id="1191f-106">Eitt af mikilvægustu sviðum til að setja upp eru heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="1191f-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="1191f-107">Góð hugmynd er að skilgreina ákveðin heiti færslubókar fyrir hvert málefni, eins og innan samstæðu, leiðrétting á uppsöfnun og villuleiðrétting.</span><span class="sxs-lookup"><span data-stu-id="1191f-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="1191f-108">Hægt er að sníða hvert heiti færslubókar til að hjálpa við að gera gagnainnfærslu fyrir hvert málefni auðvelda og örugga.</span><span class="sxs-lookup"><span data-stu-id="1191f-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="1191f-109">Á **færslubókarheiti** síðu er hægt að setja upp eftirfarandi einingar:</span><span class="sxs-lookup"><span data-stu-id="1191f-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="1191f-110">**Verkflæðissamþykkt** – til Að auka innri stýringu skal skilgreina færslubókarverkflæði sem koma á umfangsmiklum mörkum fyrir yfirferð og samþykktarskref, byggt á skilyrðum eins og heildar debetupphæð.</span><span class="sxs-lookup"><span data-stu-id="1191f-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="1191f-111">Verkflæði fyrir almennar færslubækur eru sett upp á síunni **Verkflæði fyrir fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="1191f-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="1191f-112">**Sjálfgildi** – Velja sjálfgildi fyrir mótlykill, gjaldmiðill, og fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="1191f-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="1191f-113">**Færslubókareftirlit** – hægt er að setja upp takmarkanir á fyrirtæki og gerð lykils og einnig í hlutagildi.</span><span class="sxs-lookup"><span data-stu-id="1191f-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="1191f-114">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="1191f-114">**Examples**</span></span>

<span data-ttu-id="1191f-115">færslubókarheiti er hægt að nota fyrir leiðréttingar eingöngu.</span><span class="sxs-lookup"><span data-stu-id="1191f-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="1191f-116">Í þessu tilfelli er hægt að tilgreina að aðeins **Fjárhags** lykilgerðin er gild fyrir öll fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="1191f-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="1191f-117">[![Gerðir lykla fyrir færslubókareftirlit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="1191f-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="1191f-118">Hægt er að nota heiti færslubókar eingöngu fyrir tiltekinn hluta eða fyrir svið aðallykla.</span><span class="sxs-lookup"><span data-stu-id="1191f-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="1191f-119">[![Hluti færslubókareftirlits](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="1191f-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="1191f-120">**Sjálfvirka bakfærslu** valkosturinn er tiltækur í almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="1191f-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="1191f-121">Til dæmis, er leiðrétting á uppsöfnun þar sem raunverulegur skjal hefur ekki enn verið unnin, eins og sýnt er í eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="1191f-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="1191f-122">[![Almenn færslubók sem er bakfærð](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="1191f-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="1191f-123">Microsoft Excel-innbót fyrir færslu í færslubók veitir meiri sjálfvirkni og auðveldar innfærslu gagna.</span><span class="sxs-lookup"><span data-stu-id="1191f-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="1191f-124">**Opnar línur í Excel** aðgerð er tiltæk á í **Almennrar færslubókar** og **fylgiskjal** síður.</span><span class="sxs-lookup"><span data-stu-id="1191f-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="1191f-125">Á **Tímabilsbækur** síða, geturðu sett upp endurteknar færslubækur í til að gera sjálfvirkt færslubókarferli.</span><span class="sxs-lookup"><span data-stu-id="1191f-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="1191f-126">Hægt er að nota sniðmát fyrir fylgiskjöl hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="1191f-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="1191f-127">Á síðunni **Almennar færslubækur** má finna aðgerðirnar **Vista** og **Velja sniðmát fylgiskjals** á síðunni **Færslubókarfylgiskjal** undir **Aðgerðir** fyrir línur fylgiskjals.</span><span class="sxs-lookup"><span data-stu-id="1191f-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="1191f-128">Tengd uppsetning</span><span class="sxs-lookup"><span data-stu-id="1191f-128">Related setup</span></span>
<span data-ttu-id="1191f-129">Eftirfarandi uppsetningar er ekki bundinn við almennar færslubækur en hjálpar að tryggja samræmda gagnainnslætti sem er rétt og auðveld.</span><span class="sxs-lookup"><span data-stu-id="1191f-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="1191f-130">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="1191f-130">Main account</span></span>

<span data-ttu-id="1191f-131">Uppsetning aðallykils býður upp á marga valkosti fyrir úrvinnslu almennrar færslubókar:</span><span class="sxs-lookup"><span data-stu-id="1191f-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="1191f-132">**DC/KR krafa** – Notið þennan valkost ef aðallykil er takmarkaður við debet-eða kreditfærslur.</span><span class="sxs-lookup"><span data-stu-id="1191f-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="1191f-133">Uppsetning er sannprófað þegar færslubók er villuleitað eða bókað.</span><span class="sxs-lookup"><span data-stu-id="1191f-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="1191f-134">**Sjálfgefinn mótlykill**</span><span class="sxs-lookup"><span data-stu-id="1191f-134">**Default offset account**</span></span>
-   <span data-ttu-id="1191f-135">**Frestað** – Fresta aðallykil fyrir innslátt gagna í öllum fyrirtækjum eða fyrir tiltekin fyrirtæki/lögaðilaa.</span><span class="sxs-lookup"><span data-stu-id="1191f-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="1191f-136">**Ekki leyfa handvirkan innslátt** – koma í veg Fyrir að notendur fært inn gildi handvirkt fyrir lykilinn í færslubók.</span><span class="sxs-lookup"><span data-stu-id="1191f-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="1191f-137">**Sjálfgildur/villuleita gjaldmiðil**</span><span class="sxs-lookup"><span data-stu-id="1191f-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="1191f-138">**Hnekkja lögaðila** – Þessi uppsetning á sérstaklega við fyrirtæki/lögaðila:</span><span class="sxs-lookup"><span data-stu-id="1191f-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="1191f-139">**sjálfgefnir/sannprófa VSK-flokka**</span><span class="sxs-lookup"><span data-stu-id="1191f-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="1191f-140">**Sjálfgefin vídd** – **Ekki föst** eða **Föst gildi**.</span><span class="sxs-lookup"><span data-stu-id="1191f-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="1191f-141">**Föst gildi** hjálpar að tryggja allar bókanir fyrir þennan aðallykil séu ávallt að nota víddargildið sem er sett upp sem **Fast**.</span><span class="sxs-lookup"><span data-stu-id="1191f-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="1191f-142">**Bókunarvilluleit**</span><span class="sxs-lookup"><span data-stu-id="1191f-142">**Posting validation**</span></span>
    -   <span data-ttu-id="1191f-143">**Villuleit notanda** – valkosturinn stýrir því hvaða notendur hafa heimild til að bóka aðallykil.</span><span class="sxs-lookup"><span data-stu-id="1191f-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="1191f-144">**Villuleit bókunargerðar** – valkosturinn stýrir því hvaða bókunargerð eru leyfðar fyrir aðallykil.</span><span class="sxs-lookup"><span data-stu-id="1191f-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="1191f-145">Bókhaldslykilskipulag og skipulag ítarlegra reglna</span><span class="sxs-lookup"><span data-stu-id="1191f-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="1191f-146">Bókhaldsskipulag og skipulag ítarlegra reglna er mjög mikilvægt fyrir að tryggja gögn sem þarf fyrir fjárhagslega skýrslugerð og afkastarakningu er sótt við úrvinnslu almennrar færslubókar og allra fylgiskjala.</span><span class="sxs-lookup"><span data-stu-id="1191f-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="1191f-147">Bókhaldslykilskipulag og skipulag ítarlegra reglna leyfa þér að klæðskerasníða upplifun af gagnainnslætti.</span><span class="sxs-lookup"><span data-stu-id="1191f-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="1191f-148">Hægt er að leyfa innslátt gagna aðeins fyrir fjárhagsvíddir sem eiga við hverja aðstæðu, og getur framfylgt þeirri kröfu að áskilin og rétt gögn séu ávallt sótt.</span><span class="sxs-lookup"><span data-stu-id="1191f-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="1191f-149">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="1191f-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="1191f-150">[Áætlanagerð: bókhaldslykilsins](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="1191f-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="1191f-151">Stofna ítarlegar reglur fyrir færslubækur</span><span class="sxs-lookup"><span data-stu-id="1191f-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="1191f-152">Stofna færslu í færslubók með því að nota sniðmát</span><span class="sxs-lookup"><span data-stu-id="1191f-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="1191f-153">Stofna og sannprófa færslubækur</span><span class="sxs-lookup"><span data-stu-id="1191f-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="1191f-154">Bóka tímabilsbækur</span><span class="sxs-lookup"><span data-stu-id="1191f-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="1191f-155">Vinna úr færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="1191f-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



