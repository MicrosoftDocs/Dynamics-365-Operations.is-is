---
title: "Sjálfvirkni reikninga lánardrottins"
description: "Í þessu efnisatriði er fjallað um aðgerðir sem eru tiltækar fyrir lok við lok sjálfvirkni reikninga lánardrottins, jafnvel reikninga með viðhengi."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 75865ece49837e2a8758c4d739d3e29ce9128945
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="11b2f-103">Sjálfvirkni reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11b2f-103">Vendor invoice automation</span></span>

<span data-ttu-id="11b2f-104">Í þessu efnisatriði er fjallað um aðgerðir sem eru tiltækar fyrir lok við lok sjálfvirkni reikninga lánardrottins, jafnvel reikninga með viðhengi.</span><span class="sxs-lookup"><span data-stu-id="11b2f-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="11b2f-105">Fyrirtæki sem vilja hagræða ferlum Viðskiptaskulda (AP) auðkenna oft reikningsvinnslur sem ein af aðalferlunum sem þurfa að vera skilvirkari.</span><span class="sxs-lookup"><span data-stu-id="11b2f-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="11b2f-106">Í mörgum tilvikum láta þessi fyrirtæki ótengdan þjónustuaðila með ljósskynjun stafa (OCR) um vinnslu reikninga á pappír.</span><span class="sxs-lookup"><span data-stu-id="11b2f-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="11b2f-107">Þeir fá síðan tölvulesanleganleg lýsigögn reiknings ásamt skannaðri mynd af hverjum reikningi.</span><span class="sxs-lookup"><span data-stu-id="11b2f-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="11b2f-108">Til að aðstoða við sjálfvirkni er "síðasta kílómetra" lausn síðan myndað til að auðvelda notkun á þessum hlutum í reikningsfærslukerfinu.</span><span class="sxs-lookup"><span data-stu-id="11b2f-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="11b2f-109">Núna gerir Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kleift að gera þessa "síðasta kílómetra" sjálfvirkni úr kassa með á reikningi lausn sjálfvirkni.</span><span class="sxs-lookup"><span data-stu-id="11b2f-109">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="11b2f-110">Lausnasamhengi</span><span class="sxs-lookup"><span data-stu-id="11b2f-110">Solution context</span></span>

<span data-ttu-id="11b2f-111">Reikningur sjálfvirkni lausn virkjar staðlað viðmót sem getur samþykkt reiknings lýsigögn á reikningshausinn og reikningslínur og viðhengjum sem á við um reikninginn.</span><span class="sxs-lookup"><span data-stu-id="11b2f-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="11b2f-112">Öll utanaðkomandi kerfi, sem getur myndað gervinga sem samræmast þessu viðmóti munu geta sent færslurnar inn í for Finance and Operations, Enterprise edition til sjálfvirkrar vinnsu á reikningum og viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="11b2f-113">Eftirfarandi skýringarmynd sýnir sýnishorn af samþættingaraðstæðum þar sem Contoso hefur gerst meðeigandi með OCR-þjónustuveitanda fyrir vinnslu á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="11b2f-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="11b2f-114">Lánardrottnar Contoso senda reikninga til þjónustuveitu með tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="11b2f-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="11b2f-115">Í gegnum OCR-vinnslu myndar þjónustuveitan lýsigögn reikningsins (haus og/eða línur) og skannaða mynd af reikningnum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="11b2f-116">Samþættingarlag umbreytir þessum gervingum síðan þannig að Finance and Operations geta nota þær.</span><span class="sxs-lookup"><span data-stu-id="11b2f-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![Dæmi um samþættingaraðstæður](media/vendor_invoice_automation_01.png)

