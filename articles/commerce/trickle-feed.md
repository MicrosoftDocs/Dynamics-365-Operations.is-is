---
title: Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar
description: Þetta efnisatriði lýsir stofnun hlutastraumspöntunar fyrir færslur verslunar í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0fdb1f636183e8365729ab8947a50614a77eaeac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211046"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="edde4-103">Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar</span><span class="sxs-lookup"><span data-stu-id="edde4-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="edde4-104">Í Dynamics 365 Retail, útgáfu 10.0.4 og eldri útgáfum, er uppgjör bókað í lok dags og allar færslur eru bókfærðar í lok dags.</span><span class="sxs-lookup"><span data-stu-id="edde4-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="edde4-105">Vinna verður úr háum færslum innan takmarkaðs tímaramma sem leiðir stundum til álags, læsingar og vandamála við bókun á uppgjöri.</span><span class="sxs-lookup"><span data-stu-id="edde4-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="edde4-106">Einnig kemur það í veg fyrir að söluaðilar geti skráð tekjur og greiðslur í bókhaldið yfir daginn.</span><span class="sxs-lookup"><span data-stu-id="edde4-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="edde4-107">Með stofnun hlutastraumspöntunar sem er hluti af Retail, útgáfu 10.0.5, er hægt að vinna úr færslum yfir daginn og eiga einungis eftir að vinna úr fjárhagslegri afstemmingu greiðslumáta og öðrum reiðufjárstjórnunarfærslum í lok dags.</span><span class="sxs-lookup"><span data-stu-id="edde4-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="edde4-108">Þessi eiginleiki jafnar álagið af því að búa til sölupantanir, reikninga og framkvæma greiðslur yfir daginn. Þetta veitir betri skilning á afkomu og gefur kost á að skrá tekjur og greiðslur í bókhald nánast í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="edde4-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="edde4-109">Hvernig á að nota bókun með hlutastraum</span><span class="sxs-lookup"><span data-stu-id="edde4-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="edde4-110">Til að virkja hlutastraumsbókun smásölufærslna skal gera eiginleikann með heitinu **Smásöluuppgjör – hlutastraumur** virkan með Eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="edde4-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="edde4-111">Áður en eiginleikinn er virkjaður skal ganga úr skugga um að engin uppgjör bíði þess að vera bókuð.</span><span class="sxs-lookup"><span data-stu-id="edde4-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="edde4-112">Núverandi uppgjörsskjali verður skipt upp í tvær gerðir: færsluuppgjör og fjárhagsskýrslu.</span><span class="sxs-lookup"><span data-stu-id="edde4-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="edde4-113">Færsluuppgjörið mun taka til allra óbókaðra og villuleitaðra færslna og stofna sölupantanir, sölureikninga, færslubækur fyrir greiðslur og afslætti og tekju-/útgjaldafærslur með þeim takti sem er grunnstilltur.</span><span class="sxs-lookup"><span data-stu-id="edde4-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="edde4-114">Grunnstilla ætti ferlið til að keyra á hárri tíðni svo fylgiskjöl séu búin til þegar færslunum er hlaðið upp í höfuðstöðvum í gegnum P-verkið.</span><span class="sxs-lookup"><span data-stu-id="edde4-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="edde4-115">Með færsluuppgjöri sem býr sjálft til sölupantanir og sölureikninga er engin þörf á að grunnstilla runuvinnsluna **Bóka birgðir**.</span><span class="sxs-lookup"><span data-stu-id="edde4-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="edde4-116">Hins vegar er enn hægt að nota hana til að uppfylla tilteknar viðskiptaþarfir sem notandinn kann að hafa.</span><span class="sxs-lookup"><span data-stu-id="edde4-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="edde4-117">Fjárhagsskýrslan er stillt á þann hátt að hún er búin til í lok dags og styður aðeins lokunaraðferðina **Vakt**.</span><span class="sxs-lookup"><span data-stu-id="edde4-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="edde4-118">Þessi skýrsla takmarkast við fjárhagslega afstemmingu og býr eingöngu til færslubækur fyrir upphæðamismun á milli talinnar upphæðar og færsluupphæðar fyrir mismunandi greiðslumáta ásamt færslubókum fyrir aðrar reiðufjárstjórnunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="edde4-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="edde4-119">Til að reikna út færsluuppgjörið skal opna **Retail og Commerce > Upplýsingatækni Retail og Commerce > Sölustaðarbókun > Reikna færsluuppgjör í runu**.</span><span class="sxs-lookup"><span data-stu-id="edde4-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="edde4-120">Til að bóka færsluuppgjörið í runu skal opna **Retail og Commerce > Upplýsingatækni Retail og Commerce > Sölustaðarbókun > Bóka færsluuppgjör í runu**.</span><span class="sxs-lookup"><span data-stu-id="edde4-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="edde4-121">Til að reikna út fjárhagsskýrsluna skal opna **Retail og Commerce > Upplýsingatækni Retail og Commerce > Sölustaðarbókun > Reikna fjárhagsskýrslur í runu**.</span><span class="sxs-lookup"><span data-stu-id="edde4-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="edde4-122">Til að bóka fjárhagsskýrslurnar í runu skal opna **Retail og Commerce > Upplýsingatækni Retail og Commerce > Sölustaðarbókun > Bóka fjárhagsskýrslur í runu**.</span><span class="sxs-lookup"><span data-stu-id="edde4-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="edde4-123">Valmyndaratriðin **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Sölustaðarbókun > Reikna uppgjör í runu** og **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Sölustaðarbókun > Bóka uppgjör í runu** verða fjarlægð með tilkomu þessa nýja eiginleika.</span><span class="sxs-lookup"><span data-stu-id="edde4-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="edde4-124">Einnig er hægt að búa til gerðir af færsluuppgjörum og fjárhagsskýrslum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="edde4-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="edde4-125">Opnið **Smásala og viðskipti > Rásir > Verslanir** og smellið á **Uppgjör**.</span><span class="sxs-lookup"><span data-stu-id="edde4-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="edde4-126">Smella skal á **Nýtt** og velja svo þá gerð uppgjörs sem stofna á.</span><span class="sxs-lookup"><span data-stu-id="edde4-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="edde4-127">Svæðin á síðunni **Uppgjör** og aðgerðir í hlutanum **Uppgjörsflokkur** á síðunni birta gögn og aðgerðir í samræmi við valda gerð uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="edde4-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]