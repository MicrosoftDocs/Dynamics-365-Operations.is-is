---
title: Stilla TDS-færibreytur í viðskiptaskuldum og viðskiptakröfum
description: Í þessu efnisatriði er útskýrt hvernig á að setja breytur í viðskiptaskuldir og viðskiptakröfur til að styðja við skatt sem dreginn er frá í uppruna (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023328"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="943bc-103">Stilla TDS-færibreytur í viðskiptaskuldum og viðskiptakröfum</span><span class="sxs-lookup"><span data-stu-id="943bc-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="943bc-104">Í þessu efnisatriði er útskýrt hvernig á að setja breytur í viðskiptaskuldir og viðskiptakröfur til að styðja við skatt sem dreginn er frá í uppruna (TDS).</span><span class="sxs-lookup"><span data-stu-id="943bc-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="943bc-105">Opnið **Skattur \> Uppsetning \> Færibreytur \> Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="943bc-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="943bc-106">Á flipanum **Uppfærslur** skal velja **Uppfæra pöntunarlínur** til að opna gluggann **Uppfæra pöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="943bc-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="943bc-107">Í hlutanum **TDS-hópur**, í reitnum **Uppfærsla TDS-hóps**, skal tilgreina aðferðina sem nota skal við uppfærslu TDS-hópsins á línustigi.</span><span class="sxs-lookup"><span data-stu-id="943bc-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="943bc-108">Stillingin er notuð þegar TDS-hópurinn er uppfærður í pöntunarhaus.</span><span class="sxs-lookup"><span data-stu-id="943bc-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="943bc-109">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="943bc-109">The following options are available:</span></span>

    - <span data-ttu-id="943bc-110">**Aldrei** – TDS-hópurinn er ekki uppfærður í pöntunarlínunum þegar hann er uppfærður í pöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="943bc-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="943bc-111">**Alltaf** – TDS-hópurinn uppfærist sjálfkrafa á pöntunarlínunum þegar hann uppfærist í pöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="943bc-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="943bc-112">**Spurning** – Notendur fá skilaboð þar sem þeir eru beðnir um að uppfæra TDS hópinn á pöntunarlínunum.</span><span class="sxs-lookup"><span data-stu-id="943bc-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="943bc-113">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="943bc-113">Select **OK**.</span></span>

    <span data-ttu-id="943bc-114">[![Svargluggi fyrir uppfærslu afurða](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="943bc-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="943bc-115">Opnið **Skattur \> Uppsetning \> Færibreytur \> Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="943bc-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="943bc-116">Á flipanum **Almennt** á flýtiflipanum **Skipting á grundvelli afhendingarupplýsinga** skal stilla valkostinn **Innhreyfingarskjal** á **Já** til að birta og skipta innhreyfingarskjali með mismunandi heimilisföngum og skattreikningsnúmerum (TAN).</span><span class="sxs-lookup"><span data-stu-id="943bc-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="943bc-117">Ef þessi valkostur er stilltur á **Nei** er ekki hægt að bóka fylgiseðil með öðru heimilisfangi og skattareikningsnúmerum.</span><span class="sxs-lookup"><span data-stu-id="943bc-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="943bc-118">Stillið valkostinn **Reikningur** á **Já** til að bóka og skipta innkaupareikningi með öðru heimilsföngum og skattareikningsnúmerum.</span><span class="sxs-lookup"><span data-stu-id="943bc-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="943bc-119">[![Skipting á grundvelli afhendingarupplýsinga](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="943bc-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="943bc-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="943bc-120">Close the page.</span></span>