<span data-ttu-id="11b2f-118">Nokkur tilbrigði með fyrrgreint dæmi eru mögulegur ef samþætting reiknings er nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="11b2f-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="11b2f-119">Gagnaflutningur er dæmi um aðra notkun þar sem hægt er að nota þetta viðmót til að stofna reikninga og viðhengi í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11b2f-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="11b2f-120">Lausnaíhlutir</span><span class="sxs-lookup"><span data-stu-id="11b2f-120">Solution components</span></span>

<span data-ttu-id="11b2f-121">Lausnafótsporið samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="11b2f-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="11b2f-122">Gagnaeiningar fyrir reikningshausinn, línur á reikningi og reikningsviðhengi</span><span class="sxs-lookup"><span data-stu-id="11b2f-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="11b2f-123">Undantekningavinnsla fyrir reikninga</span><span class="sxs-lookup"><span data-stu-id="11b2f-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="11b2f-124">Hlið-við-hlið viðhengjabirtir í reikningum</span><span class="sxs-lookup"><span data-stu-id="11b2f-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="11b2f-125">Afgangurinn af þessu efnisatriði gefur ítarlegar lýsingar á þessum lausnaþáttum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="11b2f-126">Gagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="11b2f-126">Data entities</span></span>

<span data-ttu-id="11b2f-127">Gagnapakki er sú vinnueining sem þarf að senda til Finance and Operations, svo að hægt sé að stofna reikningshausa, reikningslínur og reikningsviðhengi.</span><span class="sxs-lookup"><span data-stu-id="11b2f-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="11b2f-128">Eftirfarandi gagnaeiningar eru notaðar fyrir gervinga sem mynda gögn pakka:</span><span class="sxs-lookup"><span data-stu-id="11b2f-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="11b2f-129">Reikningshaus lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11b2f-129">Vendor invoice header</span></span>
+ <span data-ttu-id="11b2f-130">Reikningslína lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11b2f-130">Vendor invoice line</span></span>
+ <span data-ttu-id="11b2f-131">Viðhengi reikningsskjals lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11b2f-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="11b2f-132">Skjalaviðhengi lánardrottnareikningsins er ný gagnaeining sem er kynnt sem hluti af þessari aðgerð.</span><span class="sxs-lookup"><span data-stu-id="11b2f-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="11b2f-133">Hauseining lánardrottnareiknings hefur verið breytt þannig að hann styður viðhengi.</span><span class="sxs-lookup"><span data-stu-id="11b2f-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="11b2f-134">Línueining lánardrottnareiknings hefur ekki verið breytt fyrir þetta sérkenni.</span><span class="sxs-lookup"><span data-stu-id="11b2f-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="11b2f-135">Þetta efnisatriði veitir ekki nákvæma skilgreiningu á gagnapakka.</span><span class="sxs-lookup"><span data-stu-id="11b2f-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="11b2f-136">Það útskýrir ekki heldur hvernig á að stofna gagnapakka.</span><span class="sxs-lookup"><span data-stu-id="11b2f-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="11b2f-137">Þessar upplýsingar eru í [Rammi fyrir gagnaeiningar og -pakka](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="11b2f-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="11b2f-138">Fylgið eftirfarandi skrefum til að mynda prófun gagna sem inniheldur reikninga og viðhengja.</span><span class="sxs-lookup"><span data-stu-id="11b2f-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="11b2f-139">Skráðu þig in í tilvik Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11b2f-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="11b2f-140">Fara í **Viðskiptaskuldir** > **Reikningar** > **Opna lánardrottnareikninga**.</span><span class="sxs-lookup"><span data-stu-id="11b2f-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="11b2f-141">Stofna reikninga sem hafa línur og viðhengi.</span><span class="sxs-lookup"><span data-stu-id="11b2f-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="11b2f-142">Viðhengin verða að vera viðhengi við haus.</span><span class="sxs-lookup"><span data-stu-id="11b2f-142">The attachments must be header attachments.</span></span> <span data-ttu-id="11b2f-143">Sem stendur styður skjalaviðhengjaeining lánardrottnareiknings ekki viðhengi við línur.</span><span class="sxs-lookup"><span data-stu-id="11b2f-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="11b2f-144">Opnaðu vinnusvæðið **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="11b2f-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="11b2f-145">Stofna útflutningsvinnslu sem inniheldur reikningshaus lánardrottins, reikningslínu lánardrottins og skjalaviðhengiseiningu lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="11b2f-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="11b2f-146">Flyttu út gögnin.</span><span class="sxs-lookup"><span data-stu-id="11b2f-146">Export the data.</span></span>
1. <span data-ttu-id="11b2f-147">Sæktu útflutt gögnin sem pakka.</span><span class="sxs-lookup"><span data-stu-id="11b2f-147">Download the exported data as a package.</span></span> <span data-ttu-id="11b2f-148">Nú má nota pakkanum til að flytja gögn inn í marktilvik til prófunar.</span><span class="sxs-lookup"><span data-stu-id="11b2f-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="11b2f-149">Ákvörðun lögaðila fyrir reikning</span><span class="sxs-lookup"><span data-stu-id="11b2f-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="11b2f-150">Reikningar sem eru innfluttir með gagnapakka er hægt að tengja lögaðila sem þeir tilheyra á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="11b2f-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="11b2f-151">Innflutningsvinnslan sem vinnur reikninginn flytur hann inn í sama fyrirtækið sem þar vinnslan var í röðun á vinnusvæðinu **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="11b2f-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="11b2f-152">Með öðrum orðum ákvarðar fyrirtæki vinnslunnar fyrirtækið sem reikningurinn tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="11b2f-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="11b2f-153">Þegar gagnapakki sem inniheldur reikninga er sendur til Finance and Operations, getur hringjandi (þ.e.a.s. samþættingarforritið sem keyrir utan Finance and Operations) nefnt kenni fyrirtækisins skýrt í HTTP-beiðninni.</span><span class="sxs-lookup"><span data-stu-id="11b2f-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="11b2f-154">Í þessu tilfelli er fyrirtækjasamhenginu sem keyrir vinnsluna í Finance and Operations hnekkt og reikningarnir eru fluttir inn í fyrirtækið sem var beint í gegnum svar HTTP.</span><span class="sxs-lookup"><span data-stu-id="11b2f-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="11b2f-155">Þessi hegðun er stöðluð gagnastjórnunarhegðun.</span><span class="sxs-lookup"><span data-stu-id="11b2f-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="11b2f-156">Það er útskýrt hér, í samhengi við reikninga, fyrir sakir heildarinnar.</span><span class="sxs-lookup"><span data-stu-id="11b2f-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="11b2f-157">Undantekningavinnsla</span><span class="sxs-lookup"><span data-stu-id="11b2f-157">Exception processing</span></span>

