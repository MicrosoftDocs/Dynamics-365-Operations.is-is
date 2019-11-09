---
title: Gagnafræðileg próf með gögnum með Regression Suite Automation Tool
description: Í þessu efni er fjallað um ráðleggingar varðandi prófanir á gögnum með því að nota Regression Suite Automation Tool.
author: kfend
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: d62f5520ebffd939f03f30064991cfb174fbcc9d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178409"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a><span data-ttu-id="6d52b-103">Gagnafræðileg próf með gögnum með Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="6d52b-103">Data agnostic testing using the Regression Suite Automation Tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d52b-104">Þó að virkni löggildingar ERP forrita geti ekki verið að fullu gagnagagnræn, þá eru til margir áfangar og aðferðir til að prófa.</span><span class="sxs-lookup"><span data-stu-id="6d52b-104">While the functional validation of an ERP application can’t be fully data agnostic, there are multiple phases and approaches for testing.</span></span> <span data-ttu-id="6d52b-105">Þessir prófunarstig eru m.a.:</span><span class="sxs-lookup"><span data-stu-id="6d52b-105">These testing phases include:</span></span>  

- <span data-ttu-id="6d52b-106">SysTest rammi</span><span class="sxs-lookup"><span data-stu-id="6d52b-106">SysTest framework</span></span>
- <span data-ttu-id="6d52b-107">ATL rammi</span><span class="sxs-lookup"><span data-stu-id="6d52b-107">ATL frameowrk</span></span>
- <span data-ttu-id="6d52b-108">Regression Suite Automation Tool (RSAT)</span><span class="sxs-lookup"><span data-stu-id="6d52b-108">Regression Suite Automation Tool (RSAT)</span></span>

