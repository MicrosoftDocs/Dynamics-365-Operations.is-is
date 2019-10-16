---
title: Skilgreina og vinna úr skiptum á skilapöntun
description: Þetta efnisatriði útskýrir hvernig skilgreina á skipti á skilum í Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3ce327a918159771df0acab276b1169d2ad77825
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025380"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="c67b9-103">Skilgreina og vinna úr skiptum á skilapöntun</span><span class="sxs-lookup"><span data-stu-id="c67b9-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c67b9-104">Í eldri útgáfum af Dynamics 365 Retail var notað skjal vöruskilapöntunar í Retail Headquarters við úrvinnslu á skilum sem tengdust pöntunum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="c67b9-104">In previous versions of Dynamics 365 Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</span></span> <span data-ttu-id="c67b9-105">Hins vegar er aðeins hægt að nota skjal skilapöntunar til að vinna úr afurðum sem verið er að skila.</span><span class="sxs-lookup"><span data-stu-id="c67b9-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="c67b9-106">Afurðir sem hefur verið skilað eru sýndar með neikvæðu magni á línum skilapöntunar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="c67b9-107">Aftur á móti eru sölur sýndar með jákvæðu magni.</span><span class="sxs-lookup"><span data-stu-id="c67b9-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="c67b9-108">Skjal vöruskilapöntunar styður hins vegar ekki jákvætt magn.</span><span class="sxs-lookup"><span data-stu-id="c67b9-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="c67b9-109">Út af þessari takmörkun studdu eldri útgáfur af Retail ekki kringumstæður þar sem skil afurða eru gerð með því að nota skjal skilapöntunar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="c67b9-110">Hins vegar er búið að bæta við virkni sem styður kringumstæður þar sem gerð eru skipti á vöruskilapöntunum.</span><span class="sxs-lookup"><span data-stu-id="c67b9-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="c67b9-111">Retail notar nú sölupöntunarskjalið í stað skjals vöruskilapöntunar til að vinna úr þess konar færslugerðum.</span><span class="sxs-lookup"><span data-stu-id="c67b9-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="c67b9-112">Skilgreina Retail til að styðja skipti á vöruskilapöntunum</span><span class="sxs-lookup"><span data-stu-id="c67b9-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="c67b9-113">Fylgið þessum skrefum til að skilgreina kerfið svo það styðji skipti á vöruskilapöntunum.</span><span class="sxs-lookup"><span data-stu-id="c67b9-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="c67b9-114">Opnið **Retail \> Uppsetning höfuðstöðva \> Færibreytur \> Smásölufæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="c67b9-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="c67b9-115">Á flýtiflipanum **Pantanir viðskiptavinar** skal stilla valkostinn **Vinna úr skilapöntunum eins og sölupöntunum** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c67b9-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="c67b9-116">Keyrið verkið **Dreifingaráætlun altækrar skilgreiningar** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="c67b9-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="c67b9-117">Skipti gerð</span><span class="sxs-lookup"><span data-stu-id="c67b9-117">Make an exchange</span></span>

<span data-ttu-id="c67b9-118">Eftir að kerfið hefur verið skilgreint samkvæmt lýsingu í kaflanum hér á undan, heldur notandi sölustaðar áfram að velja sölupöntun eða sölureikning til að vinna úr skilum eins og í eldri útgáfum af Retail.</span><span class="sxs-lookup"><span data-stu-id="c67b9-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="c67b9-119">Eftir að skilavörum er bætt við körfuna getur notandinn hins vegar bætt nýjum sölulínum við hana.</span><span class="sxs-lookup"><span data-stu-id="c67b9-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="c67b9-120">Notandi verður að skilgreina allar nauðsynlegar eigindir fyrir þessar nýju sölulínur til að geta unnið úr pöntunarlínu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="c67b9-121">Þessar eigindir fela í sér afhendingaraðferð og uppfyllingarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="c67b9-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="c67b9-122">Greiðslan sem þarf að inna af hendi fyrir færsluna verður nettó af línum vöruskilapöntunar og línum sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="c67b9-123">Þegar greiðsla er gerð upp fyrir færsluna verður skilapöntunin bókuð sem sölupöntunarskjal í Retail Headquarters og kerfið reikningsfærir um leið skilalínurnar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="c67b9-124">Til að bjóða upp á aukinn sýnileika á hinum ýmsu upphæðum fyrir körfuna hefur þremur nýjum upphæðareitum verið bætt við hana.</span><span class="sxs-lookup"><span data-stu-id="c67b9-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="c67b9-125">Hægt er að nota skjáhönnuðinn til að gera þessa nýju reiti tiltæka í notandaviðmóti sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="c67b9-126">**Innborgun notuð** – Upphæð innborgunar sem er notuð í færslu þegar notandi velur að pöntun viðskiptavinar verði sótt.</span><span class="sxs-lookup"><span data-stu-id="c67b9-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="c67b9-127">Ef engin hnekking innborgunar er til staðar, og 10% innborgun er skilgreind, er upphæðin í þessum reit 90% af heildarupphæð pöntunar viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="c67b9-128">**Taka með upphæð** – Heildarupphæð fyrir línur þar sem afhendingarmátinn var stilltur á **Taka með** þegar pöntun viðskiptavinar var stofnuð eða breytt, eða við skipti á pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="c67b9-129">Upphæðin í þessum reit inniheldur skatta og gjöld.</span><span class="sxs-lookup"><span data-stu-id="c67b9-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="c67b9-130">**Upphæð skila** – Heildarfjöldi lína sem eru með neikvætt magn við skipti á pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c67b9-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="c67b9-131">Upphæðin í þessum reit inniheldur skatta og gjöld.</span><span class="sxs-lookup"><span data-stu-id="c67b9-131">The amount in this field includes taxes and charges.</span></span>