<span data-ttu-id="11b2f-158">Í tilvikum þar sem reikningar lánardrottna koma inn í Finance and Operations í gegnum samþættingu, verður að vera auðveld leið fyrir inn Reikninga lánardrottna hópur undantekningar ferli eða mistekist reikninga og til að stofna reikninga í bið úr reikningum sem mistakast.</span><span class="sxs-lookup"><span data-stu-id="11b2f-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="11b2f-159">Þessi undantekningavinnsla á reikningum lánadrottna er nú hluti af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11b2f-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="11b2f-160">Listasíða undantekninga</span><span class="sxs-lookup"><span data-stu-id="11b2f-160">Exceptions list page</span></span>

<span data-ttu-id="11b2f-161">Nýja listasíðan fyrir reikningsundantekningar er alltaf tiltæk í **Viðskiptaskuldum** > **Reikningum** > **Flytja verkefnismistök** > **reikningar Lánardrottins sem hefur mistekist að flytja**.</span><span class="sxs-lookup"><span data-stu-id="11b2f-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="11b2f-162">Þessi síða sýnir allar hausfærslur lánardrottnareiknings úr sviðsetningartöflunni í gagnaeiningu hauss lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="11b2f-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="11b2f-163">Athugið að hægt er að skoða sömu skrár á vinnusvæðinu **Gagnastjórnun** þar sem er einnig hægt að framkvæma sömu aðgerðir sem eru gefnar í undantekningunni meðhöndlun aðgerð.</span><span class="sxs-lookup"><span data-stu-id="11b2f-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="11b2f-164">Hins vegar UI sem undantekningin meðhöndlunaraðgerð veitir bestuð fyrir virkan notanda.</span><span class="sxs-lookup"><span data-stu-id="11b2f-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Listasíða undantekninga](media/vendor_invoice_automation_02.png)