<span data-ttu-id="6d52b-109">[![Próf flokkunarpýramída](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)</span><span class="sxs-lookup"><span data-stu-id="6d52b-109">[![Test classification pyramid](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)</span></span>

## <a name="overview"></a><span data-ttu-id="6d52b-110">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="6d52b-110">Overview</span></span>
-   <span data-ttu-id="6d52b-111">**SysTest umgjörð** - SysTest umgjörðin er áreiðanleg til að skrifa einingapróf.</span><span class="sxs-lookup"><span data-stu-id="6d52b-111">**SysTest framework** – The SysTest framework is reliable for writing unit tests.</span></span> <span data-ttu-id="6d52b-112">Vegna þess að einingapróf eru venjulega að prófa aðferð eða aðgerð, ættu þau alltaf að vera gögn samnýtt og aðeins háð innsláttargögnum sem eru til staðar sem hluti af prófinu.</span><span class="sxs-lookup"><span data-stu-id="6d52b-112">Because unit tests are generally testing a method or function, they should always be data agnostic and dependent only on the input data that is provided as part of the test.</span></span>
-   <span data-ttu-id="6d52b-113">**ATL umgjörð** - Microsoft er með ATL ramma sem er abstrakt á SysTest umgjörðina og gerir hagnýt prófaskrif mun einfaldari og áreiðanlegri.</span><span class="sxs-lookup"><span data-stu-id="6d52b-113">**ATL framework** – Microsoft has an ATL framework that is an abstraction on the SysTest framework and makes functional test writing much more simple and reliable.</span></span> <span data-ttu-id="6d52b-114">Þessa ramma ætti að nota til að skrifa íhlutapróf eða einföld samþættingarpróf.</span><span class="sxs-lookup"><span data-stu-id="6d52b-114">This framework should be used for writing component tests or simple integration tests.</span></span>
-   <span data-ttu-id="6d52b-115">**RSAT** - RSAT er notað við samþættingarpróf og hagsveiflupróf.</span><span class="sxs-lookup"><span data-stu-id="6d52b-115">**RSAT** – The RSAT is used for integration tests and business cycle tests.</span></span> <span data-ttu-id="6d52b-116">Hagsveifluprófin, einnig kölluð aðhvarfsgildingarprófanir, eru háð fyrirliggjandi gögnum.</span><span class="sxs-lookup"><span data-stu-id="6d52b-116">The business cycle tests, also called the regression validation tests, are dependent on existing data.</span></span> <span data-ttu-id="6d52b-117">Samt sem áður geta þessi próf orðið gagnörvandi ef þú tekur til viðbótarþátta.</span><span class="sxs-lookup"><span data-stu-id="6d52b-117">However, these tests can become data agnostic if you consider additional factors.</span></span> 

    - <span data-ttu-id="6d52b-118">O Þar sem einingapróf og íhlutapróf eru lágmörk og geta að öllu leyti verið gagnagagnafull gögn (ekki háð núverandi gagnapakka), eru hagsveiflupróf eða aðhvarfsgildingarprófanir háð nokkrum gögnum sem fyrir eru.</span><span class="sxs-lookup"><span data-stu-id="6d52b-118">o Where unit tests and component tests are low level and can fully be data agnostic (not dependent on existing dataset), the business cycle or regression validation tests are dependent on some existing data.</span></span> <span data-ttu-id="6d52b-119">Þessi gögn fela í sér uppsetningu, stillingar (breytur) og aðalgögn (viðskiptavini, smásali, hlutir osfrv.), En aldrei viðskiptagögn.</span><span class="sxs-lookup"><span data-stu-id="6d52b-119">This data includes setup, configuration settings (parameters), and master data (customer, vendors, items, etc.), but never transaction data.</span></span> <span data-ttu-id="6d52b-120">Gakktu úr skugga um að meðan á prófinu stendur, ef einhverju af þessu er breytt, að þeim sé snúið aftur sem hluti af lokaprófinu.</span><span class="sxs-lookup"><span data-stu-id="6d52b-120">Make sure that during the test, if any of these are being changed, that they are reverted back as part of the final test.</span></span>
    - <span data-ttu-id="6d52b-121">Veldu aðalgögn út frá ákveðnum forsendum í stað þess að velja ákveðna skrá.</span><span class="sxs-lookup"><span data-stu-id="6d52b-121">Select master data based on certain criteria instead of selecting a particular record.</span></span> <span data-ttu-id="6d52b-122">Til dæmis, ef þú vilt velja hlut út frá víddargildum hans og framboði á lager, síaðu vörulistann með þessum gildum, veldu fyrsta hlutinn og afritaðu númerið sem á að nota til framtíðarprófa.</span><span class="sxs-lookup"><span data-stu-id="6d52b-122">For example, if you want to select an item based on its dimension values and stock availability, filter the product list with those values, select the first item, and copy the number to be used for future tests.</span></span> <span data-ttu-id="6d52b-123">Ef það er einföld aðalgagnalína eins og viðskiptavinur, söluaðili eða hlutur, þá er hægt að búa hana til sem hluta af sjálfvirkni og nota í framtíðarprófum með keðju.</span><span class="sxs-lookup"><span data-stu-id="6d52b-123">If it’s a simple master data line such as customer, vendor, or item, it can be created as part of the automation and used in future tests through chaining.</span></span> 
    - <span data-ttu-id="6d52b-124">O Sláðu inn sérstök auðkenni, svo sem reikningsnúmer, í gegnum númeraröðina eða með því að nota Microsoft Excel-aðgerðir eins og =TEXT(NOW(),"yyyymmddhhmm").</span><span class="sxs-lookup"><span data-stu-id="6d52b-124">o Enter the unique identifiers, such as invoice numbers, through the number sequence or by using Microsoft Excel functions such as =TEXT(NOW(),"yyyymmddhhmm").</span></span> <span data-ttu-id="6d52b-125">Þessi aðgerð mun veita einstakt númer á hverri mínútu, sem gerir þér kleift að fylgjast með þegar aðgerðin átti sér stað.</span><span class="sxs-lookup"><span data-stu-id="6d52b-125">This function will provide a unique number every minute, which allows you to track when the action happened.</span></span> <span data-ttu-id="6d52b-126">Þetta er hægt að nota fyrir breytur eins og móttökunúmer vöru og reikningsnúmer lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="6d52b-126">This can be used for variables such as product receipt numbers and vendor invoice numbers.</span></span> <span data-ttu-id="6d52b-127">Þessar prófanir halda áfram að vinna í sama gagnagrunni aftur og aftur, án þess að þurfa neina endurreisn.</span><span class="sxs-lookup"><span data-stu-id="6d52b-127">These tests continue to work on the same database again and again, without requiring any restoration.</span></span>
    - <span data-ttu-id="6d52b-128">Stilltu alltaf **Breyta stillingu** umhverfisins á **Lesa** eða **Breyta** sem fyrsta prófatilvikið vegna þess að sjálfgefinn valkostur er **Sjálfvirkt**. Valkostirnir **Sjálfvirkt** nota alltaf fyrri stillingu og geta valdið óáreiðanlegum prófum.</span><span class="sxs-lookup"><span data-stu-id="6d52b-128">Always set the **Edit mode** of the environment to **Read** or **Edit** as the first test case because the default option is **Auto**. The **Auto** options always uses the previous setting and can cause unreliable tests.</span></span> 
 
    <span data-ttu-id="6d52b-129">[![Valkostasíða, afkastaflipi](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)</span><span class="sxs-lookup"><span data-stu-id="6d52b-129">[![Options page, Performance tab](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)</span></span>
 
    - <span data-ttu-id="6d52b-130">Staðfesta aðeins eftir að þú síar á tiltekin viðskipti í stað almennrar staðfestingar.</span><span class="sxs-lookup"><span data-stu-id="6d52b-130">Only validate after you filter on a particular transaction instead of generic validation.</span></span> <span data-ttu-id="6d52b-131">Til dæmis, fyrir fjölda færslna, síaðu að viðskiptanúmerinu eða viðskiptadeginum þannig að löggildingin útiloki öll önnur viðskipti.</span><span class="sxs-lookup"><span data-stu-id="6d52b-131">For example, for the number of records, filter for the transaction number or the transaction date so that the validation excludes all other transactions.</span></span> 
    - <span data-ttu-id="6d52b-132">Ef þú ert að athuga jafnvægi viðskiptavina eða fjárhagsáætlunarprófun skaltu vista gildi fyrst og bæta síðan við viðskiptagildi þínu til að staðfesta væntanlega niðurstöðu í stað þess að staðfesta fast væntanlegt gildi.</span><span class="sxs-lookup"><span data-stu-id="6d52b-132">If you are checking a customer balance or budget check, save the value first and then add your transaction value to validate the expected result instead of validating a fixed expected value.</span></span> 
 