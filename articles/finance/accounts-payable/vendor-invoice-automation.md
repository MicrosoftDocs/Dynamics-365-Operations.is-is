---
title: Sjálfvirkni reikninga lánardrottins
description: Í þessu efnisatriði er fjallað um aðgerðir sem eru tiltækar fyrir lok við lok sjálfvirkni reikninga lánardrottins, jafnvel reikninga með viðhengi.
author: abruer
manager: AnnBe
ms.date: 05/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4560d7b61fa8f014f9a1185da087df8b1c8e61ba
ms.sourcegitcommit: b7af921189048d9f2eb4d3fd57c704c742bc96e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/23/2020
ms.locfileid: "3396010"
---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="52cf4-103">Sjálfvirkni reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="52cf4-103">Vendor invoice automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52cf4-104">Í þessu efnisatriði er fjallað um aðgerðir sem eru tiltækar fyrir lok við lok sjálfvirkni reikninga lánardrottins, jafnvel reikninga með viðhengi.</span><span class="sxs-lookup"><span data-stu-id="52cf4-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="52cf4-105">Fyrirtæki sem vilja hagræða ferlum Viðskiptaskulda (AP) auðkenna oft reikningsvinnslur sem ein af aðalferlunum sem þurfa að vera skilvirkari.</span><span class="sxs-lookup"><span data-stu-id="52cf4-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="52cf4-106">Í mörgum tilvikum láta þessi fyrirtæki ótengdan þjónustuaðila með ljósskynjun stafa (OCR) um vinnslu reikninga á pappír.</span><span class="sxs-lookup"><span data-stu-id="52cf4-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="52cf4-107">Þeir fá síðan tölvulesanleganleg lýsigögn reiknings ásamt skannaðri mynd af hverjum reikningi.</span><span class="sxs-lookup"><span data-stu-id="52cf4-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="52cf4-108">Til að aðstoða við sjálfvirkni er "síðasta kílómetra" lausn síðan myndað til að auðvelda notkun á þessum hlutum í reikningsfærslukerfinu.</span><span class="sxs-lookup"><span data-stu-id="52cf4-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="52cf4-109">Núna er þessi „síðustu metrunum“ sjálfvirkni virkjuð beint úr kassanum með því að nota lausn sjálfvirkra reikninga.</span><span class="sxs-lookup"><span data-stu-id="52cf4-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="52cf4-110">Lausnasamhengi</span><span class="sxs-lookup"><span data-stu-id="52cf4-110">Solution context</span></span>

<span data-ttu-id="52cf4-111">Reikningur sjálfvirkni lausn virkjar staðlað viðmót sem getur samþykkt reiknings lýsigögn á reikningshausinn og reikningslínur og viðhengjum sem á við um reikninginn.</span><span class="sxs-lookup"><span data-stu-id="52cf4-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="52cf4-112">Öll utanaðkomandi kerfi, sem getur myndað gervinga sem samræmast þessu viðmóti munu geta sent færslurnar inn til sjálfvirkrar vinnslu á reikningum og viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="52cf4-113">Eftirfarandi skýringarmynd sýnir sýnishorn af samþættingaraðstæðum þar sem Contoso hefur gerst meðeigandi með OCR-þjónustuveitanda fyrir vinnslu á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="52cf4-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="52cf4-114">Lánardrottnar Contoso senda reikninga til þjónustuveitu með tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="52cf4-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="52cf4-115">Í gegnum OCR-vinnslu myndar þjónustuveitan lýsigögn reikningsins (haus og/eða línur) og skannaða mynd af reikningnum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="52cf4-116">Samþættingarlag umbreytir þessum gervingum síðan svo að hægt sé að geta nota þær.</span><span class="sxs-lookup"><span data-stu-id="52cf4-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![Dæmi um samþættingaraðstæður](media/vendor_invoice_automation_01.png)

