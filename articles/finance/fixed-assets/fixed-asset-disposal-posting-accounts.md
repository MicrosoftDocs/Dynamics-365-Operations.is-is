---
title: Bókunarlyklar eignaafskráningar
description: Þetta efnisatriði útskýrir hvernig á að setja upp almenna bókunarreikninga til að losna við eignir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a46125dbe5262ba388e3958ea452975a98243f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187154"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="e7749-103">Bókunarlyklar eignaafskráningar</span><span class="sxs-lookup"><span data-stu-id="e7749-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7749-104">Þetta efnisatriði útskýrir hvernig á að setja upp almenna bókunarreikninga til að losna við eignir.</span><span class="sxs-lookup"><span data-stu-id="e7749-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="e7749-105">Á síðunni Bókunarreglur eigna, veljið Afskráning - sala og afskráning - rýrnun í flýtiflipanum Fjárhagslykill, til að setja upp bókanir í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="e7749-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="e7749-106">Fyrir báðar færslugerðirnar fjárhagslykil tekjufærður losunarvirði eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="e7749-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="e7749-107">Skuldfærslan er bókuð á mótlykil, sem gæti t.d. bankareikning.</span><span class="sxs-lookup"><span data-stu-id="e7749-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="e7749-108">Ef eign er seld á viðskiptavin, er viðskiptavinalykillinn notaður frekar en mótlykillinn.</span><span class="sxs-lookup"><span data-stu-id="e7749-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="e7749-109">Smelltu á Afskráning og smelltu síðan á Sala eða Rýrnun og settu síðan upp sundurliðaða lykla til að bakfæra bókað nettóvirði af eign.</span><span class="sxs-lookup"><span data-stu-id="e7749-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="e7749-110">Einnig er hægt að færa upplýsingar inn á svæðinu Bókunargildi og Sölugildi á síðunni Losunarfæribreytur.</span><span class="sxs-lookup"><span data-stu-id="e7749-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="e7749-111">Losunarfærslan fyrir eign í lágvirðishópi minnkar bókað nettóvirði lágvirðishópsins einungis eftir losun upphæðar.</span><span class="sxs-lookup"><span data-stu-id="e7749-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="e7749-112">Hins vegar verður bókað nettóvirði eignar minnkað í núll þegar sala vöru er hærri en bókað nettógildi lágvirðishóps.</span><span class="sxs-lookup"><span data-stu-id="e7749-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>