<span data-ttu-id="11b2f-166">Þessi listasíða felur í sér eftirtalin svæði sem berast inn í gegnum streymi:</span><span class="sxs-lookup"><span data-stu-id="11b2f-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="11b2f-167">**Fyrirtæki** – Það fyrirtæki sem reikningurinn tilheyrir</span><span class="sxs-lookup"><span data-stu-id="11b2f-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="11b2f-168">**Villuboð** – Villuboðin sem ramminn stjórnun gagna úthreyfingar til að útskýra af hverju ekki var hægt að stofna reikning</span><span class="sxs-lookup"><span data-stu-id="11b2f-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="11b2f-169">**Númer** – Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="11b2f-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="11b2f-170">**Reikningslykill**</span><span class="sxs-lookup"><span data-stu-id="11b2f-170">**Invoice account**</span></span>
+ <span data-ttu-id="11b2f-171">**Nafn** – Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11b2f-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="11b2f-172">**Lykill lánardrottins**</span><span class="sxs-lookup"><span data-stu-id="11b2f-172">**Vendor account**</span></span>
+ <span data-ttu-id="11b2f-173">**Innkaupapöntun** – Númer innkaupapöntunar fyrir reikninginn</span><span class="sxs-lookup"><span data-stu-id="11b2f-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="11b2f-174">**Bókunardagsetning**</span><span class="sxs-lookup"><span data-stu-id="11b2f-174">**Posting date**</span></span>
+ <span data-ttu-id="11b2f-175">**Reikningsdagsetning**</span><span class="sxs-lookup"><span data-stu-id="11b2f-175">**Invoice date**</span></span>
+ <span data-ttu-id="11b2f-176">**Lýsing reiknings**</span><span class="sxs-lookup"><span data-stu-id="11b2f-176">**Invoice description**</span></span>
+ <span data-ttu-id="11b2f-177">**Gjaldmiðill**</span><span class="sxs-lookup"><span data-stu-id="11b2f-177">**Currency**</span></span>
+ <span data-ttu-id="11b2f-178">**Kladdi**</span><span class="sxs-lookup"><span data-stu-id="11b2f-178">**Log**</span></span>
+ <span data-ttu-id="11b2f-179">**Línutilvísun** – Kennið sem er fengið frá utanaðkomandi kerfi</span><span class="sxs-lookup"><span data-stu-id="11b2f-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="11b2f-180">Línutilvísun er ekki reikningskenni.</span><span class="sxs-lookup"><span data-stu-id="11b2f-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="11b2f-181">Þessi listasíða hefur einnig forskoðunarrúðu sem þú getur notað á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="11b2f-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="11b2f-182">Skoða öll villuboðin svo að ekki þurfi að útvíkka dálkinn **Villuboð** í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="11b2f-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="11b2f-183">Skoða allan listann yfir viðhengi fyrir reikninginn, ef einhver viðhengi fylgdu með reikningnum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="11b2f-184">Listasíðan styður eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="11b2f-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="11b2f-185">**Breyta** – Opna undantekningarfærsluna í breytingarham, þannig að hægt sé að laga vandamálin.</span><span class="sxs-lookup"><span data-stu-id="11b2f-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="11b2f-186">**Valkostir** – Farðu í staðlaða valkostina sem eru tiltækir á listasíðunum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="11b2f-187">Hægt er að nota valkostinn **Bæta við vinnusvæði** til að festa listasíðu undantekninga á vinnusvæðið sem lista eða reit.</span><span class="sxs-lookup"><span data-stu-id="11b2f-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="11b2f-188">Upplýsingasíða undantekninga</span><span class="sxs-lookup"><span data-stu-id="11b2f-188">Exception details page</span></span>

