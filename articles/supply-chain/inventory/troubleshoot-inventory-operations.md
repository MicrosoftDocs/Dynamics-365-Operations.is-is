---
title: Úrræðaleita birgðaaðgerðir
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með birgðaaðgerðir.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: ee1bfbf1b5aa736e1ee5bd38403b6c94c2bd036b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225003"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="fd570-103">Úrræðaleita birgðaaðgerðir</span><span class="sxs-lookup"><span data-stu-id="fd570-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd570-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með birgðaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="fd570-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="fd570-105">Ekki er hægt að finna felligluggann „Verkflæði“ fyrir birgðabækur.</span><span class="sxs-lookup"><span data-stu-id="fd570-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="fd570-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fd570-106">Issue description</span></span>

<span data-ttu-id="fd570-107">Ekki er hægt að **Verkflæði** felligluggann á færslusíðunni eða tengdar verkflæðisaðgerðir eru ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="fd570-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="fd570-108">Þrjár ástæður geta verið fyrir þessu vandamáli eins og lýst er í eftirfarandi undirköflum.</span><span class="sxs-lookup"><span data-stu-id="fd570-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="fd570-109">Úrlausn úrlausnaratriðis 1</span><span class="sxs-lookup"><span data-stu-id="fd570-109">Issue resolution 1</span></span>

<span data-ttu-id="fd570-110">Ef vandamálið á við alla notendur kann það að koma upp vegna þess að samþykktarverkflæði hefur ekki verið úthlutað á færslubókarheitið.</span><span class="sxs-lookup"><span data-stu-id="fd570-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="fd570-111">Til að laga úr vandamálið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="fd570-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="fd570-112">Farið í **Birgðastjórnun &gt; Uppsetning &gt; Færslubókarheiti &gt; Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="fd570-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="fd570-113">Veljið heiti færslubókar úr listadálknum til að opna stillingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="fd570-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="fd570-114">Á flipanum **Almennt** skal stilla **Samþykktarverkflæði** valkostinn á *Já*.</span><span class="sxs-lookup"><span data-stu-id="fd570-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="fd570-115">Ef notandi er beðinn um að staðfesta breytinguna skal velja **Já**.</span><span class="sxs-lookup"><span data-stu-id="fd570-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="fd570-116">Í reitnum **Verkflæði** skal velja verkflæðið sem á að nota fyrir valið heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="fd570-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="fd570-117">Úrlausn úrlausnaratriðis 2</span><span class="sxs-lookup"><span data-stu-id="fd570-117">Issue resolution 2</span></span>

<span data-ttu-id="fd570-118">Ef verkflæðið notar sérsniðinn kóða gætu vandamál komið upp eftir uppfærslu á kerfinu.</span><span class="sxs-lookup"><span data-stu-id="fd570-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="fd570-119">Í verkflæði færslubókar gæti til dæmis hnappurinn **Senda inn** verið skyggður þannig að ekki er hægt að velja hann til að samþykkja innsendingu.</span><span class="sxs-lookup"><span data-stu-id="fd570-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="fd570-120">Ef hnappurinn **Senda inn** er skyggður gæti verkflæðið hafa verið sérstillt, sem þýðir að aðferð verkflæðisins, `canSubmitToWorkflow()` í `FormDataUtil`, hafi verið stækkuð.</span><span class="sxs-lookup"><span data-stu-id="fd570-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="fd570-121">Til að laga þetta vandamál skal breyta því hvernig aðferð er stækkuð fyrir `canSubmitToWorkflow()` til að nota skipulagið í eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="fd570-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="fd570-122">Úrlausn úrlausnaratriðis 3</span><span class="sxs-lookup"><span data-stu-id="fd570-122">Issue resolution 3</span></span>

<span data-ttu-id="fd570-123">Ef vandamálið á aðeins við fáa tiltekna notendur gætu þessir notendur ekki haft þau öryggisréttindi sem krafist er til að keyra verkflæðisaðgerðir á birgðabókum.</span><span class="sxs-lookup"><span data-stu-id="fd570-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="fd570-124">Gangið úr skugga um að hver og neinn notandi hafi öryggisréttindin *Vinna með verkflæði í birgðabók*.</span><span class="sxs-lookup"><span data-stu-id="fd570-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="fd570-125">Sjálfgefið er að þessum réttindum sé úthlutað á skyldu sem er með sama heiti og skyldan er notuð í hlutverkunum *Starfsmaður í vöruhúsi* og *Vöruhúsastjórnandi*.</span><span class="sxs-lookup"><span data-stu-id="fd570-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="fd570-126">Birgðabókin mín er áfram í læstri stöðu og runuvinnsla verkflæðis virkar ekki.</span><span class="sxs-lookup"><span data-stu-id="fd570-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="fd570-127">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fd570-127">Issue description</span></span>

