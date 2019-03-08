---
title: Fastir bókunarlyklar eignakaupa
description: Þessi grein útskýrir hvernig á að setja upp almenna bókunarreikninga til eignast eignir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ac1580e33197c0cd8a82f34804d4639945d861
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "325366"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="17496-103">Fastir bókunarlyklar eignakaupa</span><span class="sxs-lookup"><span data-stu-id="17496-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17496-104">Þessi grein útskýrir hvernig á að setja upp almenna bókunarreikninga til eignast eignir.</span><span class="sxs-lookup"><span data-stu-id="17496-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="17496-105">Lyklar sem eru notaðir til að bóka eignakaup geta verið mismunandi, eftir því hvaða aðferð er notuð til að kaupa eignir.</span><span class="sxs-lookup"><span data-stu-id="17496-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="17496-106">Á síðunni bókunarreglur eigna, í Fjárhagsreiknings flipa, veljið Kaup og Leiðrétting kaupa til að setja upp eignalykla til að bóka í fjárhaginn.</span><span class="sxs-lookup"><span data-stu-id="17496-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="17496-107">Í færslubókum og á innkaupapöntunum er Fjárhagsreikningur oftast efnahagslykillinn þar sem kaupvirði nýju eignarinnar er skuldfært.</span><span class="sxs-lookup"><span data-stu-id="17496-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="17496-108">Þessi lykill getur ekki birst í færslubók og er ekki hægt að skipta út í færslum.</span><span class="sxs-lookup"><span data-stu-id="17496-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="17496-109">Mótlykill er líka efnahagslykill.</span><span class="sxs-lookup"><span data-stu-id="17496-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="17496-110">Í almennu færslubókinni og í eignabókinni er þessi lykill oft bankareikningurinn sem er notaður til að greiða fyrir kaup eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="17496-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="17496-111">Mótlykillinn er sjálfgefinn lykill sem er stungið upp á í færslubókunum.</span><span class="sxs-lookup"><span data-stu-id="17496-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="17496-112">Hægt er að breyta þessu í færslubókinni í einhvern annan reikning úr bókhaldslykli eða í lánardrottnalykil, ef eignin var keypt af lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="17496-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="17496-113">Þegar reikningabók eða innkaupapöntun í viðskiptaskuldum eru notuð fyrir eignakaup, er mótlyklinum fyrir eignafærsluna skipt úr fyrir lánardrottnareikninginn sem er valinn fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="17496-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="17496-114">Fyrir kaup bókuð með því að nota færslubókina eignabirgðir í fjárhagnum er eignin ekki keypt af utanaðkomandi aðila heldur færð úr eigin birgðum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="17496-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="17496-115">Þess vegna, mótlykill er lykill birgðaúthreyfingar fyrir birgðavara í birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="17496-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="17496-116">Frekari upplýsingar eru í [Kaupa eignir með innkaupum](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="17496-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