<span data-ttu-id="11b2f-189">Þegar breytingastillingar eru opnaðar birtis upplýsingasíða fyrir reikninginn sem er með vandamál.</span><span class="sxs-lookup"><span data-stu-id="11b2f-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="11b2f-190">Ef einhver viðhengi eru til staðar birtast reikningurinn og sjálfgefna viðhengið hlið við hlið á upplýsingasíðu um undantekningar.</span><span class="sxs-lookup"><span data-stu-id="11b2f-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Upplýsingasíða undantekninga](media/vendor_invoice_automation_03.png)

<span data-ttu-id="11b2f-192">Á fyrrigreindi mynd voru engar línur fyrir reikningshaus lánardrottins sem kom inn.</span><span class="sxs-lookup"><span data-stu-id="11b2f-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="11b2f-193">Þess vegna er línuhlutinn í kaflanum auður.</span><span class="sxs-lookup"><span data-stu-id="11b2f-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="11b2f-194">Upplýsingasíða um undantekningar styður eftirfarandi aðgerð:</span><span class="sxs-lookup"><span data-stu-id="11b2f-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="11b2f-195">**Stofna reikning í bið** – Þegar vandamál á reikningnum hafa verið löguð sem hluti af undantekningavinnslu, er hægt að smella á þennan hnapp til að stofna reikning í bið.</span><span class="sxs-lookup"><span data-stu-id="11b2f-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="11b2f-196">Stofnun reikninga fer fram í bakgrunni (eins og ósamstillt aðgerð).</span><span class="sxs-lookup"><span data-stu-id="11b2f-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="11b2f-197">Samnýtt þjónusta samanb. v. fyrirtækjabyggða undantekningavinnslu</span><span class="sxs-lookup"><span data-stu-id="11b2f-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="11b2f-198">Listasíða undantekninga styður staðlaða öryggisbyggingu sem vinnusvæðið **Gagnastjórnun** styður fyrir vinnslu á stigaðgerðir færslur.</span><span class="sxs-lookup"><span data-stu-id="11b2f-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="11b2f-199">Hægt er að tryggja innflutningsvinnslu reiknings á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="11b2f-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="11b2f-200">Eftir notandahlutverki</span><span class="sxs-lookup"><span data-stu-id="11b2f-200">By user role</span></span>
+ <span data-ttu-id="11b2f-201">Eftir notanda</span><span class="sxs-lookup"><span data-stu-id="11b2f-201">By user</span></span>
+ <span data-ttu-id="11b2f-202">Eftir lögaðila</span><span class="sxs-lookup"><span data-stu-id="11b2f-202">By legal entity</span></span>

![Innflutningsvinnsla sem er tryggð eftir hlutverki notanda og lögaðila](media/vendor_invoice_automation_04.png)

