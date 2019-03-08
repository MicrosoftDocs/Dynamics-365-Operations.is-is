---
title: Skoðun uppruna bókhalds
description: Þessari grein veitir upplýsingar um hugbúnaðinn skoðun bókhaldsuppruna, sem hægt er að nota fyrir nákvæma greiningu á upprunaupplýsingum á bakvið færslur fjárhagslykils.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de5de039c0e3332943bae4846768fc628810906e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "330196"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="cd933-103">Skoðun uppruna bókhalds</span><span class="sxs-lookup"><span data-stu-id="cd933-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd933-104">Þessari grein veitir upplýsingar um hugbúnaðinn skoðun bókhaldsuppruna, sem hægt er að nota fyrir nákvæma greiningu á upprunaupplýsingum á bakvið færslur fjárhagslykils.</span><span class="sxs-lookup"><span data-stu-id="cd933-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="cd933-105">Skoðun uppruna bókhalds er ný síða sem sýnir upplýsingar um uppruna.</span><span class="sxs-lookup"><span data-stu-id="cd933-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="cd933-106">Hægt er að nota Skoðun uppruna bókhalds annaðhvort sem stakt verkfæri eða til að greina upplýsingar á bak við bókhaldsfærslur í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="cd933-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="cd933-107">Til dæmis er hægt að nota Skoðun uppruna bókhalds til°að fá sem nákvæmastar upplýsingar um uppruna fyrir stöðu á Endurskoðunarstöðu eða fylgiskjali færslu.</span><span class="sxs-lookup"><span data-stu-id="cd933-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="cd933-108">Hægt er að nota eiginleikann Flytja yfir í MS Excel til frekari skoðunar á upplýsingunum°í Microsoft Excel (til dæmis í Pivot-töflu eða Pivot-töflu skýrslu).</span><span class="sxs-lookup"><span data-stu-id="cd933-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="cd933-109">Skoðun uppruna lykils sýnir alltaf sömu heildarupphæð fyrir hvern fjárhagslykil°eins og fjárhagurinn sýnir (t.d. í prófjöfnuði).</span><span class="sxs-lookup"><span data-stu-id="cd933-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="cd933-110">Eins°og í prófjöfnuði er hægt að birta hluta í aðskildum dálkum.</span><span class="sxs-lookup"><span data-stu-id="cd933-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="cd933-111">Veljið viðeigandi fjárhagsvíddasafn.</span><span class="sxs-lookup"><span data-stu-id="cd933-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="cd933-112">Hægt er að nota færibreytur til að skilgreina tímabil fyrir greiningu.</span><span class="sxs-lookup"><span data-stu-id="cd933-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="cd933-113">Þessi virkni svipar einnig til aðgerða í prófjöfnuði.</span><span class="sxs-lookup"><span data-stu-id="cd933-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="cd933-114">Fyrir öll skjöl sem eru notuð í upprunaskjalsrammanum sýnir Skoðun uppruna lykils viðbótarupplýsingar, byggðar á dreifingu á fjárhagsupphæð og, ef við á, dreifingu á fjárhagsupphæð.</span><span class="sxs-lookup"><span data-stu-id="cd933-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="cd933-115">Þessar upplýsingar fela meðal annars í sér gerð peningaupphæðar, verk, verkþátt, tegund og línueiginleika.</span><span class="sxs-lookup"><span data-stu-id="cd933-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="cd933-116">Hér eru nokkur°dæmi um greiningu sem hægt er að gera:</span><span class="sxs-lookup"><span data-stu-id="cd933-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="cd933-117">Frávik milli innkaupapantana og reikninga lánardrottna, þar sem hvert frávik er táknað af peningaupphæð, t.d. gjaldfráviki.</span><span class="sxs-lookup"><span data-stu-id="cd933-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="cd933-118">Reikningshæfir eða ekki reikningshæfir tímar og útgjöld á verk, viðskiptaeiningu og aðallykil.</span><span class="sxs-lookup"><span data-stu-id="cd933-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="cd933-119">Fyrir upprunaskjöl sem nota einkennishugtakið tilvísanir í upprunaskjöl, gefur Skoðun uppruna bókhalds jafnvel nánari upplýsingar, svo sem um viðskiptavin, lánardrottin, starfsmann, afurð, magn, textaeiningu og lýsingar.</span><span class="sxs-lookup"><span data-stu-id="cd933-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="cd933-120">Hér eru nokkur°dæmi um greiningu sem hægt er að gera:</span><span class="sxs-lookup"><span data-stu-id="cd933-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="cd933-121">Hótelútgjöld eftir viðskiptaeiningu og hótel vörumerki fyrir fjárhagstímabil, byggt á kostnaðarskýrslum</span><span class="sxs-lookup"><span data-stu-id="cd933-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="cd933-122">Afsláttur fyrir lánardrottin, vöru, deild</span><span class="sxs-lookup"><span data-stu-id="cd933-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="cd933-123">Fyrir þessi skjöl er einnig hægt að skoða raunveruleg upprunaskjöl úr Skoðun uppruna bókhalds.</span><span class="sxs-lookup"><span data-stu-id="cd933-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>



