---
title: Vinnsla almennrar færslubókar
description: Þetta efnisatriði lýsir eiginleikum í Microsoft Dynamics 365 Finance sem geta hjálpað við að gera vinnslu almennrar færslubókar auðveldari, sem og að tryggja að rétt gögn séu tekin og að innri stýring sé ekki í hættu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2becf8213cfa46e2c0cf0c553f0b5e503dfc3704
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570241"
---
# <a name="general-journal-processing"></a><span data-ttu-id="964fc-103">Vinnsla almennrar færslubókar</span><span class="sxs-lookup"><span data-stu-id="964fc-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="964fc-104">Þetta efnisatriði lýsir eiginleikum sem geta hjálpað við að gera vinnslu almennrar færslubókar auðveldari, sem og að tryggja að rétt gögn séu tekin og að innri stýring sé ekki í hættu.</span><span class="sxs-lookup"><span data-stu-id="964fc-104">This topic describes capabilities that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="964fc-105">Færslubókanöfn</span><span class="sxs-lookup"><span data-stu-id="964fc-105">Journal names</span></span>

<span data-ttu-id="964fc-106">Eitt af mikilvægustu sviðum til að setja upp eru heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="964fc-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="964fc-107">Góð hugmynd er að skilgreina ákveðin heiti færslubókar fyrir hvert málefni, eins og innan samstæðu, leiðrétting á uppsöfnun og villuleiðrétting.</span><span class="sxs-lookup"><span data-stu-id="964fc-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="964fc-108">Hægt er að sníða hvert heiti færslubókar til að hjálpa við að gera gagnainnfærslu fyrir hvert málefni auðvelda og örugga.</span><span class="sxs-lookup"><span data-stu-id="964fc-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="964fc-109">Á **færslubókarheiti** síðu er hægt að setja upp eftirfarandi einingar:</span><span class="sxs-lookup"><span data-stu-id="964fc-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="964fc-110">**Verkflæðissamþykkt** – til Að auka innri stýringu skal skilgreina færslubókarverkflæði sem koma á umfangsmiklum mörkum fyrir yfirferð og samþykktarskref, byggt á skilyrðum eins og heildar debetupphæð.</span><span class="sxs-lookup"><span data-stu-id="964fc-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="964fc-111">Setja upp verkflæði fyrir almennar færslubækur á í **verkflæði fyrir fjárhag** síðu.</span><span class="sxs-lookup"><span data-stu-id="964fc-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="964fc-112">**Sjálfgildi** – Velja sjálfgildi fyrir mótlykill, gjaldmiðill, og fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="964fc-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="964fc-113">**Færslubókareftirlit** – hægt er að setja upp takmarkanir á fyrirtæki og gerð lykils og einnig í hlutagildi.</span><span class="sxs-lookup"><span data-stu-id="964fc-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="964fc-114">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="964fc-114">**Examples**</span></span>