<span data-ttu-id="52cf4-118">Nokkur tilbrigði með fyrrgreint dæmi eru mögulegur ef samþætting reiknings er nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="52cf4-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="52cf4-119">Gagnaflutningur er dæmi um aðra notkun þar sem hægt er að nota þetta viðmót til að stofna reikninga og viðhengi.</span><span class="sxs-lookup"><span data-stu-id="52cf4-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="52cf4-120">Lausnaíhlutir</span><span class="sxs-lookup"><span data-stu-id="52cf4-120">Solution components</span></span>

<span data-ttu-id="52cf4-121">Lausnafótsporið samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="52cf4-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="52cf4-122">Gagnaeiningar fyrir reikningshausinn, línur á reikningi og reikningsviðhengi</span><span class="sxs-lookup"><span data-stu-id="52cf4-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="52cf4-123">Undantekningavinnsla fyrir reikninga</span><span class="sxs-lookup"><span data-stu-id="52cf4-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="52cf4-124">Hlið-við-hlið viðhengjabirtir í reikningum</span><span class="sxs-lookup"><span data-stu-id="52cf4-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="52cf4-125">Afgangurinn af þessu efnisatriði gefur ítarlegar lýsingar á þessum lausnaþáttum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="52cf4-126">Gagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="52cf4-126">Data entities</span></span>

