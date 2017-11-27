---
title: "Bókunarlyklar eignaafskráningar"
description: "Þetta efnisatriði útskýrir hvernig á að setja upp almenna bókunarreikninga til að losna við eignir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bfed7657649f938c3d436468891d40d4194b555d
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="d897f-103">Bókunarlyklar eignaafskráningar</span><span class="sxs-lookup"><span data-stu-id="d897f-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d897f-104">Þetta efnisatriði útskýrir hvernig á að setja upp almenna bókunarreikninga til að losna við eignir.</span><span class="sxs-lookup"><span data-stu-id="d897f-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="d897f-105">Á síðunni Bókunarreglur eigna, veljið Afskráning - sala og afskráning - rýrnun í flýtiflipanum Fjárhagslykill, til að setja upp bókanir í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="d897f-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="d897f-106">Fyrir báðar færslugerðirnar fjárhagslykil tekjufærður losunarvirði eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="d897f-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="d897f-107">Skuldfærslan er bókuð á mótlykil, sem gæti t.d. bankareikning.</span><span class="sxs-lookup"><span data-stu-id="d897f-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="d897f-108">Ef eign er seld á viðskiptavin, er viðskiptavinalykillinn notaður frekar en mótlykillinn.</span><span class="sxs-lookup"><span data-stu-id="d897f-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="d897f-109">Smelltu á Afskráning og smelltu síðan á Sala eða Rýrnun og settu síðan upp sundurliðaða lykla til að bakfæra bókað nettóvirði af eign.</span><span class="sxs-lookup"><span data-stu-id="d897f-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="d897f-110">Einnig er hægt að færa upplýsingar inn á svæðinu Bókunargildi og Sölugildi á síðunni Losunarfæribreytur.</span><span class="sxs-lookup"><span data-stu-id="d897f-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="d897f-111">Losunarfærslan fyrir eign í lágvirðishópi minnkar bókað nettóvirði lágvirðishópsins einungis eftir losun upphæðar.</span><span class="sxs-lookup"><span data-stu-id="d897f-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="d897f-112">Hins vegar verður bókað nettóvirði eignar minnkað í núll þegar sala vöru er hærri en bókað nettógildi lágvirðishóps.</span><span class="sxs-lookup"><span data-stu-id="d897f-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






