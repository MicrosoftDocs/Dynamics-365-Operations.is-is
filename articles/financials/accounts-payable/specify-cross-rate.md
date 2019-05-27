---
title: Tilgreina meðalgengi
description: Þetta efnisatriði veitir upplýsingar um meðalgengi í Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546065"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="2cf5f-103">Tilgreina meðalgengi</span><span class="sxs-lookup"><span data-stu-id="2cf5f-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cf5f-104">Í þessu efnisatriði útskýrir tilgang meðalgengi og hvernig á að tilgreina meðalgengi þegar greiðsla með reikningi er jafnaður.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="2cf5f-105">Nota skal meðalgengi þegar öll eftirfarandi skilyrði gilda:</span><span class="sxs-lookup"><span data-stu-id="2cf5f-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="2cf5f-106">Jafnað er á milli greiðslu með reikningi.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="2cf5f-107">Nota aðra gjaldmiðla greiðslulínu og reikningslínu.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="2cf5f-108">Hvorugur gjaldmiðill er uppgjörsmynt.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="2cf5f-109">Meðalgengi er ekki notað til að umreikna gjaldmiðil greiðslufærslu yfir á bókahaldsgjaldmiðil greiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="2cf5f-110">Í staðinn eru gengi gengistöflunnar sóttar til að reikna út virðið á gjaldmiðilsupphæð greiðslufærslunnar og gjaldmiðilsupphæð bókhaldsgreiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="2cf5f-111">Til dæmis bókhaldsgjaldmiðli er USD, er gjaldmiðill reikningsins er CAD og gjaldmiðil greiðslunnar er EUR.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="2cf5f-112">Meðalgengi er hægt að færa inn gengi til að þýða beint á milli CAD og EUR og ekki þarf að þýða gegnum USD.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="2cf5f-113">Þegar reikningur og aðalgreiðsla eru valin er hægt að slá inn meðalgengi fyrir reikningslínuna.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="2cf5f-114">Meðalgengið er gengið á milli gjaldmiðlanna fyrir þær færslur sem og fyrir jöfnunardagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="2cf5f-115">Farðu inn á eina af eftirfarandi síðum:</span><span class="sxs-lookup"><span data-stu-id="2cf5f-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="2cf5f-116">**Viðskiptakröfur > Almennt > Viðskiptavinir > Allir viðskiptavinir**</span><span class="sxs-lookup"><span data-stu-id="2cf5f-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="2cf5f-117">**Viðskiptaskuldir > Algengar > Lánardrottnar > Allir lánardrottnar**</span><span class="sxs-lookup"><span data-stu-id="2cf5f-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="2cf5f-118">**Innkaup og aðföng > Algengt > Lánardrottnar > Allir lánardrottnar**</span><span class="sxs-lookup"><span data-stu-id="2cf5f-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="2cf5f-119">Veljið viðskiptavininn eða lánardrottinninn sem eiga þær opnu færslur sem eru jafnaðar.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="2cf5f-120">Fyrir viðskiptavin, á listasíðunni **Allir viðskiptavinir**, skal fara í **Safna > Jafna opnar færslur**.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="2cf5f-121">Fyrir lánardrottin, á listasíðunni **Allir lánardrottnar**, skal fara í **Reikningur > Jafna opnar færslur**.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="2cf5f-122">Veldu færsluna sem er aðalgreiðslan og smelltu síðan á **Merkja greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="2cf5f-123">Gátreiturinn í dálknum **Merkja** er valinn og upplýsingatákn birtist í dálknum **Aðalgreiðsla**.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="2cf5f-124">Í reitnum **Meðalgengi** skal færa inn gengi milli gjaldmiðils reiknings og gjaldmiðils greiðslu frá og með jöfnunardagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
