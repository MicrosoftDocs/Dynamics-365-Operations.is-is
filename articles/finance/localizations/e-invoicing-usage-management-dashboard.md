---
title: Stjórnborð notkunarstjórnunar
description: Í þessu efnisatriði er útskýrt hvernig nota á stjórnborð notkunar til að fylgjast með notkun rafrænu reikningsfærsluþjónustunnar og uppfylla reglur.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130507"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="11156-103">Stjórnborð notkunarstjórnunar</span><span class="sxs-lookup"><span data-stu-id="11156-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11156-104">Stjórnborðið **Notkunarstjórnun** hjálpar til við að fylgjast með notkun rafrænnar reikningsfærsluþjónustu og hjálpar því fyrirtækinu þínu að halda sig við mánaðarlega notkun.</span><span class="sxs-lookup"><span data-stu-id="11156-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="11156-105">Reglufylgni ákvarðast með því að reikna út magn innsendingar og bera það saman við fengið magn innsendingar til að greina frávik milli fengins magns og notaðs magns.</span><span class="sxs-lookup"><span data-stu-id="11156-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="11156-106">Stjórnborðið inniheldur eftirfarandi vísa:</span><span class="sxs-lookup"><span data-stu-id="11156-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="11156-107">Einn kostnaðarvísi sem hægt er að nota til að fylgjast með notkun vegna reglufylgni við leyfisveitingar:</span><span class="sxs-lookup"><span data-stu-id="11156-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="11156-108">Notkun á mánuði (útflutningur)</span><span class="sxs-lookup"><span data-stu-id="11156-108">Usage per month (export)</span></span>

- <span data-ttu-id="11156-109">Þrír rekstrarvísar sem hægt er að nota til að fylgjast með notkun rafrænnar reikningsfærsluþjónustu í stjórnunarskyni:</span><span class="sxs-lookup"><span data-stu-id="11156-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="11156-110">Notkun eftir eiginleika</span><span class="sxs-lookup"><span data-stu-id="11156-110">Usage by feature</span></span>
    - <span data-ttu-id="11156-111">Notkun eftir umhverfi</span><span class="sxs-lookup"><span data-stu-id="11156-111">Usage by environment</span></span>
    - <span data-ttu-id="11156-112">Notkun á mánuði (innflutningur)</span><span class="sxs-lookup"><span data-stu-id="11156-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="11156-113">Umfang mælinga</span><span class="sxs-lookup"><span data-stu-id="11156-113">Measurement scope</span></span>

- <span data-ttu-id="11156-114">Mælieining:</span><span class="sxs-lookup"><span data-stu-id="11156-114">Unit of measure:</span></span> 

    <span data-ttu-id="11156-115">Stjórnborð **Notkunarstjórnunar** telur innsendingu á viðskiptaskjölum og innfluttum rafrænum reikningum.</span><span class="sxs-lookup"><span data-stu-id="11156-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="11156-116">Fyrirtæki:</span><span class="sxs-lookup"><span data-stu-id="11156-116">Organization:</span></span> 

    <span data-ttu-id="11156-117">Talning er tekin saman með auðkenni leigjanda fyrir fyrirtækið, burtséð frá fjölda tilvika Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management, eða fjölda lögaðila þar sem rafræn reikningsfærsluþjónusta er virk.</span><span class="sxs-lookup"><span data-stu-id="11156-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="11156-118">Vísir: Notkun á mánuði (útflutningur)</span><span class="sxs-lookup"><span data-stu-id="11156-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="11156-119">Þessi vísir veitir upplýsingar um rafræna reikninga sem fyrirtækið gefur út á skilgreindu tímabili.</span><span class="sxs-lookup"><span data-stu-id="11156-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="11156-120">Gildissvið</span><span class="sxs-lookup"><span data-stu-id="11156-120">Scope</span></span>
