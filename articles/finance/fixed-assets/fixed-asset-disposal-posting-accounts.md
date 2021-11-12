---
title: Bókunarlyklar eignaafskráningar
description: Þetta efnisatriði útskýrir hvernig á að setja upp almenna bókunarreikninga til að losna við eignir.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c82cb8b82f2cc8424675f76c68613a2b5aa76745
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675519"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>Bókunarlyklar eignaafskráningar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp almenna bókunarreikninga þegar losna á við eignir.

Til að setja upp almenna bókunarreikninga til að nota þegar losna á við eign skal velja **Losun - sala** og **Losun - rýrnun** á flýtiflipanum **Fjárhagslyklar** á síðunni **Bókunarreglur eigna**.

Fyrir báðar færslugerðirnar (losnað við eign með sölu eða rýrnun) er fjárhagslykillinn kreditfærður fyrir losunarvirði eignarinnar. Debetfærslan er bókuð á mótlykil sem gæti verið bankareikningur (sem dæmi). Ef eign er seld á viðskiptavin, er viðskiptavinalykillinn notaður frekar en mótlykillinn. Frekari upplýsingar er að finna í [Losa eign sem rýrnun](dispose-of-a-fixed-asset-as-scrap.md).

Smelltu á **Afskráning** og smelltu síðan á **Sala** eða **Rýrnun** og settu síðan upp sundurliðaða lykla til að bakfæra bókað nettóvirði af eign. Einnig er hægt að færa upplýsingar inn á svæðinu **Bókunargildi** og **Sölugildi** á síðunni **Losunarfæribreytur**. 

Losunarfærslan fyrir eign í lágvirðishópi minnkar bókað nettóvirði lágvirðishópsins einungis eftir losun upphæðar. Hins vegar verður bókað nettóvirði eignar minnkað í núll þegar sala vöru er hærri en bókað nettógildi lágvirðishóps.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