<span data-ttu-id="964fc-115">færslubókarheiti er hægt að nota fyrir leiðréttingar eingöngu.</span><span class="sxs-lookup"><span data-stu-id="964fc-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="964fc-116">Í þessu tilfelli er hægt að tilgreina að aðeins **Fjárhags** lykilgerðin er gild fyrir öll fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="964fc-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="964fc-117">[![Gerðir lykla fyrir færslubókareftirlit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="964fc-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="964fc-118">Hægt er að nota heiti færslubókar eingöngu fyrir tiltekinn hluta eða fyrir svið aðallykla.</span><span class="sxs-lookup"><span data-stu-id="964fc-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="964fc-119">[![Hluti færslubókareftirlits](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="964fc-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="964fc-120">**Sjálfvirka bakfærslu** valkosturinn er tiltækur í almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="964fc-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="964fc-121">Til dæmis, er leiðrétting á uppsöfnun þar sem raunverulegur skjal hefur ekki enn verið unnin, eins og sýnt er í eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="964fc-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="964fc-122">[![Almenn færslubók sem er bakfærð](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="964fc-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="964fc-123">Microsoft Excel innbót fyrir færslu í færslubók veitir meiri sjálfvirkni og auðveldar innfærslu gagna.</span><span class="sxs-lookup"><span data-stu-id="964fc-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="964fc-124">**Opnar línur í Excel** aðgerð er tiltæk á í **Almennrar færslubókar** og **fylgiskjal** síður.</span><span class="sxs-lookup"><span data-stu-id="964fc-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="964fc-125">Á **Tímabilsbækur** síða, geturðu sett upp endurteknar færslubækur í til að gera sjálfvirkt færslubókarferli.</span><span class="sxs-lookup"><span data-stu-id="964fc-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="964fc-126">Hægt er að nota sniðmát fyrir fylgiskjöl hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="964fc-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="964fc-127">Á síðunni **Almennar færslubækur** má finna aðgerðirnar **Vista** og **Velja sniðmát fylgiskjals** á síðunni **Færslubókarfylgiskjal** undir **Aðgerðir** fyrir línur fylgiskjals.</span><span class="sxs-lookup"><span data-stu-id="964fc-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="964fc-128">Tengd uppsetning</span><span class="sxs-lookup"><span data-stu-id="964fc-128">Related setup</span></span>
<span data-ttu-id="964fc-129">Eftirfarandi uppsetning er ekki bundinn við almennar færslubækur en hjálpar að tryggja gagnainnslætti sem eru réttir og auðveldir.</span><span class="sxs-lookup"><span data-stu-id="964fc-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="964fc-130">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="964fc-130">Main account</span></span>

<span data-ttu-id="964fc-131">Uppsetning aðallykils býður upp á marga valkosti fyrir úrvinnslu almennrar færslubókar:</span><span class="sxs-lookup"><span data-stu-id="964fc-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="964fc-132">**DC/KR krafa** – Notið þennan valkost ef aðallykil er takmarkaður við debet-eða kreditfærslur.</span><span class="sxs-lookup"><span data-stu-id="964fc-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="964fc-133">Uppsetning er sannprófað þegar færslubók er villuleitað eða bókað.</span><span class="sxs-lookup"><span data-stu-id="964fc-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="964fc-134">**Sjálfgefinn mótlykill**</span><span class="sxs-lookup"><span data-stu-id="964fc-134">**Default offset account**</span></span>
-   <span data-ttu-id="964fc-135">**Frestað** – Fresta aðallykil fyrir innslátt gagna í öllum fyrirtækjum eða fyrir tiltekin fyrirtæki/lögaðila.</span><span class="sxs-lookup"><span data-stu-id="964fc-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="964fc-136">**Ekki leyfa handvirkan innslátt** – koma í veg Fyrir að notendur fært inn gildi handvirkt fyrir lykilinn í færslubók.</span><span class="sxs-lookup"><span data-stu-id="964fc-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="964fc-137">**Sjálfgildur/villuleita gjaldmiðil**</span><span class="sxs-lookup"><span data-stu-id="964fc-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="964fc-138">**Hnekkja lögaðila** – Þessi uppsetning á sérstaklega við fyrirtæki/lögaðila:</span><span class="sxs-lookup"><span data-stu-id="964fc-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="964fc-139">**sjálfgefnir/sannprófa VSK-flokka**</span><span class="sxs-lookup"><span data-stu-id="964fc-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="964fc-140">**Sjálfgefin vídd** – **Ekki föst** eða **Föst gildi**.</span><span class="sxs-lookup"><span data-stu-id="964fc-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="964fc-141">**Föst gildi** hjálpar að tryggja allar bókanir fyrir þennan aðallykil séu ávallt að nota víddargildið sem er sett upp sem **Fast**.</span><span class="sxs-lookup"><span data-stu-id="964fc-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="964fc-142">**Bókunarvilluleit**</span><span class="sxs-lookup"><span data-stu-id="964fc-142">**Posting validation**</span></span>
    -   <span data-ttu-id="964fc-143">**Villuleit notanda** – valkosturinn stýrir því hvaða notendur hafa heimild til að bóka aðallykil.</span><span class="sxs-lookup"><span data-stu-id="964fc-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="964fc-144">**Villuleit bókunargerðar** – valkosturinn stýrir því hvaða bókunargerð eru leyfðar fyrir aðallykil.</span><span class="sxs-lookup"><span data-stu-id="964fc-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="964fc-145">Bókhaldslykilskipulag og skipulag ítarlegra reglna</span><span class="sxs-lookup"><span data-stu-id="964fc-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="964fc-146">Bókhaldsskipulag og skipulag ítarlegra reglna er mjög mikilvægt til að tryggja gögn sem þarf fyrir fjárhagslega skýrslugerð og afkastarakningu er sótt við úrvinnslu almennrar færslubókar og allra fylgiskjala.</span><span class="sxs-lookup"><span data-stu-id="964fc-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="964fc-147">Bókhaldslykilskipulag og skipulag ítarlegra reglna leyfa þér að klæðskerasníða upplifun af gagnainnslætti.</span><span class="sxs-lookup"><span data-stu-id="964fc-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="964fc-148">Hægt er að leyfa gagnaskráningu aðeins fyrir fjárhagsvíddir sem eiga við í hverjum aðstæðum fyrir sig, og sem getur framfylgt þeirri kröfu að áskilin og rétt gögn séu ávallt sótt.</span><span class="sxs-lookup"><span data-stu-id="964fc-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="964fc-149">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="964fc-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="964fc-150">[Áætlanagerð: bókhaldslykilsins](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="964fc-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="964fc-151">Stofna ítarlegar reglur fyrir færslubækur</span><span class="sxs-lookup"><span data-stu-id="964fc-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="964fc-152">Stofna færslu í færslubók með því að nota sniðmát</span><span class="sxs-lookup"><span data-stu-id="964fc-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="964fc-153">Stofna og sannprófa færslubækur</span><span class="sxs-lookup"><span data-stu-id="964fc-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="964fc-154">Bóka tímabilsbækur</span><span class="sxs-lookup"><span data-stu-id="964fc-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="964fc-155">Vinna úr færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="964fc-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="964fc-156">Herma eftir bókun</span><span class="sxs-lookup"><span data-stu-id="964fc-156">Simulate posting</span></span>
<span data-ttu-id="964fc-157">Þú getur fundið **Herma eftir bókun** í valmyndinni **Sannprófa** fyrir flestar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="964fc-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="964fc-158">Þegar þú sannprófar færslubók með aðgerðinni **Sannprófa** prófar kerfið færslubókina í ákveðnum villuskilyrðum.</span><span class="sxs-lookup"><span data-stu-id="964fc-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="964fc-159">Ef þú notar aðgerðina **Herma eftir bókun** keyrir kerfið öll sömu ferlin sem eru keyrð við bókun án þess að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="964fc-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="964fc-160">Þú getur síðan farið yfir skilaboðin sem birtast, lagað allar villur sem þú finnur og opnað síðan á valmyndina **Bóka** til að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="964fc-160">You can then review the posting messages that are displayed, fix any errors that you find, and then open the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="964fc-161">**Herma eftir bókun** er ekki í boði fyrir runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="964fc-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="964fc-162">Hins vegar er kóði í boði til að herma eftir bókun í runu og þróunaraðilar geta aukið við kóðann til að bæta þessari virkni við.</span><span class="sxs-lookup"><span data-stu-id="964fc-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  

## <a name="journal-unlock"></a><span data-ttu-id="964fc-163">Aflæsing færslubókar</span><span class="sxs-lookup"><span data-stu-id="964fc-163">Journal unlock</span></span>
<span data-ttu-id="964fc-164">Hnappur er til á færslubókarsíðunni til að opna færslubók sem hefur stöðuna „læst af kerfinu“ stillt á Já.</span><span class="sxs-lookup"><span data-stu-id="964fc-164">A button is available on the journal page to unlock a journal that has a status of "locked by system" set to Yes.</span></span> <span data-ttu-id="964fc-165">Þessari aflæsingu er hægt að framkvæma af kerfisstjóra sem hefur greint hvaða framkvæmd hópastörf og staðfest að þessi færslubók er ekki lengur unnin af runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="964fc-165">This unlock can be performed by an administrator of the system who has analyzed any executing batch jobs and confirmed this journal is no longer actively being processed by a batch job.</span></span> <span data-ttu-id="964fc-166">Þessi hnappur virkjast með aðgerðinni sem heitir **Hnappur til að aflæsa færslubók** á síðunni **Stjórnun eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="964fc-166">This button is enabled by the feature named **Journal Unlock button** on the **Feature management** page.</span></span> 

## <a name="workflow-recall"></a><span data-ttu-id="964fc-167">Afturköllun verkflæðis</span><span class="sxs-lookup"><span data-stu-id="964fc-167">Workflow recall</span></span> 
<span data-ttu-id="964fc-168">Geta til að rifja upp dagbók í verkflæði sem hefur stöðuna „óendurheimtanleg“ er virk með því að nota hnappinn **Verkflæði** í dagbók og á síðunni **Verkflæðissaga**.</span><span class="sxs-lookup"><span data-stu-id="964fc-168">The ability to recall a journal in a workflow that has a status of "unrecoverable" is enabled by using the **Workflow** button on a journal, and on the **Workflow history** page.</span></span> <span data-ttu-id="964fc-169">Þetta er gert kleift með aðgerðinni sem heitir **Endurstilling á verkflæðisstöðu fyrir færslubækur** á síðunni **Stjórnun eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="964fc-169">This is enabled by the feature named **Resetting the workflow status for journals** on the **Feature management** page.</span></span>

## <a name="delete-journal-lines"></a><span data-ttu-id="964fc-170">Eyða færslubókarlínum</span><span class="sxs-lookup"><span data-stu-id="964fc-170">Delete Journal Lines</span></span>
<span data-ttu-id="964fc-171">Getan til að eyða öllum dagbókarlínum hratt er virk í dagbók undir **Aðgerðir** > **Eyða færslubókalínum**.</span><span class="sxs-lookup"><span data-stu-id="964fc-171">The ability to delete all journal lines quickly is enabled in a journal under **Functions** > **Delete Journal Lines**.</span></span> <span data-ttu-id="964fc-172">Til að virkja þennan eiginleika, á **Stjórnun eiginleika** skaltu velja **Eyða afkastafínstillingu færslubókar**.</span><span class="sxs-lookup"><span data-stu-id="964fc-172">To enable this feature, on the **Feature management**, select **Delete journal performance optimizations**.</span></span>