<span data-ttu-id="52cf4-127">Gagnapakki er sú vinnueining sem þarf að senda svo að hægt sé að stofna reikningshausa, reikningslínur og reikningsviðhengi.</span><span class="sxs-lookup"><span data-stu-id="52cf4-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="52cf4-128">Eftirfarandi gagnaeiningar eru notaðar fyrir gervinga sem mynda gögn pakka:</span><span class="sxs-lookup"><span data-stu-id="52cf4-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="52cf4-129">Reikningshaus lánardrottins</span><span class="sxs-lookup"><span data-stu-id="52cf4-129">Vendor invoice header</span></span>
+ <span data-ttu-id="52cf4-130">Reikningslína lánardrottins</span><span class="sxs-lookup"><span data-stu-id="52cf4-130">Vendor invoice line</span></span>
+ <span data-ttu-id="52cf4-131">Viðhengi reikningsskjals lánardrottins</span><span class="sxs-lookup"><span data-stu-id="52cf4-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="52cf4-132">Skjalaviðhengi lánardrottnareikningsins er ný gagnaeining sem er kynnt sem hluti af þessari aðgerð.</span><span class="sxs-lookup"><span data-stu-id="52cf4-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="52cf4-133">Hauseining lánardrottnareiknings hefur verið breytt þannig að hann styður viðhengi.</span><span class="sxs-lookup"><span data-stu-id="52cf4-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="52cf4-134">Línueining lánardrottnareiknings hefur ekki verið breytt fyrir þetta sérkenni.</span><span class="sxs-lookup"><span data-stu-id="52cf4-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="52cf4-135">Ítarlegar upplýsingar um gagnapakka er að finna í [Yfirlit gagnastjórnunar](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="52cf4-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="52cf4-136">Frekari upplýsingar um hvernig á að búa til gagnapakka með vinnusvæði gagnastjórnunar er að finna í [Meðhöndla og nota gagnapakka í Dynamics 365 Finance and Operations forritslausn](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="52cf4-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="52cf4-137">Fylgið eftirfarandi skrefum til að mynda prófun gagna sem inniheldur reikninga og viðhengja.</span><span class="sxs-lookup"><span data-stu-id="52cf4-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="52cf4-138">Skráðu þig inn á tilvikið.</span><span class="sxs-lookup"><span data-stu-id="52cf4-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="52cf4-139">Fara í **Viðskiptaskuldir** > **Reikningar** > **Opna lánardrottnareikninga**.</span><span class="sxs-lookup"><span data-stu-id="52cf4-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="52cf4-140">Stofna reikninga sem hafa línur og viðhengi.</span><span class="sxs-lookup"><span data-stu-id="52cf4-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52cf4-141">Viðhengin verða að vera viðhengi við haus.</span><span class="sxs-lookup"><span data-stu-id="52cf4-141">The attachments must be header attachments.</span></span> <span data-ttu-id="52cf4-142">Sem stendur styður skjalaviðhengjaeining lánardrottnareiknings ekki viðhengi við línur.</span><span class="sxs-lookup"><span data-stu-id="52cf4-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="52cf4-143">Opnaðu vinnusvæðið **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="52cf4-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="52cf4-144">Stofna útflutningsvinnslu sem inniheldur reikningshaus lánardrottins, reikningslínu lánardrottins og skjalaviðhengiseiningu lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="52cf4-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="52cf4-145">Flyttu út gögnin.</span><span class="sxs-lookup"><span data-stu-id="52cf4-145">Export the data.</span></span>
1. <span data-ttu-id="52cf4-146">Sæktu útflutt gögnin sem pakka.</span><span class="sxs-lookup"><span data-stu-id="52cf4-146">Download the exported data as a package.</span></span> <span data-ttu-id="52cf4-147">Nú má nota pakkanum til að flytja gögn inn í marktilvik til prófunar.</span><span class="sxs-lookup"><span data-stu-id="52cf4-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="52cf4-148">Ákvörðun lögaðila fyrir reikning</span><span class="sxs-lookup"><span data-stu-id="52cf4-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="52cf4-149">Reikningar sem eru innfluttir með gagnapakka er hægt að tengja lögaðila sem þeir tilheyra á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="52cf4-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="52cf4-150">Innflutningsvinnslan sem vinnur reikninginn flytur hann inn í sama fyrirtækið sem þar vinnslan var í röðun á vinnusvæðinu **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="52cf4-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="52cf4-151">Með öðrum orðum ákvarðar fyrirtæki vinnslunnar fyrirtækið sem reikningurinn tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="52cf4-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="52cf4-152">Þegar gagnapakki sem inniheldur reikninga er sendur til Finance, getur hringjandi (þ.e.a.s. samþættingarforritið sem keyrir utan Finance) nefnt kenni fyrirtækisins skýrt í HTTP-beiðninni.</span><span class="sxs-lookup"><span data-stu-id="52cf4-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="52cf4-153">Í þessu tilfelli er fyrirtækjasamhenginu sem keyrir vinnsluna í Finance hnekkt og reikningarnir eru fluttir inn í fyrirtækið sem var beint í gegnum svar HTTP.</span><span class="sxs-lookup"><span data-stu-id="52cf4-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="52cf4-154">Þessi hegðun er stöðluð gagnastjórnunarhegðun.</span><span class="sxs-lookup"><span data-stu-id="52cf4-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="52cf4-155">Það er útskýrt hér, í samhengi við reikninga, fyrir sakir heildarinnar.</span><span class="sxs-lookup"><span data-stu-id="52cf4-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="52cf4-156">Undantekningavinnsla</span><span class="sxs-lookup"><span data-stu-id="52cf4-156">Exception processing</span></span>

<span data-ttu-id="52cf4-157">Í aðstæðum þar sem lánardrottinsreikningar koma inn Finance and Operations með samþættingu þarf að vera til staðar auðveld leið fyrir meðlimi viðskiptaskulda til að vinna úr undantekningum eða reikninga sem ekki eru samþykktir og stofna reikninga í bið út frá reikningum sem mistókst.</span><span class="sxs-lookup"><span data-stu-id="52cf4-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="52cf4-158">Þessi frábrigðavinnsla fyrir reikninga lánardrottins er nú hluti af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="52cf4-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="52cf4-159">Listasíða undantekninga</span><span class="sxs-lookup"><span data-stu-id="52cf4-159">Exceptions list page</span></span>

<span data-ttu-id="52cf4-160">Nýja listasíðan fyrir reikningsundantekningar er alltaf tiltæk í **Viðskiptaskuldum** > **Reikningum** > **Flytja verkefnismistök** > **reikningar Lánardrottins sem hefur mistekist að flytja**.</span><span class="sxs-lookup"><span data-stu-id="52cf4-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="52cf4-161">Þessi síða sýnir allar hausfærslur lánardrottnareiknings úr sviðsetningartöflunni í gagnaeiningu hauss lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="52cf4-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="52cf4-162">Athugið að hægt er að skoða sömu skrár á vinnusvæðinu **Gagnastjórnun** þar sem er einnig hægt að framkvæma sömu aðgerðir sem eru gefnar í undantekningunni meðhöndlun aðgerð.</span><span class="sxs-lookup"><span data-stu-id="52cf4-162">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="52cf4-163">Hins vegar UI sem undantekningin meðhöndlunaraðgerð veitir bestuð fyrir virkan notanda.</span><span class="sxs-lookup"><span data-stu-id="52cf4-163">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Listasíða undantekninga](media/vendor_invoice_automation_02.png)

