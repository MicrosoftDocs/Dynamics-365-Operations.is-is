---
title: "Fastir bókunarlyklar eignakaupa"
description: "Þessi grein útskýrir hvernig á að setja upp almenna bókunarreikninga til eignast eignir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: bd7f89a7dbf8aa87794f8d4b57bda54433e5feb1
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-acquisition-posting-accounts"></a>Fastir bókunarlyklar eignakaupa

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir hvernig á að setja upp almenna bókunarreikninga til eignast eignir.

Lyklar sem eru notaðir til að bóka eignakaup geta verið mismunandi, eftir því hvaða aðferð er notuð til að kaupa eignir. Á síðunni bókunarreglur eigna, í Fjárhagsreiknings flipa, veljið Kaup og Leiðrétting kaupa til að setja upp eignalykla til að bóka í fjárhaginn. 

Í færslubókum og á innkaupapöntunum er Fjárhagsreikningur oftast efnahagslykillinn þar sem kaupvirði nýju eignarinnar er skuldfært. Þessi lykill getur ekki birst í færslubók og er ekki hægt að skipta út í færslum. 

Mótlykill er líka efnahagslykill. Í almennu færslubókinni og í eignabókinni er þessi lykill oft bankareikningurinn sem er notaður til að greiða fyrir kaup eignarinnar. Mótlykillinn er sjálfgefinn lykill sem er stungið upp á í færslubókunum. Hægt er að breyta þessu í færslubókinni í einhvern annan reikning úr bókhaldslykli eða í lánardrottnalykil, ef eignin var keypt af lánardrottni. 

Þegar reikningabók eða innkaupapöntun í viðskiptaskuldum eru notuð fyrir eignakaup, er mótlyklinum fyrir eignafærsluna skipt úr fyrir lánardrottnareikninginn sem er valinn fyrir færsluna.

Fyrir kaup bókuð með því að nota færslubókina eignabirgðir í fjárhagnum er eignin ekki keypt af utanaðkomandi aðila heldur færð úr eigin birgðum fyrirtækisins. Þess vegna, mótlykill er lykill birgðaúthreyfingar fyrir birgðavara í birgðastjórnun.

Frekari upplýsingar eru í [Kaupa eignir með innkaupum](acquire-assets-procurement.md).




