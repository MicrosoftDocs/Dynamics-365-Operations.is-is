---
title: Nota ytri gögn við sjóðsstreymisspár (forskoðun)
description: Þetta efnisatriði lýsir uppsetningarskrefunum sem þarf að ljúka til að hægt sé að færa ytri gögn inn eða flytja það inn í sjóðstreymisspár.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 801327dc54f6d4cfef7a9f062395e29846783e8f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644946"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="b3477-103">Nota ytri gögn við sjóðsstreymisspár (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="b3477-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="b3477-104">Ytri gögn er hægt að færa inn eða flytja inn í sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="b3477-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="b3477-105">Þetta efnisatriði lýsir uppsetningarskrefunum sem eru sértæk fyrir notkun ytri gagna og sem gera kleift að taka ytri gögn með í sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="b3477-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="b3477-106">Ytri gagnauppsetning</span><span class="sxs-lookup"><span data-stu-id="b3477-106">External data setup</span></span>

<span data-ttu-id="b3477-107">Notaðu flipann **Ytri uppruni** á **uppsetning sjóðstreymisspár** síðu (**reiðufjár-og bankastjórnun \> sjóðsstreymisspá**) til að færa inn stillingar sem styðja notkun ytri gagna í sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="b3477-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="b3477-108">Frekari upplýsingar um uppsetninguna er að finna í [Sjóðstreymisspár´](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="b3477-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="b3477-109">Til að færa inn ytri gögn fyrir sjóðsstreymisspár er hægt að nota Opna í Excel til að færa inn og breyta ytri gögnum.</span><span class="sxs-lookup"><span data-stu-id="b3477-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="b3477-110">Velja skal hnappinn **Ytri gögn** og velja síðan annað hvort **bæta við ytri gögnum** eða **breyta fyrirliggjandi ytri gögnum**.</span><span class="sxs-lookup"><span data-stu-id="b3477-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="b3477-111">Þegar Microsoft Excel-skráin er opnuð er hægt að færa inn upplýsingar í eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="b3477-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="b3477-112">**Færslukenni**</span><span class="sxs-lookup"><span data-stu-id="b3477-112">**Entry ID**</span></span>
- <span data-ttu-id="b3477-113">**Lýsing** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="b3477-113">**Description** (optional)</span></span>
- <span data-ttu-id="b3477-114">**Heiti ytri uppruna** – Velja skal eitt af gildunum á listanum sem voru skilgreindir þegar fjármálainnsýn var sett upp.</span><span class="sxs-lookup"><span data-stu-id="b3477-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="b3477-115">**Lögaðili**</span><span class="sxs-lookup"><span data-stu-id="b3477-115">**Legal Entity**</span></span>
- <span data-ttu-id="b3477-116">**Dagsetning**</span><span class="sxs-lookup"><span data-stu-id="b3477-116">**Date**</span></span>
- <span data-ttu-id="b3477-117">**Upphæð í gjaldmiðli færslu**</span><span class="sxs-lookup"><span data-stu-id="b3477-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="b3477-118">**Gjaldmiðilskóði**</span><span class="sxs-lookup"><span data-stu-id="b3477-118">**Currency Code**</span></span>
- <span data-ttu-id="b3477-119">**Sjálfgefin vídd** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="b3477-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="b3477-120">**Skjalanúmer** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="b3477-120">**Document number** (optional)</span></span>
- <span data-ttu-id="b3477-121">**Reikningsnúmer** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="b3477-121">**Account number** (optional)</span></span>
- <span data-ttu-id="b3477-122">**Reikningsheiti** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="b3477-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="b3477-123">Flytur inn ytri gögn með því að nota rammann Stjórnun gagna</span><span class="sxs-lookup"><span data-stu-id="b3477-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="b3477-124">Hægt er að flytja inn ytri gögn fyrir sjóðsstreymisspá með því að nota vinnusvæðið **Gagnastjórnun** og eininguna sem er nefnd **Færsla ytri uppruna sjóðstreymisspár**.</span><span class="sxs-lookup"><span data-stu-id="b3477-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="b3477-125">Til viðbótar, ef nauðsynlegt er að setja uppsetningargögn úr einu umhverfi í annað, verða eftirfarandi einingar til staðar fyrir uppsetningartöflurnar sem krafist er:</span><span class="sxs-lookup"><span data-stu-id="b3477-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="b3477-126">Uppsetning ytri uppruna sjóðstreymisspár</span><span class="sxs-lookup"><span data-stu-id="b3477-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="b3477-127">Lögaðilauppsetning ytri uppruna sjóðstreymisspár</span><span class="sxs-lookup"><span data-stu-id="b3477-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="b3477-128">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="b3477-128">Privacy notice</span></span>
<span data-ttu-id="b3477-129">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="b3477-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
