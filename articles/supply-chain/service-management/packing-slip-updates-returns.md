---
title: Uppfærslur á fylgiseðli fyrir skil
description: Áður en hægt er að taka á móti skilavöru í birgðum, þarf að uppfæra fylgiseðil fyrir pöntunina sem hún tilheyrir.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e3ea1fc5a7d75682df431b73be40b28ba6f6bc9
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830004"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="391f5-103">Uppfærslur á fylgiseðli fyrir skil</span><span class="sxs-lookup"><span data-stu-id="391f5-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="391f5-104">Áður en hægt er að taka á móti skilavöru í birgðum, þarf að uppfæra fylgiseðil fyrir pöntunina sem hún tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="391f5-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="391f5-105">Á sama hátt og uppfærsluferli reiknings er uppfærsla fjárhagsfærslunnar, er uppfærsluferli fylgiseðils efnisleg uppfærsla birgðafærslunnar, sem þýðir að það framkvæmir breytingarnar á birgðunum.</span><span class="sxs-lookup"><span data-stu-id="391f5-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="391f5-106">Þegar um er að ræða skil, eru skrefin sem hafa verið úthlutuð fyrir ráðstöfunaraðgerð innleidd á meðan á fylgiseðilsuppfærslu stendur.</span><span class="sxs-lookup"><span data-stu-id="391f5-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="391f5-107">Hægt er að vinna fylgiseðilsuppfærslu í annað hvort  vörukomubók eða skilapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="391f5-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="391f5-108">Hluti ferlisins við bókun fylgiseðla er að hægt sé að tengja tilvísunarnúmer fylgiseðils úr sendingarskjölum viðskiptavinar við pöntunarlínur.</span><span class="sxs-lookup"><span data-stu-id="391f5-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="391f5-109">Þessi tenging er valfrjáls og aðeins til tilvísunar.</span><span class="sxs-lookup"><span data-stu-id="391f5-109">This association is optional and for reference only.</span></span> <span data-ttu-id="391f5-110">Hún býr ekki til neinar færsluuppfærslur.</span><span class="sxs-lookup"><span data-stu-id="391f5-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="391f5-111">Ef allar væntanlegar skilavörur hafa ekki skilað sér skaltu hafa aðeins það magn með sem hefur verið tekið á móti í uppfærslu fylgiseðlar.</span><span class="sxs-lookup"><span data-stu-id="391f5-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="391f5-112">Skildu eftir vörurnar sem eftir eru af pöntuninni þar til afgangurinn af skilasendingunni hefur skilað sér.</span><span class="sxs-lookup"><span data-stu-id="391f5-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="391f5-113">Ef hlutur er sendur frá biðgeymslu til „Afhendingar- og móttökudeildar“, svo sem þegar eftirlitsaðili biðgeymslunnar veit ekki hvar á að geyma hlutinn í birgðum, verður að uppfæra viðeigandi fylgiseðil til að skrá rétt og bregðast við ráðstöfunarkóðanum sem er tilgreindur vegna biðgeymslunnar.</span><span class="sxs-lookup"><span data-stu-id="391f5-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="391f5-114">Þegar þú uppfærir fylgiseðil fyrir skilavöru sem er frá sölusamningi er skuldbinding sölusamningsins fyrir vöruna sjálfkrafa uppfærð til að endurspegla breytinguna á magninu eða upphæðinni.</span><span class="sxs-lookup"><span data-stu-id="391f5-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="391f5-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="391f5-115">See also</span></span>

[<span data-ttu-id="391f5-116">Framkvæma uppfærslur á reikningi vegna skila</span><span class="sxs-lookup"><span data-stu-id="391f5-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


