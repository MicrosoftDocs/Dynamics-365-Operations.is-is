---
title: Uppfærslur á fylgiseðli fyrir skil
description: Áður en hægt er að taka á móti skilavöru í birgðum, þarf að uppfæra fylgiseðil fyrir pöntunina sem hún tilheyrir.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aba61e6acf5fb959917da9ddea94c21fe1460d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "344870"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="016a8-103">Uppfærslur á fylgiseðli fyrir skil</span><span class="sxs-lookup"><span data-stu-id="016a8-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="016a8-104">Áður en hægt er að taka á móti skilavöru í birgðum, þarf að uppfæra fylgiseðil fyrir pöntunina sem hún tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="016a8-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="016a8-105">Á sama hátt og uppfærsluferli reiknings er uppfærsla fjárhagsfærslunnar, er uppfærsluferli fylgiseðils efnisleg uppfærsla birgðafærslunnar, sem þýðir að það framkvæmir breytingarnar á birgðunum.</span><span class="sxs-lookup"><span data-stu-id="016a8-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="016a8-106">Þegar um er að ræða skil, eru skrefin sem hafa verið úthlutuð fyrir ráðstöfunaraðgerð innleidd á meðan á fylgiseðilsuppfærslu stendur.</span><span class="sxs-lookup"><span data-stu-id="016a8-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="016a8-107">Hægt er að vinna fylgiseðilsuppfærslu í annað hvort  vörukomubók eða skilapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="016a8-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="016a8-108">Hluti ferlisins við bókun fylgiseðla er að hægt sé að tengja tilvísunarnúmer fylgiseðils úr sendingarskjölum viðskiptavinar við pöntunarlínur.</span><span class="sxs-lookup"><span data-stu-id="016a8-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="016a8-109">Þessi tenging er valfrjáls og aðeins til tilvísunar.</span><span class="sxs-lookup"><span data-stu-id="016a8-109">This association is optional and for reference only.</span></span> <span data-ttu-id="016a8-110">Hún býr ekki til neinar færsluuppfærslur.</span><span class="sxs-lookup"><span data-stu-id="016a8-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="016a8-111">Ef allar væntanlegar skilavörur hafa ekki skilað sér skaltu hafa aðeins það magn með sem hefur verið tekið á móti í uppfærslu fylgiseðlar.</span><span class="sxs-lookup"><span data-stu-id="016a8-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="016a8-112">Skildu eftir vörurnar sem eftir eru af pöntuninni þar til afgangurinn af skilasendingunni hefur skilað sér.</span><span class="sxs-lookup"><span data-stu-id="016a8-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="016a8-113">Ef hlutur er sendur frá biðgeymslu til „Afhendingar- og móttökudeildar“, svo sem þegar eftirlitsaðili biðgeymslunnar veit ekki hvar á að geyma hlutinn í birgðum, verður að uppfæra viðeigandi fylgiseðil til að skrá rétt og bregðast við ráðstöfunarkóðanum sem er tilgreindur vegna biðgeymslunnar.</span><span class="sxs-lookup"><span data-stu-id="016a8-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="016a8-114">Þegar þú uppfærir fylgiseðil fyrir skilavöru sem er frá sölusamningi er skuldbinding sölusamningsins fyrir vöruna sjálfkrafa uppfærð til að endurspegla breytinguna á magninu eða upphæðinni.</span><span class="sxs-lookup"><span data-stu-id="016a8-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="016a8-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="016a8-115">See also</span></span>

[<span data-ttu-id="016a8-116">Framkvæma uppfærslur á reikningi vegna skila</span><span class="sxs-lookup"><span data-stu-id="016a8-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


