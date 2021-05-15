---
title: Fylgiskjal er ekki búið til
description: Í þessu efnisatriði er að finna upplýsingar um úrræðaleit sem getur hjálpað til þegar búa á til fylgiskjal en það gerist ekki.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947658"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="5143d-103">Fylgiskjal er ekki búið til</span><span class="sxs-lookup"><span data-stu-id="5143d-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5143d-104">Ef búa á til fylgiskjal, en síðan **Fylgiskjalafærslur** sýnir ekki nein fylgiskjöl skal fylgja skrefunum í eftirfarandi hlutum eins og þarf til að úrræðaleita þetta vandamál.</span><span class="sxs-lookup"><span data-stu-id="5143d-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="5143d-105">[![Síða fylgiskjalsfærslna sem er ekki með nein fylgiskjöl](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="5143d-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="5143d-106">Athuga gildissvið skatts</span><span class="sxs-lookup"><span data-stu-id="5143d-106">Check the tax applicability</span></span>

1. <span data-ttu-id="5143d-107">Farið í **Skattur** \> **Reglubundin verk** \> **Færslur undirbókar sem hafa ekki verið fluttar**.</span><span class="sxs-lookup"><span data-stu-id="5143d-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="5143d-108">Ef skráning er til staðar skal velja hana og síðan **Flytja núna**.</span><span class="sxs-lookup"><span data-stu-id="5143d-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="5143d-109">[![Hnappur fyrir flutning núna á síðu fyrir færslur undirbókar sem hafa ekki verði fluttar](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="5143d-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="5143d-110">Opnið síðuna **Færslur fylgiskjals** aftur til að sjá hvort fylgiskjalið hafi verið búið til.</span><span class="sxs-lookup"><span data-stu-id="5143d-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="5143d-111">Ákvarða hvort sérstilling sé til staðar</span><span class="sxs-lookup"><span data-stu-id="5143d-111">Determine whether customization exists</span></span>

<span data-ttu-id="5143d-112">Ef þú hefur lokið við skrefin í fyrri hlutanum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="5143d-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="5143d-113">Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.</span><span class="sxs-lookup"><span data-stu-id="5143d-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