<span data-ttu-id="fd570-128">Ein af birgðabókum notanda er læst af einhverri aðgerð og ekki er verið að losa hana.</span><span class="sxs-lookup"><span data-stu-id="fd570-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="fd570-129">Ef óþekkt villa kemur til dæmis upp við bókun (sem er aðgerð kerfislæsingar) gæti færslubókin áfram verið í læstri stöðu.</span><span class="sxs-lookup"><span data-stu-id="fd570-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="fd570-130">Í þessu tilviki mun rekill vinnuliðar í verkflæði birta villu á meðan sannprófun á læsingu er gerð.</span><span class="sxs-lookup"><span data-stu-id="fd570-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fd570-131">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="fd570-131">Issue resolution</span></span>

<span data-ttu-id="fd570-132">Skráið ykkur inn í SQL-þjónstilvik fyrir Supply Chain Management og athugið hvort **InventJournalTable.SystemBlocked** sé stillt á *1*.</span><span class="sxs-lookup"><span data-stu-id="fd570-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="fd570-133">Ef svo er skal ganga úr skugga um að færslubókin eigi ekki að vera í læstri stöðu og síðan endurstilla **InventJournalTable.SystemBlocked** á *0*.</span><span class="sxs-lookup"><span data-stu-id="fd570-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="fd570-134">Verkflæði fyrir birgðabókina mína klárast aldrei og hvorki er hægt að breyta færslubókinni né bóka hana.</span><span class="sxs-lookup"><span data-stu-id="fd570-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="fd570-135">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fd570-135">Issue description</span></span>

<span data-ttu-id="fd570-136">Þegar búið er að senda inn samþykktarverkflæði færslubókar hættir verkflæðisferli að svara og ekki verður hægt að breyta eða vinna úr færslubókunum.</span><span class="sxs-lookup"><span data-stu-id="fd570-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fd570-137">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="fd570-137">Issue resolution</span></span>

<span data-ttu-id="fd570-138">Ýmsar ástæður eru fyrir því að ekki er hægt að ljúka við verkflæðisferli.</span><span class="sxs-lookup"><span data-stu-id="fd570-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="fd570-139">Kannið eftirfarandi vandamál:</span><span class="sxs-lookup"><span data-stu-id="fd570-139">Check for the following issues:</span></span>

- <span data-ttu-id="fd570-140">Opnið **Birgðastjórnun &gt; Uppsetning&gt; Verkflæði birgðastjórnunar**, og farið yfir skilgreininguna á verkflæðinu sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="fd570-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="fd570-141">Fyrir frekari upplýsingar sjá [Samþykktarverkflæði birgðabókar](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="fd570-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="fd570-142">Í verkflæðinu gæti hugsanlega hafa komið upp undantekning eða villa.</span><span class="sxs-lookup"><span data-stu-id="fd570-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="fd570-143">Farið yfir feril vinnuliðar í verkflæðinu sem um ræðir til að sjá hvort í honum sé forritsvilla sem stöðvar verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="fd570-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="fd570-144">Aðeins er hægt að uppfæra birgðabókina eða breyta henni ef hún er samþykkt.</span><span class="sxs-lookup"><span data-stu-id="fd570-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="fd570-145">Ef afturköllun er virk er hægt að reyna að afturkalla færslubókina.</span><span class="sxs-lookup"><span data-stu-id="fd570-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="fd570-146">Ekki er hægt að fresta keyrslu á runuvinnslunni af mörgum ástæðum.</span><span class="sxs-lookup"><span data-stu-id="fd570-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="fd570-147">Sumar af þessum ástæðum gætu stafað af vandamáli varðandi verkflæðisrammann.</span><span class="sxs-lookup"><span data-stu-id="fd570-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="fd570-148">Skilyrði verkflæðis birgðabókar gilda aðeins á færslubókarstigi, ekki á línustigi</span><span class="sxs-lookup"><span data-stu-id="fd570-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="fd570-149">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fd570-149">Issue description</span></span>

