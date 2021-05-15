---
title: Rangt reitargildi í TaxTrans
description: Í þessu efnisatriði er að finna upplýsingar um úrræðaleit á röngum reitargildum í TaxTrans.
author: bijian
manager: beya
ms.date: 04/27/2021
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
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947654"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="5e2a7-103">Rangt reitargildi í TaxTrans</span><span class="sxs-lookup"><span data-stu-id="5e2a7-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e2a7-104">Ef reitgildi í **TaxTrans** er rangt skal nota upplýsingarnar í þessu efnisatriði til að reyna að leysa vandamálið.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="5e2a7-105">Yfirlit yfir gildi</span><span class="sxs-lookup"><span data-stu-id="5e2a7-105">Overview of values</span></span>
<span data-ttu-id="5e2a7-106">Eftirfarandi listi sýnir hvernig **TaxTrans**, **TaxUncommitted** og **TmpTaxWorkTrans** eru svipuð gagnasett en virka öðruvísi.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="5e2a7-107">**TaxTrans** er síðasta niðurstaða bókaðrar skattfærslu í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="5e2a7-108">**TaxUncommitted** er milliútreikningur á skattaniðurstöðu sem helst í gagnagrunninum (ef það á við), sem verður notaður síðar í bókun.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="5e2a7-109">**TmpTaxWorkTrans** er tímabundin reiknuð skattútkoma í töflunni í minninu (Töflagerð = InMemory).</span><span class="sxs-lookup"><span data-stu-id="5e2a7-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="5e2a7-110">Ef þú finnur grunnorsök fyrir röngum dálki **TaxTrans** hefurðu einnig fundið grunnorsökina á röngum dálki **TaxUncommitted** og **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="5e2a7-111">Þetta er vegna þess að dálkarnir þrír eru afritaðir af hverjum öðrum.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="5e2a7-112">Yfirleitt er **TmpTaxWorkTrans** búið til við skattaútreikning og síðan, er **TaxUncommitted** búið til, ef við á.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="5e2a7-113">Á meðan á skattafærslu stendur myndast **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="5e2a7-114">Bæta við rofstöðum</span><span class="sxs-lookup"><span data-stu-id="5e2a7-114">Add breakpoints</span></span>
<span data-ttu-id="5e2a7-115">Til að bæta við rofstöðum skal ljúka eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="5e2a7-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="5e2a7-116">Bæta viðbótum og rofstöðum við í *insert()* og *update()* í viðbótunum eins og sýnt er hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="5e2a7-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="5e2a7-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="5e2a7-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="5e2a7-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="5e2a7-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="5e2a7-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="5e2a7-120">Einnig er hægt að bæta við rofstöðum beint þegar **TaxUnCommitted** er ekki innifalið.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="5e2a7-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="5e2a7-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="5e2a7-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="5e2a7-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="5e2a7-123">Endurgera og kemba</span><span class="sxs-lookup"><span data-stu-id="5e2a7-123">Reproduce and debug</span></span>

<span data-ttu-id="5e2a7-124">Eftir að rofpunktar hafa verið stilltir verða allar breytingar á varanleika gagna sýnilegar við kembun.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="5e2a7-125">Til að finna grundvallarorsök á röngum dálki **TaxTrans**, **TaxUncommitted** eða **TmpTaxWorkTrans** skal yfirfara og hafa eftirfarandi atriði í huga:</span><span class="sxs-lookup"><span data-stu-id="5e2a7-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="5e2a7-126">Síðasti rofstaðurinn þar sem dálkurinn er réttur.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="5e2a7-127">Fyrsti rofstaður þar sem dálkurinn er rangur.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="5e2a7-128">Hvað gerist á milli þessara tveggja punkta.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="5e2a7-129">Ákvarða hvort sérstilling sé til staðar</span><span class="sxs-lookup"><span data-stu-id="5e2a7-129">Determine whether customization exists</span></span>
<span data-ttu-id="5e2a7-130">Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu skoða hvort sérstillingar séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="5e2a7-131">Ef sérstilling er til staðar skal hafa samband við notendaþjónustu Microsoft til að fá aðstoð.</span><span class="sxs-lookup"><span data-stu-id="5e2a7-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

