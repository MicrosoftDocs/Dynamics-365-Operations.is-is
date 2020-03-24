---
title: Breyta afhendingarmáta í POS
description: Þetta efni lýsir því hvernig á að stilla og nota breytingamáta fyrir afhendingu í POS.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 26e798c664844b575de6f019ad8f5349ed92be98
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/10/2020
ms.locfileid: "3114405"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="c4523-103">Breyta afhendingarmáta í POS</span><span class="sxs-lookup"><span data-stu-id="c4523-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c4523-104">Þetta efnisatriði lýsir því hvernig á að setja upp og nota „breyting á afhendingarstillingu“ virkni í sölustað (POS) umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="c4523-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="c4523-105">Í Dynamics 365 Commerce útgáfur 10.0.10 og nýrri, **Breyta afhendingaraðferð** aðgerð (647) er tiltæk til að bæta við POS skjáuppsetninguna þína.</span><span class="sxs-lookup"><span data-stu-id="c4523-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="c4523-106">Breytingarháttur afhendingaraðgerðar veitir þér möguleika á að breyta afhendingarháttum fyrir eina eða fleiri sölulínur fyrir sendingu í POS viðskiptunum.</span><span class="sxs-lookup"><span data-stu-id="c4523-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="c4523-107">Í fyrri útgáfum af viðskiptum varstu að fara í gegnum það í heild sinni **Senda allt** eða **Senda valið** stillingar streyma ef þú vilt breyta afhendingarháttum á núverandi línu sem var stillt til sendingar.</span><span class="sxs-lookup"><span data-stu-id="c4523-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="c4523-108">Þetta ferli var tímafrekt og gæti valdið slysni breytingum á uppruna afhendingar eða afhendingardögum fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="c4523-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="c4523-109">Hin nýja virkni býður upp á aðra aðferð til að uppfæra skilvirkni á þessum sölulínum á skilvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="c4523-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="c4523-110">Nánari upplýsingar um hvernig á að bæta aðgerð við hnapp á POS hnapparitinu, sjá [Skjáuppsetning fyrir sölustað](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="c4523-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="c4523-111">Eftir að þessi aðgerð er stillt í POS, þegar þú velur **Breyta afhendingaraðferð**, verður þér kynnt listasíða sem gerir þér kleift að velja línurnar í viðskiptunum sem þú vilt breyta afhendingarháttum fyrir.</span><span class="sxs-lookup"><span data-stu-id="c4523-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="c4523-112">Þú getur valið nokkrar eða allar línurnar, eða lokað án þess að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="c4523-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="c4523-113">Sölulínurnar sem áður voru stilltar til sendingar eru einu línurnar á listanum sem þú getur breytt.</span><span class="sxs-lookup"><span data-stu-id="c4523-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="c4523-114">Ef þú vilt breyta línu sem er ætluð til afhendingar eða flutnings í skip, verður þú að nota **Senda allt** eða **Senda valið** aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="c4523-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="c4523-115">Hins vegar, ef þú vilt breyta línu sem er tilgreind sem sending í pallbíll eða flutning, verður þú að nota **Sækja allt**, **Sækja valið**, **Framkvæma allt** eða **Framkvæma valið** aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="c4523-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="c4523-116">Eftir að þú hefur valið línurnar sem þú vilt breyta, smelltu á **Breyta afhendingaraðferð** að vera beðinn um að velja valkosti afhendingarstillingar.</span><span class="sxs-lookup"><span data-stu-id="c4523-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="c4523-117">Ef þú valdir margar línur til að breyta, birtir POS aðeins afhendingaraðferðir sem hafa verið stilltir sem leyfilegt fyrir allar valdar vörur.</span><span class="sxs-lookup"><span data-stu-id="c4523-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="c4523-118">Hægt er að stilla afhendingaraðferðir til að styðja við tilteknar vörur og afhendingarföng.</span><span class="sxs-lookup"><span data-stu-id="c4523-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="c4523-119">Ef það er til staðar afhendingarstaður sem er ásættanlegur fyrir eina vöru- og heimilisfangasamsetningu en er ekki ásættanlegur fyrir aðra valda vöru- og heimilisfangasamsetningu, er afhendingarháttur ekki tiltækur.</span><span class="sxs-lookup"><span data-stu-id="c4523-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="c4523-120">Þú gætir þurft að velja línur einn í einu og breyta afhendingarháttum fyrir hverja línu fyrir sig ef þú vilt velja afhendingaraðferð fyrir eina vöru sem er ekki studd af annarri vöru.</span><span class="sxs-lookup"><span data-stu-id="c4523-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="c4523-121">Eftir að þú hefur valið nýja afhendingarstillingu birtist viðskiptasíðan.</span><span class="sxs-lookup"><span data-stu-id="c4523-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="c4523-122">Til að skoða nýju afhendingarstillingarnar þínar skaltu velja flipann **Afhending** á færslulistanum.</span><span class="sxs-lookup"><span data-stu-id="c4523-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>   
