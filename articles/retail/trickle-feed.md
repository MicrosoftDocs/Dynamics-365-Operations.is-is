---
title: Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar
description: Þetta efnisatriði lýsir stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar í Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693090"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="2d7ca-103">Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar (opin forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="2d7ca-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2d7ca-104">Í Dynamics 365 Retail útgáfu 10.0.4 og eldri útgáfum er smásöluuppgjör bókað í lok dags og allar færslur eru bókfærðar í lok dags.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-104">In Dynamics 365 Retail versions 10.0.4 and earlier, retail statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="2d7ca-105">Vinna verður úr háum færslum innan takmarkaðs tímaramma sem leiðir stundum til álags, læsingar og vandamála við bókun á uppgjöri.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="2d7ca-106">Einnig kemur það í veg fyrir að söluaðilar geti skráð tekjur og greiðslur í bókhaldið yfir daginn.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="2d7ca-107">Opin forútgáfa af stofnun hlutastraumspöntunar sem er hluti af Retail, útgáfu 10.0.5 gerir það kleift að vinna úr færslum yfir daginn og eiga einungis eftir að vinna úr fjárhagslegri afstemmingu greiðslumáta og öðrum reiðufjárstjórnunarfærslum við lok dags.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="2d7ca-108">Þessi eiginleiki jafnar álagið af því að búa til sölupantanir, reikninga og framkvæma greiðslur yfir daginn. Þetta veitir betri skilning á afkomu og gefur kost á að skrá tekjur og greiðslur í bókhald nánast í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="2d7ca-109">Hvernig á að nota bókun með hlutastraum</span><span class="sxs-lookup"><span data-stu-id="2d7ca-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="2d7ca-110">Til að virkja bókun með hlutastraum fyrir smásölufærslur skal fara í **Kerfisstjórnun > Uppsetning > Skilgreining leyfis** og gera lykillinn fyrir **smásöluuppgjör** óvirkan.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-110">To enable trickle feed-based posting of retail transactions, go to **System administration > Set up > License configuration** and disable the the **Retail statements** key.</span></span>

2. <span data-ttu-id="2d7ca-111">Á sömu síðu skal virkja leyfislykilinn fyrir **Smásöluuppgjör (hlutastraumur) - Forskoðun**.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-111">On the same page, enable the **Retail statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="2d7ca-112">Þegar þessi lykill er virkjaður skal ganga úr skugga um að engin uppgjör bíði þess að vera bókuð.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

> [!Important]
> <span data-ttu-id="2d7ca-113">Áður en leyfislykillinn fyrir **Smásöluuppgjör (hlutastraumur) - Forskoðun** er virkjaður skal ganga úr skugga um að engin uppgjör bíði þess að vera bókuð.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-113">Before you enable the **Retail statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="2d7ca-114">Núverandi uppgjörsskjali verður skipt upp í tvær mismunandi tegundir, færsluuppgjör og fjárhagsskýrslu.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="2d7ca-115">Færsluuppgjörið mun taka til allra óbókaðra og villuleitaðra smásölufærslna og stofna sölupantanir, sölureikninga, færslubækur fyrir greiðslur og afslætti og tekju-/útgjaldafærslur með þeim takti sem er grunnstilltur.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-115">The transactional statement will pick up all unposted and validated retail transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="2d7ca-116">Grunnstilla ætti ferlið til að keyra á hárri tíðni svo fylgiskjöl séu búin til þegar smásölufærslunum er hlaðið upp í Retail Headquarters í gegnum P-verkið.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-116">You should configure this process to run at a high frequency so that documents are created when the retail transactions are uploaded into Retail Headquarters through the P-job.</span></span> <span data-ttu-id="2d7ca-117">Með færsluuppgjöri sem býr sjálft til sölupantanir og sölureikninga er engin þörf á að grunnstilla runuvinnsluna **Bóka birgðir**.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="2d7ca-118">Hins vegar er enn hægt að nota hana til að uppfylla tilteknar viðskiptaþarfir sem notandinn kann að hafa.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="2d7ca-119">Fjárhagsskýrslan er stillt á þann hátt að hún er búin til í lok dags og styður aðeins lokunaraðferðina **Vakt**.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="2d7ca-120">Þessi skýrsla takmarkast við fjárhagslega afstemmingu og býr eingöngu til færslubækur fyrir upphæðamismun á milli talinnar upphæðar og færsluupphæðar fyrir mismunandi greiðslumáta ásamt færslubókum fyrir aðrar reiðufjárstjórnunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="2d7ca-121">Til að reikna út færsluuppgjörið skal smella á **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Reikna færsluuppgjör í runu**.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-121">To calculate the transactional statement, click **Retail > Retail IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="2d7ca-122">Til að bóka yfirlit færsluuppgjörs í runu skal smella á **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Bóka færsluuppgjör í runu**.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-122">To post the transactional statement statements in batch, click **Retail > Retail IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="2d7ca-123">Til að reikna út fjárhagsskýrsluna skal smella á **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Reikna fjárhagsskýrslur í runu**.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-123">To calculate the financial statement, click **Retail > Retail IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="2d7ca-124">Til að bóka fjárhagsskýrslur í runu skal smella á **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Bóka fjárhagsskýrslur í runu**.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-124">To post the financial statements in batch, click **Retail > Retail IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="2d7ca-125">Valmyndaratriðin **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Reikna uppgjör í runu** og **Smásala > Upplýsingatækni smásölu > Sölustaðarbókun > Bóka uppgjör í runu** verða fjarlægð með tilkomu þessa nýja eiginleika.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-125">The menu items **Retail > Retail IT > POS Posting > Calculate statements in batch** and **Retail > Retail IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="2d7ca-126">Einnig er hægt að búa til gerðir af færsluuppgjörum og fjárhagsskýrslum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="2d7ca-127">Opna skal **Smásala > Rásir > Smásöluverslanir** og smella á **Smásöluuppgjör**.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-127">Go to **Retail > Channels > Retail stores** and click **Retail statements**.</span></span> <span data-ttu-id="2d7ca-128">Smella skal á **Nýtt** og velja svo þá gerð uppgjörs sem stofna á.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="2d7ca-129">Svæðin á síðunni **Smásöluuppgjör** og aðgerðir í hlutanum **Uppgjörsflokkur** á síðunni birta gögn og aðgerðir í samræmi við valda gerð uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="2d7ca-129">Fields on the **Retail statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
