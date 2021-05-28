---
title: TDS-útreikningur á færslum innan samstæðu
description: Þetta efnisatriði lýsir ferlinu sem er notað til að reikna út frádrátt skatt sem dreginn er frá í uppruna (TDS) á færsla milli fyrirtækja í áföngum.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023331"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="e9f9f-103">TDS-útreikningur á færslum innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="e9f9f-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9f9f-104">Þetta efnisatriði lýsir ferlinu sem er notað til að reikna út frádrátt skatt sem dreginn er frá í uppruna (TDS) á færsla milli fyrirtækja í áföngum.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="e9f9f-105">Þegar innkaupapöntun eða sölupöntun samstæðu er stofnuð er sjálfgefinn TDS-hópur sem er skilgreindur fyrir viðskiptavininn eða lánardrottinn notaður til að reikna út TDS-fjárhæðina.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="e9f9f-106">TDS-upphæðin er bókuð á reikninga sem hægt er að endurheimta eða greiða eftir bókun reikningsins.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="e9f9f-107">Samstæðusölupöntun eða innkaupapöntun er sjálfkrafa stofnuð fyrir upprunalega innkaupapöntunina eða sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="e9f9f-108">Sjálfgefni TDS-hópurinn er sýndur á samstæðupöntun, þannig að hægt er að reikna út TDS.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="e9f9f-109">Hægt er að breyta TDS-hópnum.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-109">You can change the TDS group.</span></span> <span data-ttu-id="e9f9f-110">Einungis er hægt að bóka reikninginn ef nettóreikningsupphæð samstæðupöntun sem er sjálfkrafa búin til samsvarar nettóreikningsupphæð á upprunalegu pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="e9f9f-111">(Nettóupphæðin er reikningsupphæðin eftir að TDS er dregið frá.)</span><span class="sxs-lookup"><span data-stu-id="e9f9f-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="e9f9f-112">Sölureikningur er til dæmis stofnaður fyrir 50.000 og **10%** TDS-hópurinn er tengdur honum.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="e9f9f-113">Upphæð bókaðs reiknings er 45.000 og upphæð bókaðs TDS reiknings fyrir sölureikninginn er 5.000 krónur.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="e9f9f-114">Innkaupapöntun stofnast sjálfkrafa fyrir samstæðusölupöntunina og **10%** TDS-hópurinn er tengdur henni.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="e9f9f-115">Ef TDS-hópnum er breytt í **15%** er ekki hægt að bóka reikninginn vegna þess að nettógreiðsluupphæðin á samstæðusölupöntunin sem var stofnuð sjálfkrafa samsvarar ekki nettógreiðsluupphæðinni í upprunalegu sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="e9f9f-116">Greiðslubók sem er búin til fyrir samstæðureikning er sjálfkrafa bókuð.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="e9f9f-117">Aðeins er hægt að bóka greiðslubókina ef nettógreiðsluupphæðin á henni samsvarar nettógreiðsluupphæðinni á upphaflegu greiðslubókinni.</span><span class="sxs-lookup"><span data-stu-id="e9f9f-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
