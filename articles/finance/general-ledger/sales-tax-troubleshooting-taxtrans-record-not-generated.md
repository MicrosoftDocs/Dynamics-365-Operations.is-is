---
title: TaxTrans færsla er ekki mynduð
description: Í þessu efni eru upplýsingar um villuleit sem geta hjálpað þegar TaxTrans færsla er ekki búin til.
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
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947655"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="172ad-103">TaxTrans færsla er ekki mynduð</span><span class="sxs-lookup"><span data-stu-id="172ad-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="172ad-104">Ef þú velur **Bókaður virðisaukaskattur** fyrir færslu en síðan **Bókaður virðisaukaskattur** sýnir annaðhvort engar skattlínur eða vantar skattlínu gæti verið að færslan **TaxTrans** hafi ekki verið búin til.</span><span class="sxs-lookup"><span data-stu-id="172ad-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="172ad-105">[![Síða bókaðs virðisaukaskatts sem er með engin línuatriði](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="172ad-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="172ad-106">Til að leysa úr vandamálinu skal fylgja skrefunum í eftirfarandi hlutum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="172ad-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="172ad-107">Athugaðu söluskattinn áður en færslan er bókuð</span><span class="sxs-lookup"><span data-stu-id="172ad-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="172ad-108">Áður en færslan er bókuð skal á síðunni **Bókun reiknings** velja **Virðisaukaskattur** til að athuga útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="172ad-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="172ad-109">[![Hnappur virðisaukaskatts á bókunarsíðu reiknings](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="172ad-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="172ad-110">Farðu yfir niðurstöður útreikningsins á síðunni **Tímabundnar VSK-færslur**.</span><span class="sxs-lookup"><span data-stu-id="172ad-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="172ad-111">Ef enginn skattur er reiknaður skal skoða [Skattur er ekki reiknaður eða skattupphæð er núll](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="172ad-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="172ad-112">Finndu TaxTrans færsluna í öllum bókuðum virðisaukaskatti</span><span class="sxs-lookup"><span data-stu-id="172ad-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="172ad-113">Farið í **Skattur** \> **Fyrirspurnir og skýrslur** \> **Fyrirspurn um virðisaukaskatt** > **Bókaður virðisaukaskattur**.</span><span class="sxs-lookup"><span data-stu-id="172ad-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="172ad-114">Í dálkahausnum **Fylgiskjal** skal velja síumerkið til að finna færsluna **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="172ad-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="172ad-115">Skoðaðu dagsetninguna ef þú finnur þær söluskattsfærslur sem leitað er að.</span><span class="sxs-lookup"><span data-stu-id="172ad-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="172ad-116">Ef dagsetningin er frábrugðin dagsetningu færslubókarhauss skal stofna þjónustubeiðni Microsoft til að fá frekari aðstoð.</span><span class="sxs-lookup"><span data-stu-id="172ad-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="172ad-117">[![Síðan Bókaður virðisaukaskattur](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="172ad-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="172ad-118">Kemba til að athuga upplýsingar</span><span class="sxs-lookup"><span data-stu-id="172ad-118">Debug to check details</span></span>

1. <span data-ttu-id="172ad-119">Frekari upplýsingar um hvernig á að kemba og ákveða hvort **TmpTaxWorkTrans** og **TaxUncommitted** séu búin til á réttan hátt er að finna í [Reitargildi í TaxTrans er ekki rétt](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="172ad-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="172ad-120">Ef **TaxTmpWorkTrans** eða **TaxUncommitted** eru búin til á réttan hátt skal bæta við rofstað á **TaxPost::SaveAndPost()** og **Tax::SaveAndPost** til að kemba ástæðuna fyrir því af hverju **TaxTrans** er ekki sett inn.</span><span class="sxs-lookup"><span data-stu-id="172ad-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="172ad-121">[![Rofstöðum bætt við í kóða](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="172ad-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="172ad-122">[![Niðurstöður rofstaða sem bætt var við](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="172ad-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="172ad-123">Ákvarða hvort sérstilling sé til staðar</span><span class="sxs-lookup"><span data-stu-id="172ad-123">Determine whether customization exists</span></span>

<span data-ttu-id="172ad-124">Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="172ad-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="172ad-125">Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.</span><span class="sxs-lookup"><span data-stu-id="172ad-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