<span data-ttu-id="fd570-150">Þetta vandamál gæti komið upp ef til dæmis reynt er að setja upp skilyrði fyrir verkflæði birgðabókar í kostnaðarupphæðinni.</span><span class="sxs-lookup"><span data-stu-id="fd570-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="fd570-151">Skilyrði er sett upp þannig að skref 1 er aðeins keyrt þegar kostnaðarupphæðin er lægri en 100.</span><span class="sxs-lookup"><span data-stu-id="fd570-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="fd570-152">Síðan er sett upp annað skilyrði þannig að skref 2 er aðeins keyrt þegar kostnaðarupphæðin er hærri en eða jöfn og 100.</span><span class="sxs-lookup"><span data-stu-id="fd570-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="fd570-153">Því næst, þegar verkflæðið er keyrt, sýnir verkflæðissagan aðeins eina línu og fyrsta skilyrðið er alltaf metið sem *satt* burtséð frá gildinu sem er sent inn.</span><span class="sxs-lookup"><span data-stu-id="fd570-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="fd570-154">Lausn á vandamálinu</span><span class="sxs-lookup"><span data-stu-id="fd570-154">Issue workaround</span></span>

<span data-ttu-id="fd570-155">Í núverandi útgáfu eiga skilyrði í verkflæði birgðabókar aðeins við á færslubókarstigi, ekki á línustigi.</span><span class="sxs-lookup"><span data-stu-id="fd570-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="fd570-156">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="fd570-156">This behavior is by design.</span></span> <span data-ttu-id="fd570-157">Mælt er með því að skilyrðið sé aðeins sett á fyrir eigindir á færslubókarstigi.</span><span class="sxs-lookup"><span data-stu-id="fd570-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="fd570-158">Síusvæðið á listasíðu lagers síar ekki niðurstöður eins og ég geri ráð fyrir.</span><span class="sxs-lookup"><span data-stu-id="fd570-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="fd570-159">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fd570-159">Issue description</span></span>

<span data-ttu-id="fd570-160">Síurnar á síusvæðinu á **Listasíða lagers** síðunni sía ekki niðurstöður eins og þú gerir ráð fyrir.</span><span class="sxs-lookup"><span data-stu-id="fd570-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fd570-161">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="fd570-161">Issue resolution</span></span>

<span data-ttu-id="fd570-162">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="fd570-162">This behavior is by design.</span></span>

