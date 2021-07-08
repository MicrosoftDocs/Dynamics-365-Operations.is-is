---
title: Fjárhagur altæks birgðabókhalds
description: Í þessu efnisatriði er fjárhagsbókum altæks birgðabókhalds lýst, sem eru skilgreindar út frá samsetningu gjaldmiðils, dagatals, viðtekinni reglu og tengingu við lögaðila.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273172"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="394a1-103">Fjárhagur altæks birgðabókhalds</span><span class="sxs-lookup"><span data-stu-id="394a1-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="394a1-104">Altækt birgðabókhald er með eigin söfn af fjárhagsbókum.</span><span class="sxs-lookup"><span data-stu-id="394a1-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="394a1-105">Í hvert sinn sem unnið er úr birgðatengdri færslu fyrir viðeigandi lögaðila getur kerfið reiknað þá færslu í eins mörgum fjárhagsbókum altæks birgðabókhalds og þarf.</span><span class="sxs-lookup"><span data-stu-id="394a1-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="394a1-106">Fjárhagur er skrá yfir debet-og kreditráðstafanir.</span><span class="sxs-lookup"><span data-stu-id="394a1-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="394a1-107">Þessar ráðstafanir eru flokkaðar með því að nota kostnaðareiningar og fjárhagslykla undirbókar.</span><span class="sxs-lookup"><span data-stu-id="394a1-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="394a1-108">Fjárhagur altæks birgðabókhalds er skilgreindur eftir samsetningunni af gjaldmiðli, dagatali, viðtekinni reglu og tengingu við lögaðila.</span><span class="sxs-lookup"><span data-stu-id="394a1-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="394a1-109">Til að setja upp fjárhagsbækur altæks birgðabókhalds skal fara í **Altækt birgðabókhald \> Uppsetning \> Fjárhagir altæks birgðabókhalds**.</span><span class="sxs-lookup"><span data-stu-id="394a1-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="394a1-110">Fyrir hvern fjárhag skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="394a1-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="394a1-111">**Heiti** - Færið inn heiti fjárhagsins.</span><span class="sxs-lookup"><span data-stu-id="394a1-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="394a1-112">**Lýsing** - Færið inn lýsingu á fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="394a1-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="394a1-113">**Fjárhagsdagatal** – Tilgreinið fjárhagsdagatal fyrir fjárhaginn.</span><span class="sxs-lookup"><span data-stu-id="394a1-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="394a1-114">**Gjaldmiðill og gerð gengis** – Notið reitina í þessum flýtiflipa til að velja bókhaldsgjaldmiðil sem fjárhagurinn notar og gerð gengir.</span><span class="sxs-lookup"><span data-stu-id="394a1-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="394a1-115">Gjaldmiðillinn sem þú velur getur verið annar en gjaldmiðillinn sem lögaðilinn notar.</span><span class="sxs-lookup"><span data-stu-id="394a1-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="394a1-116">Í altæku birgðabókhaldi geta notendur skilgreint eins margar fjárhagsbækur kostnaðar og þarf til.</span><span class="sxs-lookup"><span data-stu-id="394a1-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="394a1-117">Altækt birgðabókhald styður birgðabókhald í mörgum gjaldmiðlum og í margs konar verðmati.</span><span class="sxs-lookup"><span data-stu-id="394a1-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="394a1-118">Stilltu eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="394a1-118">Set the following fields:</span></span>

    - <span data-ttu-id="394a1-119">**Gjaldmiðill** – Veljið þann kostnaðargjaldmiðil þar sem unnið er með birgðatengd gildi.</span><span class="sxs-lookup"><span data-stu-id="394a1-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="394a1-120">Þessi gildi eru birgðavirði, kostnaður seldra vara, birgðir í flutningi og alls kyns frávik.</span><span class="sxs-lookup"><span data-stu-id="394a1-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="394a1-121">**Gerð gengis** – Veljið gengið sem kerfið á að nota til að umreikna færsluupphæðinni í færslugjaldmiðilinn og staðalkostnað varanna í kostnaðargjaldmiðilinn.</span><span class="sxs-lookup"><span data-stu-id="394a1-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="394a1-122">**Heiti viðtekinnar reglu** – Tilgreinið viðtekna reglu.</span><span class="sxs-lookup"><span data-stu-id="394a1-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="394a1-123">Viðtekin regla er safn af reglum sem ákvarðar hvernig kostnaður verður færður inn í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="394a1-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="394a1-124">**Lögaðili** – Fjárhagurinn mun gera grein fyrir skjölunum sem bókuð eru í völdum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="394a1-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="394a1-125">**Undirbúningur** – Veljið hvort birgðafærslur sem voru stofnaðar áður en fjárhagurinn var stofnaður eigi að vera unnar í samræmi við gjaldmiðil og viðtekna reglu í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="394a1-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="394a1-126">Veljið eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="394a1-126">Select one of the following values:</span></span>

    - <span data-ttu-id="394a1-127">**Virkjað** – Fjárhagurinn á að vinna úr færslum sem voru stofnaðar áður en fjárhagurinn var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="394a1-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="394a1-128">**Óvirkjað** – Fjárhagurinn á aðeins að vinna úr færslum sem eru stofnaðar eftir að fjárhagurinn var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="394a1-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="394a1-129">Þú getur **ekki** komið aftur og stillt þennan reit eftir að þú hefur slegið inn ný skjöl.</span><span class="sxs-lookup"><span data-stu-id="394a1-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="394a1-130">**Staða** – Kerfið stillir sjálfkrafa stöðu nýlega stofnaðra fjárhagsbóka á *Undirbúa*.</span><span class="sxs-lookup"><span data-stu-id="394a1-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