<span data-ttu-id="52cf4-165">Þessi listasíða felur í sér eftirtalin svæði sem berast inn í gegnum streymi:</span><span class="sxs-lookup"><span data-stu-id="52cf4-165">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="52cf4-166">**Fyrirtæki** – Það fyrirtæki sem reikningurinn tilheyrir</span><span class="sxs-lookup"><span data-stu-id="52cf4-166">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="52cf4-167">**Villuboð** – Villuboðin sem ramminn stjórnun gagna úthreyfingar til að útskýra af hverju ekki var hægt að stofna reikning</span><span class="sxs-lookup"><span data-stu-id="52cf4-167">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="52cf4-168">**Númer** – Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="52cf4-168">**Number** – The invoice number</span></span>
+ <span data-ttu-id="52cf4-169">**Reikningslykill**</span><span class="sxs-lookup"><span data-stu-id="52cf4-169">**Invoice account**</span></span>
+ <span data-ttu-id="52cf4-170">**Nafn** – Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="52cf4-170">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="52cf4-171">**Lykill lánardrottins**</span><span class="sxs-lookup"><span data-stu-id="52cf4-171">**Vendor account**</span></span>
+ <span data-ttu-id="52cf4-172">**Innkaupapöntun** – Númer innkaupapöntunar fyrir reikninginn</span><span class="sxs-lookup"><span data-stu-id="52cf4-172">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="52cf4-173">**Bókunardagsetning**</span><span class="sxs-lookup"><span data-stu-id="52cf4-173">**Posting date**</span></span>
+ <span data-ttu-id="52cf4-174">**Reikningsdagsetning**</span><span class="sxs-lookup"><span data-stu-id="52cf4-174">**Invoice date**</span></span>
+ <span data-ttu-id="52cf4-175">**Lýsing reiknings**</span><span class="sxs-lookup"><span data-stu-id="52cf4-175">**Invoice description**</span></span>
+ <span data-ttu-id="52cf4-176">**Gjaldmiðill**</span><span class="sxs-lookup"><span data-stu-id="52cf4-176">**Currency**</span></span>
+ <span data-ttu-id="52cf4-177">**Kladdi**</span><span class="sxs-lookup"><span data-stu-id="52cf4-177">**Log**</span></span>
+ <span data-ttu-id="52cf4-178">**Línutilvísun** – Kennið sem er fengið frá utanaðkomandi kerfi</span><span class="sxs-lookup"><span data-stu-id="52cf4-178">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="52cf4-179">Línutilvísun er ekki reikningskenni.</span><span class="sxs-lookup"><span data-stu-id="52cf4-179">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="52cf4-180">Þessi listasíða hefur einnig forskoðunarrúðu sem þú getur notað á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="52cf4-180">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="52cf4-181">Skoða öll villuboðin svo að ekki þurfi að útvíkka dálkinn **Villuboð** í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="52cf4-181">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="52cf4-182">Skoða allan listann yfir viðhengi fyrir reikninginn, ef einhver viðhengi fylgdu með reikningnum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-182">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="52cf4-183">Listasíðan styður eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="52cf4-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="52cf4-184">**Breyta** – Opna undantekningarfærsluna í breytingarham, þannig að hægt sé að laga vandamálin.</span><span class="sxs-lookup"><span data-stu-id="52cf4-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="52cf4-185">**Valkostir** – Farðu í staðlaða valkostina sem eru tiltækir á listasíðunum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="52cf4-186">Hægt er að nota valkostinn **Bæta við vinnusvæði** til að festa listasíðu undantekninga á vinnusvæðið sem lista eða reit.</span><span class="sxs-lookup"><span data-stu-id="52cf4-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="52cf4-187">Upplýsingasíða undantekninga</span><span class="sxs-lookup"><span data-stu-id="52cf4-187">Exception details page</span></span>