- <span data-ttu-id="11156-121">Fjöldi viðskiptaskjala sem eru send frá Finance og Supply Chain Management til rafrænu reikningsfærsluþjónustunnar, óháð fjölda lína sem þessi viðskiptaskjöl innihalda.</span><span class="sxs-lookup"><span data-stu-id="11156-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="11156-122">Fjöldi innsendra viðskiptaskjala sem rafræna reikningsfærsluþjónustan hefur unnið úr.</span><span class="sxs-lookup"><span data-stu-id="11156-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="11156-123">Skjal telst hafa verið unnið þegar flæði aðgerða sem eru skilgreindar í uppsetningu eiginleika er lokið.</span><span class="sxs-lookup"><span data-stu-id="11156-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="11156-124">Þegar rafrænn reikningur er sendur á utanaðkomandi vefþjónustu er talning óháð niðurstöðum úr vinnslu vefþjónustu (samþykkt, hafnað eða villa skemaprófunar).</span><span class="sxs-lookup"><span data-stu-id="11156-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="11156-125">Ef vefþjónustunni barst beiðni frá rafrænni reikningsfærsluþjónustu og svaraði henni telst innsendingin gild talning.</span><span class="sxs-lookup"><span data-stu-id="11156-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="11156-126">**Undantekning:** Viðskiptaskjöl eru ekki talin ef þau eru send aftur frá Finance og Supply Chain Management til rafrænnar reikningsfærsluþjónustu eins og í þeim tilvikum þar sem endursending á sama viðskiptaskjalinu er nauðsynleg til að breyta stöðu rafræna reikningsins.</span><span class="sxs-lookup"><span data-stu-id="11156-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="11156-127">Útgáfa á brasilískum rafrænum reikningi (fjárhagsskjali) telst til dæmis gild en beiðni um afturköllun hans er ekki talin.</span><span class="sxs-lookup"><span data-stu-id="11156-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="11156-128">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="11156-128">Calculation</span></span>

<span data-ttu-id="11156-129">Útreikningur á stöðunni er reiknaður á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="11156-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="11156-130">Staða = Laust + keypt – notað</span><span class="sxs-lookup"><span data-stu-id="11156-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="11156-131">Hvar:</span><span class="sxs-lookup"><span data-stu-id="11156-131">Where:</span></span>

- <span data-ttu-id="11156-132">Laust:</span><span class="sxs-lookup"><span data-stu-id="11156-132">Free:</span></span>
  
    <span data-ttu-id="11156-133">Ókeypis magn viðskiptaskjala sem viðskiptavinurinn getur sent inn á mánuði.</span><span class="sxs-lookup"><span data-stu-id="11156-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="11156-134">Það inniheldur pakka með 100 viðskiptaskjölum sem hægt er að senda til rafrænu reikningsfærsluþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="11156-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="11156-135">Ókeypis magn safnast ekki upp og eftirstöðvar eru ekki færðar yfir á næsta tímabil.</span><span class="sxs-lookup"><span data-stu-id="11156-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="11156-136">Innkeypt:</span><span class="sxs-lookup"><span data-stu-id="11156-136">Purchased:</span></span>
  
    <span data-ttu-id="11156-137">Pakki með 1000 viðskiptaskjölum sem hægt er að senda til rafrænu reikningsfærsluþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="11156-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="11156-138">Þennan pakka þarf að útvega mánaðarlega fyrir fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="11156-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="11156-139">Keypt magn safnast ekki upp og eftirstöðvar eru ekki færðar yfir á næsta tímabil.</span><span class="sxs-lookup"><span data-stu-id="11156-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="11156-140">Notað:</span><span class="sxs-lookup"><span data-stu-id="11156-140">Used:</span></span> 

    <span data-ttu-id="11156-141">Talning á innsendum viðskiptaskjölum til rafrænnar reikningsfærsluþjónustu samkvæmt skilgreindu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="11156-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="11156-142">Ef fyrirtækið áformar að fara yfir mánaðarlegt magn 100 ókeypis innsendinga skaltu kaupa hámarksmagn til að tryggja að þú fylgir reglum um leyfisveitingar Microsoft fyrir rafræna reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="11156-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="11156-143">Sem stendur þarf að slá inn keypt magn handvirkt samkvæmt innkaupadagsetningunni sem margar pakkningar með 1000 innsendingum.</span><span class="sxs-lookup"><span data-stu-id="11156-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="11156-144">Vísir: Notkun eftir eiginleika</span><span class="sxs-lookup"><span data-stu-id="11156-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="11156-145">Þessi vísir sýnir notkun rafrænna reikningsfærslueiginleika fyrir útgáfu rafrænna reikninga á skilgreindu tímabili.</span><span class="sxs-lookup"><span data-stu-id="11156-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="11156-146">Útreikningur:</span><span class="sxs-lookup"><span data-stu-id="11156-146">Calculation:</span></span>
  
    <span data-ttu-id="11156-147">Notað = Talning á hversu oft hver rafrænn reikningsfærslueiginleiki var notaður við innsendingu viðskiptaskjala til rafrænnar reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="11156-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="11156-148">Vísir: Notkun eftir umhverfi</span><span class="sxs-lookup"><span data-stu-id="11156-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="11156-149">Þessi vísir sýnir notkun á umhverfum rafrænna reikningsfærsluþjónustu á skilgreindu tímabili.</span><span class="sxs-lookup"><span data-stu-id="11156-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="11156-150">Útreikningur:</span><span class="sxs-lookup"><span data-stu-id="11156-150">Calculation:</span></span>
    
    <span data-ttu-id="11156-151">Notað = Talning á hversu oft hver rafræn reikningsfærsluþjónusta var notað við innsendingu viðskiptaskjala til rafrænnar reikningsfærsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="11156-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="11156-152">Vísir: Notkun á mánuði (innflutningur)</span><span class="sxs-lookup"><span data-stu-id="11156-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="11156-153">Þessi vísir sýnir magn á innflutningi rafrænna reikninga af hendi rafrænnar reikningsfærsluþjónustu til Finance og Supply Chain Management á skilgreindu tímabili.</span><span class="sxs-lookup"><span data-stu-id="11156-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="11156-154">Umfang:</span><span class="sxs-lookup"><span data-stu-id="11156-154">Scope:</span></span>

    <span data-ttu-id="11156-155">Rafrænir reikningar sem eru fluttir inn í Finance og Supply Chain Management, burtséð frá fjölda lína sem þessir rafrænu reikningar innihalda.</span><span class="sxs-lookup"><span data-stu-id="11156-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="11156-156">Útreikningur:</span><span class="sxs-lookup"><span data-stu-id="11156-156">Calculation:</span></span>

    <span data-ttu-id="11156-157">Móttekið = Talning á rafrænum reikningum sem eru fluttir inn í Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="11156-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="11156-158">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="11156-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="11156-159">Innkaup</span><span class="sxs-lookup"><span data-stu-id="11156-159">Purchase</span></span>

