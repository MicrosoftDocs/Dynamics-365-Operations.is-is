---
title: Yfirlit yfir úrlausn á ósamræmi við jöfnun samtalna reiknings
description: Hægt er að nota jöfnun fyrir samtölur reiknings til að aðstoða við að tryggja að heildarreikningsupphæð víki ekki frá áætluðum upphæðum með meira en leyfileg frávikum.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a20368385ec43547ee3d29770bd83cdec47e4a
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864943"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a><span data-ttu-id="cdd15-103">Yfirlit yfir úrlausn á ósamræmi við jöfnun samtalna reiknings</span><span class="sxs-lookup"><span data-stu-id="cdd15-103">Resolve discrepancies during invoice totals matching overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdd15-104">Ein gerð villuprófunar á reikningsjöfnun er jöfnun fyrir samtölur reiknings.</span><span class="sxs-lookup"><span data-stu-id="cdd15-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="cdd15-105">Til að tilgreina að kerfið eigi að framkvæma jöfnun fyrir samtölur reiknings, á **Færibreytur viðskiptaskulda** síðunni í **Reikningaprófun** flipanum skal stilla **Jafna samtölur reiknings** valkostinn á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cdd15-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="cdd15-106">Hægt er að nota jöfnun fyrir samtölur reiknings til að aðstoða við að tryggja að heildarreikningsupphæð víki ekki frá áætluðum upphæðum með meira en leyfileg frávikum.</span><span class="sxs-lookup"><span data-stu-id="cdd15-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="cdd15-107">Sex samtölur eru bornar saman á síðunni **Upplýsingar um jöfnun á samtölum reiknings**.</span><span class="sxs-lookup"><span data-stu-id="cdd15-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="cdd15-108">Ef ein af samtölunum víkur frá áætlaðri samsvarandi heildar innkaupapöntun er jöfnunarmisræmi merkt.</span><span class="sxs-lookup"><span data-stu-id="cdd15-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="cdd15-109">Til að fara yfir reikning sem hefur misræmi í samtölum, í **Reikningsfærsla lánardrottins** vinnusvæðinu skal smella á **Biðreikningar** reitinn.</span><span class="sxs-lookup"><span data-stu-id="cdd15-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="cdd15-110">Í Aðgerðasvæði, á **Yfirfara** flipanum, smellið á **Samsvörunarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="cdd15-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="cdd15-111">Ef misræmi hefur fundist birtist viðvörunartákn við upphæð reiknings.</span><span class="sxs-lookup"><span data-stu-id="cdd15-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="cdd15-112">Hægt er að skoða frekari upplýsingar um samtölur með því að skoða upplýsingar um samsvörun reikninga.</span><span class="sxs-lookup"><span data-stu-id="cdd15-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="cdd15-113">Eftir að kennsl hafa verið borin á misræmið, gæti verið að það þurfi að hafa samband við lánardrottinninn ef talið er að upplýsingarnar á reikningnum séu ekki réttar.</span><span class="sxs-lookup"><span data-stu-id="cdd15-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="cdd15-114">Það er síðan háð samkomulagi við lánardrottinn, hver eftirfarandi verka verða framkvæmd:</span><span class="sxs-lookup"><span data-stu-id="cdd15-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="cdd15-115">Samþykkja verðmismun og bóka reikninginn með misræmi í samsvörun.</span><span class="sxs-lookup"><span data-stu-id="cdd15-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="cdd15-116">Kerfið getur sett upp að krefjast eigi samþykkis áður en hægt er að bóka ef misræmi eru í samsvörun.</span><span class="sxs-lookup"><span data-stu-id="cdd15-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="cdd15-117">Í þessu tilfelli er að samþykkja misræmi í samsvörun og einnig er hægt að færa inn athugasemd um samþykki.</span><span class="sxs-lookup"><span data-stu-id="cdd15-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="cdd15-118">Síðan er hægt að velja að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="cdd15-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="cdd15-119">Endurskoða reikningsupphæð skv. þeirri upphæð sem reiknað var með og bóka reikninginn þannig..</span><span class="sxs-lookup"><span data-stu-id="cdd15-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="cdd15-120">Biðja um fullan kreditreikning og nýjan leiðréttan reikning frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="cdd15-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="cdd15-121">Nánari upplýsingar er að finna í [Rannsaka eða leysa úr undantekningum](tasks/research-resolve-exceptions.md)</span><span class="sxs-lookup"><span data-stu-id="cdd15-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>