<span data-ttu-id="52cf4-188">Þegar breytingastillingar eru opnaðar birtis upplýsingasíða fyrir reikninginn sem er með vandamál.</span><span class="sxs-lookup"><span data-stu-id="52cf4-188">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="52cf4-189">Ef einhver viðhengi eru til staðar birtast reikningurinn og sjálfgefna viðhengið hlið við hlið á upplýsingasíðu um undantekningar.</span><span class="sxs-lookup"><span data-stu-id="52cf4-189">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Upplýsingasíða undantekninga](media/vendor_invoice_automation_03.png)

<span data-ttu-id="52cf4-191">Á fyrrigreindi mynd voru engar línur fyrir reikningshaus lánardrottins sem kom inn.</span><span class="sxs-lookup"><span data-stu-id="52cf4-191">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="52cf4-192">Þess vegna er línuhlutinn í kaflanum auður.</span><span class="sxs-lookup"><span data-stu-id="52cf4-192">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="52cf4-193">Upplýsingasíða um undantekningar styður eftirfarandi aðgerð:</span><span class="sxs-lookup"><span data-stu-id="52cf4-193">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="52cf4-194">**Stofna reikning í bið** – Þegar vandamál á reikningnum hafa verið löguð sem hluti af undantekningavinnslu, er hægt að smella á þennan hnapp til að stofna reikning í bið.</span><span class="sxs-lookup"><span data-stu-id="52cf4-194">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="52cf4-195">Stofnun reikninga fer fram í bakgrunni (eins og ósamstillt aðgerð).</span><span class="sxs-lookup"><span data-stu-id="52cf4-195">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="52cf4-196">Samnýtt þjónusta samanb. v. fyrirtækjabyggða undantekningavinnslu</span><span class="sxs-lookup"><span data-stu-id="52cf4-196">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="52cf4-197">Listasíða undantekninga styður staðlaða öryggisbyggingu sem vinnusvæðið **Gagnastjórnun** styður fyrir vinnslu á stigaðgerðir færslur.</span><span class="sxs-lookup"><span data-stu-id="52cf4-197">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="52cf4-198">Hægt er að tryggja innflutningsvinnslu reiknings á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="52cf4-198">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="52cf4-199">Eftir notandahlutverki</span><span class="sxs-lookup"><span data-stu-id="52cf4-199">By user role</span></span>
+ <span data-ttu-id="52cf4-200">Eftir notanda</span><span class="sxs-lookup"><span data-stu-id="52cf4-200">By user</span></span>
+ <span data-ttu-id="52cf4-201">Eftir lögaðila</span><span class="sxs-lookup"><span data-stu-id="52cf4-201">By legal entity</span></span>

![Innflutningsvinnsla sem er tryggð eftir hlutverki notanda og lögaðila](media/vendor_invoice_automation_04.png)