<span data-ttu-id="11156-160">Í flipanum **Notkun á mánuði (útflutningur)** skal velja **Kaup** til að skrá handvirkt magn fenginna innsendinga.</span><span class="sxs-lookup"><span data-stu-id="11156-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="11156-161">Fyrir ákveðna dagsetningu er valið **Nýtt** og færður inn fjöldi **Pakkninga** sem fengnar voru fyrir þann dag.</span><span class="sxs-lookup"><span data-stu-id="11156-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="11156-162">**Magnið** er reiknað svona:</span><span class="sxs-lookup"><span data-stu-id="11156-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="11156-163">Magn = Pakkningar \* 1.000</span><span class="sxs-lookup"><span data-stu-id="11156-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="11156-164">Reiknað **Magn** kemur fram í **Keypt** í vísinum **Notkun á mánuði (útflutningur)**.</span><span class="sxs-lookup"><span data-stu-id="11156-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="11156-165">Update</span><span class="sxs-lookup"><span data-stu-id="11156-165">Update</span></span>

<span data-ttu-id="11156-166">Smellið á **Uppfæra** á aðgerðasvæðinu til að uppfæra útreikninginn og uppfæra gögnin sem sýnd eru á síðunni og í grafinu.</span><span class="sxs-lookup"><span data-stu-id="11156-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="11156-167">Hreinsa ferilsgögn</span><span class="sxs-lookup"><span data-stu-id="11156-167">Reset history data</span></span>

<span data-ttu-id="11156-168">Veljið **Endurstilla ferilsgögn** á aðgerðasvæðinu til að uppfæra gagnagrunninn þar sem vísarnir eru reiknaðir.</span><span class="sxs-lookup"><span data-stu-id="11156-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="11156-169">Stjórnborðið **Notkunarstjórnun** sýnir ekki peningaupphæðir.</span><span class="sxs-lookup"><span data-stu-id="11156-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="11156-170">Í staðinn sýnir það aðeins magn taldra innsendinga og innfluttra skjala.</span><span class="sxs-lookup"><span data-stu-id="11156-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
