---
title: "Hlutastaðsetning reglulegrar talningar"
description: "Áætlanir um reglulega talningu stýra raunverulegum talningaraðgerðum. Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 856ac2a61bc06a772b586a0cf77496fc360db623
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="partial-location-cycle-counting"></a>Hlutastaðsetning reglulegrar talningar

[!include[banner](../includes/banner.md)]


Áætlanir um reglulega talningu stýra raunverulegum talningaraðgerðum. Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar.

Með því að nota áætlanir fyrir reglulega talningu, er hægt að stýra raunverulegum talningaraðgerðum. Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar. Með því að sía tilteknar vörur getur vöruhúsastjóri dregið úr kostnaði við endurskoðun, forðast samstæðumistök og sparað tíma.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Skilgreining hlutastaðsetningar reglulegrar talningar
Þegar þú notast við vinnuferla vöruhúss í talningaraðgerðum er vinnuhaus stofnaður fyrir hverja staðsetningu. Þegar þú skilgreinir áætlun fyrir reglulega talningu, getur þú notað fyrirspurnina **Velja staðsetningar** til að takmarka þá talningarvinnu sem stofnað er til. Þegar afurðir fyrir áætlun reglulegrar talningar eru valdar er bæði hægt að velja fyrirspurnir um afurð og afurðarafbirgði til að fínstilla hvað er talið. 

Þú getur tengt **vinnusniðmát** við áætlun fyrir reglulega talningu til að skilgreina hvernig regluleg talningarvinna skal stofnuð. Vísað er beint í vinnusniðmát fyrir talningaraðgerðir úr áætlun fyrir reglulega talningu. 

Þegar upplýsingar um vinnusniðmát eru skilgreindar getur þú notað valmöguleikann **Vinnulínuskil** til að tilgreina hvort talningarvinnulínurnar eigi að flokkast eftir vörunúmeri eða afurðarafbrigðisnúmeri. Þessi uppsetning er nauðsynleg viljir þú aðeins telja efnislegar lagerbirgðir fyrir tilteknar afurðir í staðsetningu. Vinnulínur fyrir talningarvinnu sem eru stofnaðar munu hafa að geyma þær upplýsingar sem þú skilgreinir hér og stýrðri talningarvinnu er stjórnað á grundvelli þessa stigs. 

Ef þú tengir áætlanir fyrir reglulega talningu við vinnusniðmát með því að nota valmöguleikann **Vinnulínuskil** er reiturinn **Regluleg talning að hluta** valinn fyrir reglulega talningarvinnu sem stofnuð er og margar vinnulínur fyrir reglulega talningu eru stofnaðar á grundvelli skilgreiningarinnar á vinnusniðmátinu. 

Áður en vinna við reglulega talningu að hluta getur farið í ferli verður þú að minnsta kosti að velja **Birta vörunúmer** fyrir valmyndaratriði fartækja sem hluta af uppsetningu reglulegrar talningar. Starfsmaður í vöruhúsi verður beðinn að skrá aðeins talningarupplýsingar sem tengjast talningarlínum (vörunúmer og afurðarvíddir). Allar aðrar efnislegar lagerbirgðir verða hunsaðar fyrir þetta talningarferli. 

Á meðan regluleg talning að hluta fer fram uppfærist dagsetning/tími í **Síðasta reglulega talning** ekki fyrir staðsetninguna.

## <a name="example"></a>Dæmi
Í þessu dæmi þarf aðeins að telja vörunúmer A0001 í vöruhúsi 61.

1.  Nýtt vinnusniðmát fyrir reglulega talningu er stofnað. Valmöguleikinn **Vinnulínuskil** er notaður til að flokka talningarlínur eftir vörunúmerum. Þar af leiðandi mun sú reglulega talningarvinna sem stofnuð er hafa línur á hvert vörunúmer. Einnig er hægt að flokka línurnar eftir afurðarafbrigðisnúmeri.
2.  Ný áætlun fyrir reglulega talningu er stofnuð sem vísar í vinnusniðmátið sem var verið að stofna. Áætlun fyrir reglulega talningu inniheldur allar staðsetningar í vöruhúsi 61 (fyrirspurnin **Velja staðsetningar**) sem geyma birgðir fyrir vörunúmer A0001. Val á tilteknum vörum er skilgreint í hlutanum **Afurðarval fyrir reglulega talningu**.
3.  Hægt er að velja afurðir fyrir áætlanir fyrir reglulega talningu með því að stilla reitinn **Auðar staðsetningar** á **Útiloka tómar**. Þegar áætlun fyrir reglulega talningu er komin í ferli er regluleg talningarvinna fyrir vörunúmer A0001 stofnuð. Hægt er að framkvæma raunverulegt talningarferli með því að nota valmyndaratriði í fartæki fyrir stýrða reglulega talningu.



<a name="see-also"></a>Sjá einnig
--------

[Regluleg talning](cycle-counting.md)

