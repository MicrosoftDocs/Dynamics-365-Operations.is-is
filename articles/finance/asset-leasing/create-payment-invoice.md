---
title: Stofna launareikninga
description: Þetta efnisatriði útskýrir hvernig á að stofna mánaðarlega reikninga fyrir leigusamning. Hægt er að stofna reikninga fyrir tiltekna leigusamninga eða nota runuvinnslu til að stofna reikninga fyrir marga leigusamninga.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444568"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="7ee71-104">Stofna launareikninga</span><span class="sxs-lookup"><span data-stu-id="7ee71-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ee71-105">Hægt er að stofna mánaðarlega reikninga fyrir tiltekna leigusamninga eða nota runuvinnslu til að stofna reikninga fyrir marga leigusamninga.</span><span class="sxs-lookup"><span data-stu-id="7ee71-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="7ee71-106">Eftirfarandi ferli sýnir hvernig á að stofna staka færslu leigugreiðslu þegar kveikt er á færibreytunni **Greiða lánardrottni** á síðunni **Uppsetning leigubókar**.</span><span class="sxs-lookup"><span data-stu-id="7ee71-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="7ee71-107">Á síðunni **Samantekt leigu** skal velja leigusamning og síðan **Bækur \> Greiðsluáætlun**.</span><span class="sxs-lookup"><span data-stu-id="7ee71-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="7ee71-108">Velja skal greiðsluna sem þarf að inna af hendi og síðan velja **Stofna færslubók**.</span><span class="sxs-lookup"><span data-stu-id="7ee71-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="7ee71-109">Þú færð skilaboð um að færslubók hafi verið stofnuð gegn valinni greiðslu.</span><span class="sxs-lookup"><span data-stu-id="7ee71-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="7ee71-110">Veldu **Reikningabækur** og veldu reikninginn sem þarf að greiða.</span><span class="sxs-lookup"><span data-stu-id="7ee71-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="7ee71-111">Á flipanum **Línur** skal fara yfir bókarfærsluna áður en hún er bókuð í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="7ee71-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ee71-112">Sjálfgefið er að reikningslínur lánardrottins sem eru stofnaðar noti bókunarreglu lánardrottins á síðunni **Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="7ee71-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="7ee71-113">Veljið rétta færslubók og veljið svo þann reikning sem þarf að greiða.</span><span class="sxs-lookup"><span data-stu-id="7ee71-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="7ee71-114">Í þessu dæmi er kveikt á færibreytunni **Greiða lánardrottni** í leigubókinni.</span><span class="sxs-lookup"><span data-stu-id="7ee71-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="7ee71-115">Þar af leiðir verður reikningurinn í reikningabókinni.</span><span class="sxs-lookup"><span data-stu-id="7ee71-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="7ee71-116">Í hlutanum **Yfirlit** birtist samantekt bókarfærslunnar og hlutinn **Línur** sýnir upplýsingar um raunverulegu færslubókarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="7ee71-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ee71-117">Ef slökkt er á færibreytunni **Greiða lánardrottni** eru greiðslubókarfærslur skráðar á síðunni **Eignarleiga** fyrir leigubókina og kerfið stofnar eignaleigufærslu í stað reiknings.</span><span class="sxs-lookup"><span data-stu-id="7ee71-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="7ee71-118">Leigugreiðslufærslan verður bókuð á færslubókarheitið sem er tilgreint í svæðinu **Mánaðarleg leigubók**.</span><span class="sxs-lookup"><span data-stu-id="7ee71-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="7ee71-119">Eftir að færslan er bókuð er hægt að skoða færsluupplýsingar og bókfært virði leiguskuldbindingar með því að velja **Skuldafærslur** í leigubókinni.</span><span class="sxs-lookup"><span data-stu-id="7ee71-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="7ee71-120">Í greiðsluáætluninni er merkt í gátreitinn **Færslubók bókuð** og línan sýnir númer reikningabókar.</span><span class="sxs-lookup"><span data-stu-id="7ee71-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="7ee71-121">Eftir að búið er að stofna greiðslubók og færslu fyrir þá færslubók verður að bakfæra færsluna áður en hægt er að endurgera hana.</span><span class="sxs-lookup"><span data-stu-id="7ee71-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
