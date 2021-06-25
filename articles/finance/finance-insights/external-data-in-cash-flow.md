---
title: Nota ytri gögn við sjóðsstreymisspár (forskoðun)
description: Þetta efnisatriði lýsir uppsetningarskrefunum sem þarf að ljúka til að hægt sé að færa ytri gögn inn eða flytja það inn í sjóðstreymisspár.
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186691"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="7c509-103">Nota ytri gögn við sjóðsstreymisspár (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="7c509-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7c509-104">Ytri gögn er hægt að færa inn eða flytja inn í sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="7c509-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="7c509-105">Þetta efnisatriði lýsir uppsetningarskrefunum sem eru sértæk fyrir notkun ytri gagna og sem gera kleift að taka ytri gögn með í sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="7c509-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="7c509-106">Ytri gagnauppsetning</span><span class="sxs-lookup"><span data-stu-id="7c509-106">External data setup</span></span>

<span data-ttu-id="7c509-107">Notaðu flipann **Ytri uppruni** á **uppsetning sjóðstreymisspár** síðu (**reiðufjár-og bankastjórnun \> sjóðsstreymisspá**) til að færa inn stillingar sem styðja notkun ytri gagna í sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="7c509-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="7c509-108">Frekari upplýsingar um uppsetninguna er að finna í [Sjóðstreymisspár´](../cash-bank-management/cash-flow-forecasting.md).</span><span class="sxs-lookup"><span data-stu-id="7c509-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="7c509-109">Til að færa inn ytri gögn fyrir sjóðsstreymisspár er hægt að nota Opna í Excel til að færa inn og breyta ytri gögnum.</span><span class="sxs-lookup"><span data-stu-id="7c509-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="7c509-110">Velja skal hnappinn **Ytri gögn** og velja síðan annað hvort **bæta við ytri gögnum** eða **breyta fyrirliggjandi ytri gögnum**.</span><span class="sxs-lookup"><span data-stu-id="7c509-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="7c509-111">Þegar Microsoft Excel-skráin er opnuð er hægt að færa inn upplýsingar í eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="7c509-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="7c509-112">**Færslukenni**</span><span class="sxs-lookup"><span data-stu-id="7c509-112">**Entry ID**</span></span>
- <span data-ttu-id="7c509-113">**Lýsing** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="7c509-113">**Description** (optional)</span></span>
- <span data-ttu-id="7c509-114">**Heiti ytri uppruna** – Velja skal eitt af gildunum á listanum sem voru skilgreindir þegar fjármálainnsýn var sett upp.</span><span class="sxs-lookup"><span data-stu-id="7c509-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="7c509-115">**Lögaðili**</span><span class="sxs-lookup"><span data-stu-id="7c509-115">**Legal Entity**</span></span>
- <span data-ttu-id="7c509-116">**Dagsetning**</span><span class="sxs-lookup"><span data-stu-id="7c509-116">**Date**</span></span>
- <span data-ttu-id="7c509-117">**Upphæð í gjaldmiðli færslu**</span><span class="sxs-lookup"><span data-stu-id="7c509-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="7c509-118">**Gjaldmiðilskóði**</span><span class="sxs-lookup"><span data-stu-id="7c509-118">**Currency Code**</span></span>
- <span data-ttu-id="7c509-119">**Sjálfgefin vídd** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="7c509-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="7c509-120">**Skjalanúmer** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="7c509-120">**Document number** (optional)</span></span>
- <span data-ttu-id="7c509-121">**Reikningsnúmer** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="7c509-121">**Account number** (optional)</span></span>
- <span data-ttu-id="7c509-122">**Reikningsheiti** (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="7c509-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="7c509-123">Flytur inn ytri gögn með því að nota rammann Stjórnun gagna</span><span class="sxs-lookup"><span data-stu-id="7c509-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="7c509-124">Hægt er að flytja inn ytri gögn fyrir sjóðsstreymisspá með því að nota vinnusvæðið **Gagnastjórnun** og eininguna sem er nefnd **Færsla ytri uppruna sjóðstreymisspár**.</span><span class="sxs-lookup"><span data-stu-id="7c509-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="7c509-125">Til viðbótar, ef nauðsynlegt er að setja uppsetningargögn úr einu umhverfi í annað, verða eftirfarandi einingar til staðar fyrir uppsetningartöflurnar sem krafist er:</span><span class="sxs-lookup"><span data-stu-id="7c509-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="7c509-126">Uppsetning ytri uppruna sjóðstreymisspár</span><span class="sxs-lookup"><span data-stu-id="7c509-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="7c509-127">Lögaðilauppsetning ytri uppruna sjóðstreymisspár</span><span class="sxs-lookup"><span data-stu-id="7c509-127">Cash flow forecast external source legal entity setup</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