<span data-ttu-id="52cf4-203">Ef öryggi er skilgreint fyrir innflutningsvinnslu reiknings virðir listasíða undantekninga þessar stillingar.</span><span class="sxs-lookup"><span data-stu-id="52cf4-203">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="52cf4-204">Notendur geta aðeins séð undantekningafærslur reikninga sem þessi uppsetning leyfir þeim að sjá.</span><span class="sxs-lookup"><span data-stu-id="52cf4-204">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="52cf4-205">Til dæmis hefur Contoso ákveðið að keyra reikningsundantekningar eftir lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-205">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="52cf4-206">Þar af leiðandi er öryggi skilgreint í innflutningsvinnslu reikninga á þann hátt að notandi í lögaðila A getur aðeins séð undantekningar reikninga í lögaðila A, en notandi í lögaðila B getur aðeins séð undantekningar reikninga í lögaðila B. Þessi uppsetning virkjar aðskilnað á skyldum fyrir stjórnun á undantekningum reikninga.</span><span class="sxs-lookup"><span data-stu-id="52cf4-206">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="52cf4-207">Contoso gæti einnig ákveðið að tryggja ekki neitt öryggi, þannig að notendur geti keyrt undantekningar reikninga fyrir allar einingar lögaðila.</span><span class="sxs-lookup"><span data-stu-id="52cf4-207">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="52cf4-208">Þessi uppsetning virkjar samnýtta þjónustuaðstæður fyrir stjórnun á undantekningum reikninga.</span><span class="sxs-lookup"><span data-stu-id="52cf4-208">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="52cf4-209">Hlið-við-hlið viðhengjabirtir</span><span class="sxs-lookup"><span data-stu-id="52cf4-209">Side-by-side attachment viewer</span></span>

<span data-ttu-id="52cf4-210">Til að aðstoða við að skoða viðhengi fyrir reikninga lánardrottins, veita eftirfarandi síður sem eru notaðar í reikningsfærslunni núna viðhengjabirti:</span><span class="sxs-lookup"><span data-stu-id="52cf4-210">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="52cf4-211">**Meðhöndlun undantekninga**</span><span class="sxs-lookup"><span data-stu-id="52cf4-211">**Exception handling**</span></span>
+ <span data-ttu-id="52cf4-212">Síðan **Lánardrottnareikningar í bið** (einnig tiltæk i endurskoðunarferli reikninga)</span><span class="sxs-lookup"><span data-stu-id="52cf4-212">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="52cf4-213">Fyrirspurnasíða **Reikningabók** (fyrir bókaða reikninga)</span><span class="sxs-lookup"><span data-stu-id="52cf4-213">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="52cf4-214">Hér eru aðalaðgerðir sem viðhengjabirtirinn veitir:</span><span class="sxs-lookup"><span data-stu-id="52cf4-214">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="52cf4-215">Skoðið allar viðhengjagerðir sem skjalastjórnun styður (skrár myndir, Vefföng og athugasemdir).</span><span class="sxs-lookup"><span data-stu-id="52cf4-215">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="52cf4-216">Skoða TIFF-skrár með mörgum síðum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-216">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="52cf4-217">Framkvæmið eftirfarandi aðgerðir í myndaskrám:</span><span class="sxs-lookup"><span data-stu-id="52cf4-217">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="52cf4-218">Merkið hluta myndarinnar.</span><span class="sxs-lookup"><span data-stu-id="52cf4-218">Highlight parts of the image.</span></span>
  + <span data-ttu-id="52cf4-219">Felur hluta myndarinnar.</span><span class="sxs-lookup"><span data-stu-id="52cf4-219">Block parts of the image.</span></span>
  + <span data-ttu-id="52cf4-220">Bæta athugasemdum við myndina.</span><span class="sxs-lookup"><span data-stu-id="52cf4-220">Add annotations to the image.</span></span>
  + <span data-ttu-id="52cf4-221">Þysjar inn og út á myndina.</span><span class="sxs-lookup"><span data-stu-id="52cf4-221">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="52cf4-222">Víðmynd myndarinnar.</span><span class="sxs-lookup"><span data-stu-id="52cf4-222">Pan the image.</span></span>
  + <span data-ttu-id="52cf4-223">Afturkalla og endurgera aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="52cf4-223">Undo and redo actions.</span></span>
  + <span data-ttu-id="52cf4-224">Breyttu myndarinni svo að hún passi.</span><span class="sxs-lookup"><span data-stu-id="52cf4-224">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="52cf4-225">Þessar aðgerðir eru tiltækar fyrir myndskrár (JPEG, TIFF, PNG og svo framvegis).</span><span class="sxs-lookup"><span data-stu-id="52cf4-225">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="52cf4-226">Allar breytingar sem gerðar eru á mynd með því að nota þessar aðgerðir eru vistaðar í myndskrá.</span><span class="sxs-lookup"><span data-stu-id="52cf4-226">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="52cf4-227">Eins og stendur felur viðhengjabirtir ekki í sér útgáfu- eða endurskoðunargetu.</span><span class="sxs-lookup"><span data-stu-id="52cf4-227">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="52cf4-228">Sjálfgefið viðhengi</span><span class="sxs-lookup"><span data-stu-id="52cf4-228">Default attachment</span></span>