<span data-ttu-id="11b2f-204">Ef öryggi er skilgreint fyrir innflutningsvinnslu reiknings virðir listasíða undantekninga þessar stillingar.</span><span class="sxs-lookup"><span data-stu-id="11b2f-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="11b2f-205">Notendur geta aðeins séð undantekningafærslur reikninga sem þessi uppsetning leyfir þeim að sjá.</span><span class="sxs-lookup"><span data-stu-id="11b2f-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="11b2f-206">Til dæmis hefur Contoso ákveðið að keyra reikningsundantekningar eftir lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="11b2f-207">Þar af leiðandi er öryggi skilgreint í innflutningsvinnslu reikninga á þann hátt að notandi í lögaðila A getur aðeins séð undantekningar reikninga í lögaðila A, en notandi í lögaðila B getur aðeins séð undantekningar reikninga í lögaðila B. Þessi uppsetning virkjar aðskilnað á skyldum fyrir stjórnun á undantekningum reikninga.</span><span class="sxs-lookup"><span data-stu-id="11b2f-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="11b2f-208">Contoso gæti einnig ákveðið að tryggja ekki neitt öryggi, þannig að notendur geti keyrt undantekningar reikninga fyrir allar einingar lögaðila.</span><span class="sxs-lookup"><span data-stu-id="11b2f-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="11b2f-209">Þessi uppsetning virkjar samnýtta þjónustuaðstæður fyrir stjórnun á undantekningum reikninga.</span><span class="sxs-lookup"><span data-stu-id="11b2f-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="11b2f-210">Hlið-við-hlið viðhengjabirtir</span><span class="sxs-lookup"><span data-stu-id="11b2f-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="11b2f-211">Til að aðstoða við að skoða viðhengi fyrir reikninga lánardrottins, veita eftirfarandi síður sem eru notaðar í reikningsfærslunni núna viðhengjabirti:</span><span class="sxs-lookup"><span data-stu-id="11b2f-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="11b2f-212">**Meðhöndlun undantekninga**</span><span class="sxs-lookup"><span data-stu-id="11b2f-212">**Exception handling**</span></span>
+ <span data-ttu-id="11b2f-213">Síðan **Lánardrottnareikningar í bið** (einnig tiltæk i endurskoðunarferli reikninga)</span><span class="sxs-lookup"><span data-stu-id="11b2f-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="11b2f-214">Fyrirspurnasíða **Reikningabók** (fyrir bókaða reikninga)</span><span class="sxs-lookup"><span data-stu-id="11b2f-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="11b2f-215">Hér eru aðalaðgerðir sem viðhengjabirtirinn veitir:</span><span class="sxs-lookup"><span data-stu-id="11b2f-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="11b2f-216">Skoðið allar viðhengjagerðir sem skjalastjórnun styður (skrár myndir, Vefföng og athugasemdir).</span><span class="sxs-lookup"><span data-stu-id="11b2f-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="11b2f-217">Skoða TIFF-skrár með mörgum síðum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="11b2f-218">Framkvæmið eftirfarandi aðgerðir í myndaskrám:</span><span class="sxs-lookup"><span data-stu-id="11b2f-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="11b2f-219">Merkið hluta myndarinnar.</span><span class="sxs-lookup"><span data-stu-id="11b2f-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="11b2f-220">Felur hluta myndarinnar.</span><span class="sxs-lookup"><span data-stu-id="11b2f-220">Block parts of the image.</span></span>
  + <span data-ttu-id="11b2f-221">Bæta athugasemdum við myndina.</span><span class="sxs-lookup"><span data-stu-id="11b2f-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="11b2f-222">Þysjar inn og út á myndina.</span><span class="sxs-lookup"><span data-stu-id="11b2f-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="11b2f-223">Víðmynd myndarinnar.</span><span class="sxs-lookup"><span data-stu-id="11b2f-223">Pan the image.</span></span>
  + <span data-ttu-id="11b2f-224">Afturkalla og endurgera aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="11b2f-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="11b2f-225">Breyttu myndarinni svo að hún passi.</span><span class="sxs-lookup"><span data-stu-id="11b2f-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="11b2f-226">Þessar aðgerðir eru tiltækar fyrir myndskrár (JPEG, TIFF, PNG og svo framvegis).</span><span class="sxs-lookup"><span data-stu-id="11b2f-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="11b2f-227">Allar breytingar sem gerðar eru á mynd með því að nota þessar aðgerðir eru vistaðar í myndskrá.</span><span class="sxs-lookup"><span data-stu-id="11b2f-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="11b2f-228">Eins og stendur felur viðhengjabirtir ekki í sér útgáfu- eða endurskoðunargetu.</span><span class="sxs-lookup"><span data-stu-id="11b2f-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="11b2f-229">Sjálfgefið viðhengi</span><span class="sxs-lookup"><span data-stu-id="11b2f-229">Default attachment</span></span>

