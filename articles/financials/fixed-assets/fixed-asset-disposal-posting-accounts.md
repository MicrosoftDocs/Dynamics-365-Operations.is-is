---
title: "Afskráning eigna, bókunarlykill"
description: "Þessi grein útskýrir hvernig á að setja upp almenna bókunarreikninga til að losna við eignir."
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 0129eae177d44100b09c2b7bce553dd5bde5ce0c
ms.contentlocale: is-is
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="1157d-103">Afskráning eigna, bókunarlykill</span><span class="sxs-lookup"><span data-stu-id="1157d-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1157d-104">Þessi grein útskýrir hvernig á að setja upp almenna bókunarreikninga til að losna við eignir.</span><span class="sxs-lookup"><span data-stu-id="1157d-104">This article explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="1157d-105">Á síðunni Bókunarreglur eigna, veljið Afskráning - sala og afskráning - rýrnun í flýtiflipanum Fjárhagslykill, til að setja upp bókanir í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="1157d-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="1157d-106">Fyrir báðar færslugerðirnar fjárhagslykil tekjufærður losunarvirði eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="1157d-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="1157d-107">Skuldfærslan er bókuð á mótlykil, sem gæti t.d. bankareikning.</span><span class="sxs-lookup"><span data-stu-id="1157d-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="1157d-108">Ef eign er seld á viðskiptavin, er viðskiptavinalykillinn notaður frekar en mótlykillinn.</span><span class="sxs-lookup"><span data-stu-id="1157d-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="1157d-109">Smelltu á Afskráning og smelltu síðan á Sala eða Rýrnun og settu síðan upp sundurliðaða lykla til að bakfæra bókað nettóvirði af eign.</span><span class="sxs-lookup"><span data-stu-id="1157d-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="1157d-110">Einnig er hægt að færa upplýsingar inn á svæðinu Bókunargildi og Sölugildi á síðunni Losunarfæribreytur.</span><span class="sxs-lookup"><span data-stu-id="1157d-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="1157d-111">Losunarfærslan fyrir eign í lágvirðishópi minnkar bókað nettóvirði lágvirðishópsins einungis eftir losun upphæðar.</span><span class="sxs-lookup"><span data-stu-id="1157d-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="1157d-112">Hins vegar verður bókað nettóvirði eignar minnkað í núll þegar sala vöru er hærri en bókað nettógildi lágvirðishóps.</span><span class="sxs-lookup"><span data-stu-id="1157d-112">However, when the sale of an asset is exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