<span data-ttu-id="52cf4-229">Ef reikningur lánardrottins hefur fleiri en eitt viðhengi er hægt að stilla eitt af skjölunum sem sjálfgefið viðhengi á síðunni **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="52cf4-229">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="52cf4-230">Valkosturinn **Er sjálfgefið viðhengi** er nýr valkostur sem var bætt við sem hluta af þessum aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-230">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="52cf4-231">Þessi valkostur er líka sýndur í gagnaeiningu skjalaviðhengis lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="52cf4-231">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="52cf4-232">Þess vegna er hægt að stilla sjálfgefið viðhengi í gegnum samþættingar.</span><span class="sxs-lookup"><span data-stu-id="52cf4-232">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="52cf4-233">Aðeins er hægt að stilla eitt skjal sem sjálfgefið viðhengi.</span><span class="sxs-lookup"><span data-stu-id="52cf4-233">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="52cf4-234">Eftir að skjal er stillt sem sjálfgefið viðhengi er það sjálfkrafa sýnt í viðhengjabirti þegar reikningurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="52cf4-234">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="52cf4-235">Ef ekkert skjal er stillt sem sjálfgefið viðhengi sýnir birtirinn ekki sjálfkrafa nein viðhengi þegar reikningurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="52cf4-235">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="52cf4-236">Sýna/fela reikningsviðhengi</span><span class="sxs-lookup"><span data-stu-id="52cf4-236">Show/hide invoice attachments</span></span>

<span data-ttu-id="52cf4-237">Ný hnappur sem er tiltækur á fyrirspurnasíðunum **Undantekningar vinnslu**, **Reikningur í bið** og **Reikningabók** gerir kleift að sýna eða fela viðhengjabirtinn.</span><span class="sxs-lookup"><span data-stu-id="52cf4-237">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="52cf4-238">Öryggi</span><span class="sxs-lookup"><span data-stu-id="52cf4-238">Security</span></span>

<span data-ttu-id="52cf4-239">Eftirfarandi aðgerðum í viðhengjabirti er stjórnað með öryggi eftir hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="52cf4-239">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="52cf4-240">Auðkennt</span><span class="sxs-lookup"><span data-stu-id="52cf4-240">Highlighting</span></span>
+ <span data-ttu-id="52cf4-241">Varið</span><span class="sxs-lookup"><span data-stu-id="52cf4-241">Block</span></span>
+ <span data-ttu-id="52cf4-242">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="52cf4-242">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="52cf4-243">Síðan Lánardrottnareikningar í bið</span><span class="sxs-lookup"><span data-stu-id="52cf4-243">Pending vendor invoices page</span></span>