<span data-ttu-id="11b2f-230">Ef reikningur lánardrottins hefur fleiri en eitt viðhengi er hægt að stilla eitt af skjölunum sem sjálfgefið viðhengi á síðunni **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="11b2f-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="11b2f-231">Valkosturinn **Er sjálfgefið viðhengi** er nýr valkostur sem var bætt við sem hluta af þessum aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="11b2f-232">Þessi valkostur er líka sýndur í gagnaeiningu skjalaviðhengis lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="11b2f-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="11b2f-233">Þess vegna er hægt að stilla sjálfgefið viðhengi í gegnum samþættingar.</span><span class="sxs-lookup"><span data-stu-id="11b2f-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="11b2f-234">Aðeins er hægt að stilla eitt skjal sem sjálfgefið viðhengi.</span><span class="sxs-lookup"><span data-stu-id="11b2f-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="11b2f-235">Eftir að skjal er stillt sem sjálfgefið viðhengi er það sjálfkrafa sýnt í viðhengjabirti þegar reikningurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="11b2f-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="11b2f-236">Ef ekkert skjal er stillt sem sjálfgefið viðhengi sýnir birtirinn ekki sjálfkrafa nein viðhengi þegar reikningurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="11b2f-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="11b2f-237">Sýna/fela reikningsviðhengi</span><span class="sxs-lookup"><span data-stu-id="11b2f-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="11b2f-238">Ný hnappur sem er tiltækur á fyrirspurnasíðunum **Undantekningar vinnslu**, **Reikningur í bið** og **Reikningabók** gerir kleift að sýna eða fela viðhengjabirtinn.</span><span class="sxs-lookup"><span data-stu-id="11b2f-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="11b2f-239">Öryggi</span><span class="sxs-lookup"><span data-stu-id="11b2f-239">Security</span></span>

<span data-ttu-id="11b2f-240">Eftirfarandi aðgerðum í viðhengjabirti er stjórnað með öryggi eftir hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="11b2f-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="11b2f-241">Auðkennt</span><span class="sxs-lookup"><span data-stu-id="11b2f-241">Highlighting</span></span>
+ <span data-ttu-id="11b2f-242">Varið</span><span class="sxs-lookup"><span data-stu-id="11b2f-242">Block</span></span>
+ <span data-ttu-id="11b2f-243">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="11b2f-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="11b2f-244">Síðan Lánardrottnareikningar í bið</span><span class="sxs-lookup"><span data-stu-id="11b2f-244">Pending vendor invoices page</span></span>

