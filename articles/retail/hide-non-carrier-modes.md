---
title: Fela afhendingarstillingar utan flutningsaðila fyrir sendingarmöguleikana í POS
description: Þetta efni lýsir stillingarvalkosti sem getur komið í veg fyrir að afhendingarstig utan flutningsaðila birtist fyrir val þegar sendingarpantanir eru búnar til í forritinu sölustaðnum (POS).
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 09ea83b3336b208f8af0a91025c2e6c50d64c385
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659022"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="d4bad-103">Fela afhendingarstillingar utan flutningsaðila fyrir sendingarmöguleikana í POS</span><span class="sxs-lookup"><span data-stu-id="d4bad-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d4bad-104">Þetta efni lýsir stillingarmöguleikum sem er í boði fyrir POS-forritið.</span><span class="sxs-lookup"><span data-stu-id="d4bad-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="d4bad-105">Þessi stillingarmöguleiki breytir hegðun við val á afhendingaraðferð þegar sendingarpantanir eru búnar til í POS.</span><span class="sxs-lookup"><span data-stu-id="d4bad-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="d4bad-106">Þegar notendur stofna sendingarpantanir viðskiptavina í POS geta þeir valið afhendingaraðferð fyrir sendinguna.</span><span class="sxs-lookup"><span data-stu-id="d4bad-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="d4bad-107">Þessi virkni er tiltæk óháð því hvort öll pöntunin er send eða eingöngu valdar línur.</span><span class="sxs-lookup"><span data-stu-id="d4bad-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="d4bad-108">Sjálfgefið er að svarglugginn þar sem afhendingarháttur er valinn sýnir allar gildar afhendingarstillingar fyrir samsetningu rásar, hlutar og afhendingarfangs.</span><span class="sxs-lookup"><span data-stu-id="d4bad-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="d4bad-109">Þessar afhendingaraðferðir eru skilgreindar á síðunni **Afhendingarmátar** í Retail Headquarters (**Sala og markaðsstarf \> Uppsetning \> Dreifing \> Afhendingarmátar**).</span><span class="sxs-lookup"><span data-stu-id="d4bad-109">These modes of delivery are defined on the **Modes of delivery** page in Retail Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="d4bad-110">Afhendingaraðferðir „ekki flutningsaðili“, svo sem **Framkvæma** eða **Pallbíll**, gæti einnig birst fyrir val í valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="d4bad-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="d4bad-111">Hins vegar hefur eiginleika verið bætt við sem gerir þér kleift að fela afhendingaraðferðir án flutningsaðila í valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="d4bad-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="d4bad-112">Til að kveikja á þessum eiginleika, á síðunni **Retail-færibreytur**, á flipanum **Pantanir viðskiptavina**, stillirðu valkostinn **Sýna aðeins valkosti flutningsmáta fyrir skipapantanir** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="d4bad-112">To turn on this feature, on the **Retail parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="d4bad-113">Eftir að þú kveikir á þessari aðgerð og keyrir viðeigandi dreifingarvinnslur til að samstilla upplýsingarnar við gagnagrunn rásarinnar, birtast ekki afhendingarstillingar fyrir flutning fyrir val á meðan á því að búa til sendingarpantanir í POS.</span><span class="sxs-lookup"><span data-stu-id="d4bad-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>