<span data-ttu-id="52cf4-244">Eftirfarandi réttindi veita aðgang tilbúna-aðeins eða les/skrif aðgang að viðhengjabirti fyrir því að merkingar-, blokkunar- og ahtugasemdaaðgerðir:</span><span class="sxs-lookup"><span data-stu-id="52cf4-244">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="52cf4-245">**Viðhalda mynd lánardrottnareiknings** – Þessi réttindi veta les/skrif aðgang.</span><span class="sxs-lookup"><span data-stu-id="52cf4-245">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="52cf4-246">**Skoða mynd lánardrottnareiknings** – Þessi réttindi veta lesaðgang.</span><span class="sxs-lookup"><span data-stu-id="52cf4-246">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="52cf4-247">Eftirfarandi skyldur veita aðeins lesaðgang eða les/skrif aðgang að viðhengjabirti fyrir þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="52cf4-247">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="52cf4-248">**Viðhalda lánardrottnareikningum** – Myndaréttindin Viðhalda lánardrottnareikningi eru tengd þessum skyldum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-248">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="52cf4-249">**Gera fyrirspurn um reikningsstöðu lánardrottins** – Myndaréttindin Skoða lánardrottnareikningi eru tengd þessum skyldum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-249">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="52cf4-250">Eftirfarandi hlutverk veita aðeins lesaðgang eða les/skrif aðgang að viðhengjabirti fyrir þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="52cf4-250">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="52cf4-251">**Afgreiðslumaður viðskiptaskulda** og **Stjórnandi viðskiptaskulda** – Skyldan Viðhalda lánardrottnareikningum er úthlutað á þessum hlutverk.</span><span class="sxs-lookup"><span data-stu-id="52cf4-251">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="52cf4-252">**Afgreiðslumaður lánardrottna**, **stjórnanda lánardrottna**, **Lykla lánardrottna miðstýrðar greiðslur afgreiðslumaður**, og **Lykla lánardrottna greiðslur afgreiðslumaður** – í Spyrjast fyrir um lánardrottinn reikningi stöðuna gjald er úthlutað á þessum hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-252">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="52cf4-253">Upplýsingasíða reikningsundantekninga</span><span class="sxs-lookup"><span data-stu-id="52cf4-253">Invoice exception details page</span></span>

<span data-ttu-id="52cf4-254">Eftirfarandi réttindi veita aðgang tilbúna-aðeins eða les/skrif aðgang að viðhengjabirti fyrir því að merkingar-, blokkunar- og ahtugasemdaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="52cf4-254">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="52cf4-255">Hlutverk sem eru nefnd í þessum hluta veita aðeins til lestrar aðgang að myndir reikning í viðhengjabirti utan í reitinn.</span><span class="sxs-lookup"><span data-stu-id="52cf4-255">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="52cf4-256">Ef hlutverk verður einnig að hafa skrifaðgang að myndunum, má veita skrifaðgang að því hlutverki með heimildinni og gjald sem er lýst hér.</span><span class="sxs-lookup"><span data-stu-id="52cf4-256">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="52cf4-257">**Viðhalda lánardrottni reikningsins haus einingar mynd** – Þessa heimildinni veitir les/skrif aðgang að reikningur myndirnar í viðhengjabirti.</span><span class="sxs-lookup"><span data-stu-id="52cf4-257">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="52cf4-258">**Skoða lánardrottni reikningsins haus einingar mynd** – Þessa heimildinni veitir les aðgang að reikningsmyndinni í viðhengjabirti.</span><span class="sxs-lookup"><span data-stu-id="52cf4-258">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="52cf4-259">Eftirfarandi skyldur veita aðeins lesaðgang að viðhengjabirti fyrir þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="52cf4-259">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="52cf4-260">**Viðhalda lánardrottnareikningum** – Myndaréttindin Viðhalda hauseiningu lánardrottnareiknings eru tengd þessum skyldum.</span><span class="sxs-lookup"><span data-stu-id="52cf4-260">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="52cf4-261">Eftirfarandi hlutverk veita aðeins lesaðgang að viðhengjabirti fyrir þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="52cf4-261">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="52cf4-262">**Afgreiðslumaður viðskiptaskulda** og **Stjórnandi viðskiptaskulda** – Skyldan Viðhalda lánardrottnareikningum er úthlutað á þessum hlutverk.</span><span class="sxs-lookup"><span data-stu-id="52cf4-262">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="52cf4-263">Sjálfgefið ef hlutverki notanda veitir breyta réttindi á öllum síðum notanda mun einnig hafa breyta heimildir í viðhengjabirti fyrir merkingar-, blokkunar- og athugasemdaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="52cf4-263">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="52cf4-264">Hins vegar í tilvikum þar sem tiltekið hlutverk á að hafa breytingarheimildir á síðunni en ekki í viðhengjabirtinum er hægt að nota viðeigandi réttindi úr fyrrgreindum lista til að uppfylla notkunartilvik.</span><span class="sxs-lookup"><span data-stu-id="52cf4-264">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