<span data-ttu-id="fd570-163">Síðan  **Lagerlisti**  er sett saman úr ítarlegri töflu yfir lagerbirgðir sem inniheldur allar tiltækar víddir.</span><span class="sxs-lookup"><span data-stu-id="fd570-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="fd570-164">Listinn á þessari síðu er hins vegar samantekt.</span><span class="sxs-lookup"><span data-stu-id="fd570-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="fd570-165">Hann gæti þar af leiðandi sameinað línur úr upprunatöflunni með því að leggja saman gildi samkvæmt víddunum sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="fd570-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="fd570-166">Síur sem eru settar upp á síusvæðinu eiga við upprunatöfluna, ekki uppsafnaðan lista.</span><span class="sxs-lookup"><span data-stu-id="fd570-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="fd570-167">Þessi hegðun getur stundum leitt til óvæntrar niðurstöðu eins og lýst er í [þessum dæmum](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="fd570-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="fd570-168"> [Síurnar sem gefnar eru upp í hnitanetinu](inventory-on-hand-list.md#grid-filters)  \*eiga*  hinsvegar við samanlagða listann.</span><span class="sxs-lookup"><span data-stu-id="fd570-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="fd570-169">Þessar síur fela í sér bæði QuickFilter efst í hnitanetinu og síuna fyrir hvern dálkahaus.</span><span class="sxs-lookup"><span data-stu-id="fd570-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="fd570-170">Eining og magn einingar virka ekki á réttan hátt í birgðabókinni.</span><span class="sxs-lookup"><span data-stu-id="fd570-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="fd570-171">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fd570-171">Issue description</span></span>

<span data-ttu-id="fd570-172">Annað eða bæði þessi vandamál gætu komið upp þegar unnið er með einingar og magn í birgðabók:</span><span class="sxs-lookup"><span data-stu-id="fd570-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="fd570-173">Ekki er hægt að breyta einingum eða magni í birgðabókinni á meðan umreikningseining er sett upp fyrir útgefna afurð og ekki er hægt að skipta um einingu í birgðabókinni.</span><span class="sxs-lookup"><span data-stu-id="fd570-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="fd570-174">Reitirnir **Magn** og **Eining** sjást í birgðabókinni, en reiturinn **Magn einingar** sést ekki.</span><span class="sxs-lookup"><span data-stu-id="fd570-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="fd570-175">Ef einingunni er breytt skal færa inn magn og bóka færslubókina, færslubókin sýnir enn upprunalega mælieininguna fyrir það magn.</span><span class="sxs-lookup"><span data-stu-id="fd570-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fd570-176">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="fd570-176">Issue resolution</span></span>

<span data-ttu-id="fd570-177">Til að laga þetta vandamál skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="fd570-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="fd570-178">Á vinnusvæðinu **Eiginleikastjórnun** skal ganga úr skugga um að kveikt sé á eiginleikanum *Notkun mælieiningar og einingarmagns í birgðabókum*.</span><span class="sxs-lookup"><span data-stu-id="fd570-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="fd570-179">Þessi eiginleiki bætir reitunum **Eining** og **Magn einingar** við færslubókina.</span><span class="sxs-lookup"><span data-stu-id="fd570-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="fd570-180">Þegar kveikt hefur verið á eiginleikanum skal nota reitina **Magn**, **Magn einingar** og **Eining** á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="fd570-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="fd570-181">**Magn** – Tilgreinið magnið með því að nota sjálfgefna einingu sem er skilgreind fyrir útgefna afurð.</span><span class="sxs-lookup"><span data-stu-id="fd570-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="fd570-182">Sjálfgefin eining er hins vegar ekki sýnd hér.</span><span class="sxs-lookup"><span data-stu-id="fd570-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="fd570-183">Ef umreikningur er uppsettur milli sjálfgefinnar einingar og einingarinnar sem er valin í reitnum **Eining** verður reiturinn **Magn** uppfærður sjálfkrafa út frá því sem er valið í reitunum **Magn einingar** og **Eining**.</span><span class="sxs-lookup"><span data-stu-id="fd570-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="fd570-184">**Magn einingar** – Tilgreinið magnið með því að velja eininguna sem er valin í reitnum **Eining**.</span><span class="sxs-lookup"><span data-stu-id="fd570-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="fd570-185">**Eining** – Veljið eininguna sem á að nota fyrir gildið í reitnum **Magn einingar**.</span><span class="sxs-lookup"><span data-stu-id="fd570-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="fd570-186">Ég fæ eftirfarandi villuskilaboð: „Hámarksfjöldi aukastafa fyrir birgðahaldseininguna er 0.“</span><span class="sxs-lookup"><span data-stu-id="fd570-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fd570-187">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fd570-187">Issue description</span></span>

<span data-ttu-id="fd570-188">Þegar reynt er að bóka birgðafærslu eða birgðafrátekningu koma upp eftirfarandi villuboð: „Hámarksfjöldi aukastafa fyrir birgðahaldseininguna er 0.“</span><span class="sxs-lookup"><span data-stu-id="fd570-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="fd570-189">Þetta vandamál kemur upp þegar magn birgðafærslunnar er tilgreint sem gildi í aukastöfum sem er undir nákvæmnismörkunum sem reiturinn styður.</span><span class="sxs-lookup"><span data-stu-id="fd570-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="fd570-190">Til dæmis *hefur magn 0,5* verið tilgreint fyrir birgðafærsluna en aðeins heiltölumagn er stutt.</span><span class="sxs-lookup"><span data-stu-id="fd570-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="fd570-191">Þess vegna ætti gildið að vera *1* í stað *0,5*.</span><span class="sxs-lookup"><span data-stu-id="fd570-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fd570-192">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="fd570-192">Issue resolution</span></span>

1. <span data-ttu-id="fd570-193">Keyrið eftirfarandi forskrift í tilviki SQL Server til að slétta magn í birgðafærslum.</span><span class="sxs-lookup"><span data-stu-id="fd570-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="fd570-194">Þessi forskrift mun leiðrétta gildi í töflunni **inventTrans** .</span><span class="sxs-lookup"><span data-stu-id="fd570-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="fd570-195">Keyra skal samræmisathugun á birgðum þar sem kveikt er á valkostinum **Leiðrétta villu**.</span><span class="sxs-lookup"><span data-stu-id="fd570-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="fd570-196">Þessi athugun mun leiðrétta gildi í tölfunni **inventSum**.</span><span class="sxs-lookup"><span data-stu-id="fd570-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd570-197">Sérstaklega er mælt með því að fara gætilega þegar forskriftinni er breytt samkvæmt þörfum umhverfisins, prófið hana í prófunarumhverfi og athugið síðan niðurstöðurnar áður en forskriftin er keyrð í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="fd570-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]