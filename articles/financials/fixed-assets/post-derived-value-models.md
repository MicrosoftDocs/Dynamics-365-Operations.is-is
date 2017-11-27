---
title: "Bókað í afleiddar bækur"
description: "Þessi grein lýsir því hvernig nota afleiddar Bækur."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 94eb82936da2a51a25105b26723088fb7dee9ae5
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="post-with-derived-books"></a><span data-ttu-id="a7936-103">Bókað í afleiddar bækur</span><span class="sxs-lookup"><span data-stu-id="a7936-103">Post with derived books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a7936-104">Þessi grein lýsir því hvernig nota afleiddar Bækur.</span><span class="sxs-lookup"><span data-stu-id="a7936-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="a7936-105">Þegar bókaðar eru færslur fyrir bóka sem inniheldur afleidd bækur, eru afleiddar bókafærslur bókaðar sjálfvirkt í færslubókum, innkaupapöntunum, eða reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="a7936-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="a7936-106">Ef aðalbókafærslur eru hins vegar undirbúnar í eignabókinni er hægt að skoða og breyta upphæðum afleiddra færslna áður en þær eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="a7936-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="a7936-107">Ákveðnir lyklar, svo sem VSK- og viðskiptavina- eða lánardrottnalyklar, eru uppfærðir aðeins einu sinni með bókunum á aðalbók.</span><span class="sxs-lookup"><span data-stu-id="a7936-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="a7936-108">Færslur afleidds bóka eru bókaðar á lyklana sem hafa verið skilgreindir fyrir afleitt bók á síðunni Bókunarreglur eigna.</span><span class="sxs-lookup"><span data-stu-id="a7936-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="a7936-109">Kaup eru oft notuð sem færslugerð fyrir afleidda bóka.</span><span class="sxs-lookup"><span data-stu-id="a7936-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="a7936-110">Þetta er notað þegar nota á bóka og afleitt bók á eign frá þeim tíma sem eignin var fengin.</span><span class="sxs-lookup"><span data-stu-id="a7936-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="a7936-111">Önnur gildi fyrir færslugerð kunna einnig að gilda.</span><span class="sxs-lookup"><span data-stu-id="a7936-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="a7936-112">Til dæmis, ef aðalbók og afleiddu bækurnar hafa sömu bilin að því er varðar sölu og losun, eru allar tegundir viðskipta með eignir tiltækar fyrir uppsetningu afleiddrar bókar.</span><span class="sxs-lookup"><span data-stu-id="a7936-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="a7936-113">Afskrift sem færð er í afleitt Bók verður sömu upphæðar og fært var fyrir aðalbók.</span><span class="sxs-lookup"><span data-stu-id="a7936-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="a7936-114">Ef afskriftaraðferðirnar eru mismunandi á milli bóka, þá á ekki að nota afleiðuaðferðina við að útbúa afskriftarfærslur.</span><span class="sxs-lookup"><span data-stu-id="a7936-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="a7936-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a7936-115">Example</span></span> 
<span data-ttu-id="a7936-116">Eftirfarandi upplýsingar sýna hvernig setja skal upp kaupfærslur með virkni fyrir afleidd bók.</span><span class="sxs-lookup"><span data-stu-id="a7936-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="a7936-117">Stofna bækurnar á síðunni Bókum.</span><span class="sxs-lookup"><span data-stu-id="a7936-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="a7936-118">Bók fyrir bókhaldið: VM 1, Núgildandi bókunarlag</span><span class="sxs-lookup"><span data-stu-id="a7936-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="a7936-119">Bóka fyrir skattamál: VM 2, Skattabókunarlag</span><span class="sxs-lookup"><span data-stu-id="a7936-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="a7936-120">Á VM 1 skal smella á flipann Afleiddar bækur. Veljið VM 2 í reitnum bók og Kaup í reitnum Færslugerð.</span><span class="sxs-lookup"><span data-stu-id="a7936-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="a7936-121">Þá er hægt að tengja bók við tilteknar eignir.</span><span class="sxs-lookup"><span data-stu-id="a7936-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="a7936-122">Þegar kaup eru færð vegna eigna með bóka VL 1 eru kaupin ekki einungis færð á VM 1, heldur einnig á afleiddu bókina VM 2.</span><span class="sxs-lookup"><span data-stu-id="a7936-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="a7936-123">Staða beggja bóka eigna er uppfærð í Opið.</span><span class="sxs-lookup"><span data-stu-id="a7936-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="a7936-124">Ef ekki eru notuð afleidd bækur skal bóka kaupin á eigninni fyrir bæði bækur VM 1 og bók VM 2.</span><span class="sxs-lookup"><span data-stu-id="a7936-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="a7936-125">Nánari upplýsingar er að finna í [Afleiddar bækur](derived-books.md)</span><span class="sxs-lookup"><span data-stu-id="a7936-125">For more information, see [Derived books](derived-books.md)</span></span>




