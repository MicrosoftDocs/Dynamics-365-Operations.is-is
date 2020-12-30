---
title: Afstemming farms í flutningsstjórnun
description: Þetta efni útskýrir ferli afstemmingar farms.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable,TMSFBDetailReconcile,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13fecd5256c7bfc3a27d15482e0fa6200cfd72df
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4430801"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="59c91-103">Afstemming farms í flutningsstjórnun</span><span class="sxs-lookup"><span data-stu-id="59c91-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59c91-104">Þetta efni útskýrir ferli afstemmingar farms.</span><span class="sxs-lookup"><span data-stu-id="59c91-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="59c91-105">Afstemming farms hægt að gera handvirkt eða hægt er að setja hann upp til að eiga sér stað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="59c91-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="59c91-106">Til að nota afstemmingu farms sjálfvirk, verður að setja upp aðalgögn endurskoðunar þar sem hægt er að skilgreina skilyrði sem ákvarða hvaða farmbréf jafnað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="59c91-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="59c91-107">Ferli afstemmingar farms</span><span class="sxs-lookup"><span data-stu-id="59c91-107">The freight reconciliation process</span></span>
<span data-ttu-id="59c91-108">Farmgjöld eru reiknaðar af taxtavél sem tengist viðkomandi farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="59c91-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="59c91-109">Þegar farmur er staðfest farmbréfs er mynduð og farmgjöld eru fluttar í honum.</span><span class="sxs-lookup"><span data-stu-id="59c91-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="59c91-110">Skatthlutfall farms eru skipts sem ýmis gjöld fyrir viðkomandi upprunaskjalið (innkaupapöntun, sölupöntun, og/eða flutningspöntun), eftir uppsetningu sem er notuð fyrir venjulegum reikningsferli.</span><span class="sxs-lookup"><span data-stu-id="59c91-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="59c91-111">Ferli afstemmingar farms (sem er einnig þekkt sem samsvarandi) getur hafist þegar farmreikninginn berst frá farmflytjandanum.</span><span class="sxs-lookup"><span data-stu-id="59c91-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="59c91-112">Hægt er að fá reikningsins rafrænt eða á pappír.</span><span class="sxs-lookup"><span data-stu-id="59c91-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="59c91-113">Ef reikningurinn er móttekin á pappír, hægt er að mynda rafræna reikninga með því að nota farmbréfið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="59c91-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="59c91-114">[![Afstemmingarferli farms](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="59c91-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="59c91-115">handvirkur afstemmingu</span><span class="sxs-lookup"><span data-stu-id="59c91-115">Manual reconciliation</span></span>
<span data-ttu-id="59c91-116">Ef verið er að afstemmingu farms handvirkt, verður að samsvara hverri reikningslínu með farmbréf línu eða línum fyrir farm sem verið er að reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="59c91-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="59c91-117">Gera þetta jöfnun á **Farmbréf og reikningsjöfnun** síðu.</span><span class="sxs-lookup"><span data-stu-id="59c91-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="59c91-118">Ef magn á reikningslínu passar ekki við upphæð farmbréf, verður að velja afstemmingarástæða fyrir mismuninn.</span><span class="sxs-lookup"><span data-stu-id="59c91-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="59c91-119">Ef eru margar ástæður fyrir afstemmingu er hægt að skipta ójöfnuð upphæð á þeim.</span><span class="sxs-lookup"><span data-stu-id="59c91-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="59c91-120">Ástæða afstemmingu ákvarðar hvernig mismunur upphæðirnar eru bókaðar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="59c91-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="59c91-121">Þegar afstemmingu allt reikningsupphæð er tekið, er hún send til samþykkis og síðan bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="59c91-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="59c91-122">Eftirfarandi dæmi sýnir hvernig á að mynda reikning farms og framkvæma afstemmingu farms.</span><span class="sxs-lookup"><span data-stu-id="59c91-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="59c91-123">[![Afstemmingarverk farms](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="59c91-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="59c91-124">Sjálfvirka afstemmingu</span><span class="sxs-lookup"><span data-stu-id="59c91-124">Automatic reconciliation</span></span>
<span data-ttu-id="59c91-125">Til að nota sjálfvirka afstemmingu, verður að tilgreina áætlun fyrir afstemmingu, og reikninga og farmflytjendur að nota.</span><span class="sxs-lookup"><span data-stu-id="59c91-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="59c91-126">Jöfnun reikningslínur og farmbréf er gert eftir uppsetningu á endurskoðunarsniðmát og farmbréfs gerð.</span><span class="sxs-lookup"><span data-stu-id="59c91-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="59c91-127">Eftir sjálfvirka afstemmingu er keyrð, verður að meðhöndla hvaða reikninga sem kerfið getur ekki samsvarað.</span><span class="sxs-lookup"><span data-stu-id="59c91-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="59c91-128">Verður svo að vinna þessar reikninga handvirkt áður en hægt er að bóka reikninga til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="59c91-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