<span data-ttu-id="11b2f-245">Eftirfarandi réttindi veita aðgang tilbúna-aðeins eða les/skrif aðgang að viðhengjabirti fyrir því að merkingar-, blokkunar- og ahtugasemdaaðgerðir:</span><span class="sxs-lookup"><span data-stu-id="11b2f-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="11b2f-246">**Viðhalda mynd lánardrottnareiknings** – Þessi réttindi veta les/skrif aðgang.</span><span class="sxs-lookup"><span data-stu-id="11b2f-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="11b2f-247">**Skoða mynd lánardrottnareiknings** – Þessi réttindi veta lesaðgang.</span><span class="sxs-lookup"><span data-stu-id="11b2f-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="11b2f-248">Eftirfarandi skyldur veita aðeins lesaðgang eða les/skrif aðgang að viðhengjabirti fyrir þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="11b2f-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="11b2f-249">**Viðhalda lánardrottnareikningum** – Myndaréttindin Viðhalda lánardrottnareikningi eru tengd þessum skyldum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="11b2f-250">**Gera fyrirspurn um reikningsstöðu lánardrottins** – Myndaréttindin Skoða lánardrottnareikningi eru tengd þessum skyldum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="11b2f-251">Eftirfarandi hlutverk veita aðeins lesaðgang eða les/skrif aðgang að viðhengjabirti fyrir þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="11b2f-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="11b2f-252">**Afgreiðslumaður viðskiptaskulda** og **Stjórnandi viðskiptaskulda** – Skyldan Viðhalda lánardrottnareikningum er úthlutað á þessum hlutverk.</span><span class="sxs-lookup"><span data-stu-id="11b2f-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="11b2f-253">**Afgreiðslumaður lánardrottna**, **stjórnanda lánardrottna**, **Lykla lánardrottna miðstýrðar greiðslur afgreiðslumaður**, og **Lykla lánardrottna greiðslur afgreiðslumaður** – í Spyrjast fyrir um lánardrottinn reikningi stöðuna gjald er úthlutað á þessum hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="11b2f-254">Upplýsingasíða reikningsundantekninga</span><span class="sxs-lookup"><span data-stu-id="11b2f-254">Invoice exception details page</span></span>

<span data-ttu-id="11b2f-255">Eftirfarandi réttindi veita aðgang tilbúna-aðeins eða les/skrif aðgang að viðhengjabirti fyrir því að merkingar-, blokkunar- og ahtugasemdaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="11b2f-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="11b2f-256">Hlutverk sem eru nefnd í þessum hluta veita aðeins til lestrar aðgang að myndir reikning í viðhengjabirti utan í reitinn.</span><span class="sxs-lookup"><span data-stu-id="11b2f-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="11b2f-257">Ef hlutverk verður einnig að hafa skrifaðgang að myndunum, má veita skrifaðgang að því hlutverki með heimildinni og gjald sem er lýst hér.</span><span class="sxs-lookup"><span data-stu-id="11b2f-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="11b2f-258">**Viðhalda lánardrottni reikningsins haus einingar mynd** – Þessa heimildinni veitir les/skrif aðgang að reikningur myndirnar í viðhengjabirti.</span><span class="sxs-lookup"><span data-stu-id="11b2f-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="11b2f-259">**Skoða lánardrottni reikningsins haus einingar mynd** – Þessa heimildinni veitir les aðgang að reikningsmyndinni í viðhengjabirti.</span><span class="sxs-lookup"><span data-stu-id="11b2f-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="11b2f-260">Eftirfarandi skyldur veita aðeins lesaðgang að viðhengjabirti fyrir þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="11b2f-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="11b2f-261">**Viðhalda lánardrottnareikningum** – Myndaréttindin Viðhalda hauseiningu lánardrottnareiknings eru tengd þessum skyldum.</span><span class="sxs-lookup"><span data-stu-id="11b2f-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="11b2f-262">Eftirfarandi hlutverk veita aðeins lesaðgang að viðhengjabirti fyrir þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="11b2f-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="11b2f-263">**Afgreiðslumaður viðskiptaskulda** og **Stjórnandi viðskiptaskulda** – Skyldan Viðhalda lánardrottnareikningum er úthlutað á þessum hlutverk.</span><span class="sxs-lookup"><span data-stu-id="11b2f-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="11b2f-264">Sjálfgefið ef hlutverki notanda veitir breyta réttindi á öllum síðum notanda mun einnig hafa breyta heimildir í viðhengjabirti fyrir merkingar-, blokkunar- og athugasemdaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="11b2f-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="11b2f-265">Hins vegar í tilvikum þar sem tiltekið hlutverk á að hafa breytingarheimildir á síðunni en ekki í viðhengjabirtinum er hægt að nota viðeigandi réttindi úr fyrrgreindum lista til að uppfylla notkunartilvik.</span><span class="sxs-lookup"><span data-stu-id="11b2f-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>

