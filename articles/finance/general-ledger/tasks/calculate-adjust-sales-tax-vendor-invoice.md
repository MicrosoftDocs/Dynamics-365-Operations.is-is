---
title: Reikna og stilla virðisaukaskatt á reikningi lánardrottins
description: Þetta efni útskýrir hvernig leiðrétta skal söluskatt í reikningi lánardrottins í Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4d01fe7587e01c04af28be934a235d955455216
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204738"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="61b40-103">Reikna og stilla virðisaukaskatt á reikningi lánardrottins</span><span class="sxs-lookup"><span data-stu-id="61b40-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61b40-104">Þetta efni útskýrir hvernig leiðrétta skal söluskatt í reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="61b40-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="61b40-105">Ef upphaflega upprunaskjal sýnir mismunandi skattupphæðir útreiknaðar, er hægt að leiðrétta þessar upphæðir fyrir bókun.</span><span class="sxs-lookup"><span data-stu-id="61b40-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="61b40-106">Þetta verkefni notar DEMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="61b40-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="61b40-107">Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Reikningabók**.</span><span class="sxs-lookup"><span data-stu-id="61b40-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="61b40-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="61b40-108">Select **New**.</span></span>
3. <span data-ttu-id="61b40-109">Í reitnum **Nafn** í nýju línunni skaltu velja valkost í fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="61b40-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="61b40-110">Í aðgerðarúðunni velurðu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="61b40-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="61b40-111">Í reitnum **Lykill** tilgreinirðu þau gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="61b40-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="61b40-112">Í reitnum **Reikningur** færirðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="61b40-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="61b40-113">Í reitnum **Kredit** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="61b40-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="61b40-114">Í reitnum **Mótlykill** skal skilgreina æskileg gildi.</span><span class="sxs-lookup"><span data-stu-id="61b40-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="61b40-115">Veldu **Virðisaukaskattur**.</span><span class="sxs-lookup"><span data-stu-id="61b40-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="61b40-116">Í reitnum **Heildarupphæð eiginlegs virðisaukaskatts** færirðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="61b40-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="61b40-117">Á flipanum **Leiðrétting** er hægt að leiðrétta vsk-upphæðir fyrir hvern vsk-kóða.</span><span class="sxs-lookup"><span data-stu-id="61b40-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="61b40-118">Veldu **Endurstilla rauntölur út frá reiknuðum upphæðum**.</span><span class="sxs-lookup"><span data-stu-id="61b40-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="61b40-119">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="61b40-119">Select **OK**.</span></span>
14. <span data-ttu-id="61b40-120">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="61b40-120">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]