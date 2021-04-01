---
title: Hlutastaðsetning reglulegrar talningar
description: Áætlanir um reglulega talningu stýra raunverulegum talningaraðgerðum. Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abafe64a17b7b284e5e045da33bb15cf3c42800b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234682"
---
# <a name="partial-location-cycle-counting"></a>Hlutastaðsetning reglulegrar talningar

[!include [banner](../includes/banner.md)]

Áætlanir um reglulega talningu stýra raunverulegum talningaraðgerðum. Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar.

Með því að nota áætlanir fyrir reglulega talningu, er hægt að stýra raunverulegum talningaraðgerðum. Hægt er að biðja um að aðeins tilteknar afurðir og afurðaafbrigði séu talin í stað þess að allar efnislegar lagerbirgðir í staðsetningu séu taldar. Með því að sía tilteknar vörur getur vöruhúsastjóri dregið úr kostnaði við endurskoðun, forðast samstæðumistök og sparað tíma.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Skilgreining hlutastaðsetningar reglulegrar talningar

Þegar þú notast við vinnuferla vöruhúss í talningaraðgerðum er vinnuhaus stofnaður fyrir hverja staðsetningu. Þegar þú skilgreinir áætlun fyrir reglulega talningu, getur þú notað fyrirspurnina **Velja staðsetningar** til að takmarka þá talningarvinnu sem stofnað er til. Þegar afurðir fyrir áætlun reglulegrar talningar eru valdar er bæði hægt að velja fyrirspurnir um afurð og afurðarafbirgði til að fínstilla hvað er talið.

Þú getur tengt **vinnusniðmát** við áætlun fyrir reglulega talningu til að skilgreina hvernig regluleg talningarvinna skal stofnuð. Vísað er beint í vinnusniðmát fyrir talningaraðgerðir úr áætlun fyrir reglulega talningu.

Þegar upplýsingar um vinnusniðmát eru skilgreindar getur þú notað valmöguleikann **Vinnulínuskil** til að tilgreina hvort talningarvinnulínurnar eigi að flokkast eftir vörunúmeri eða afurðarafbrigðisnúmeri. Þessi uppsetning er nauðsynleg viljir þú aðeins telja efnislegar lagerbirgðir fyrir tilteknar afurðir í staðsetningu. Vinnulínur fyrir talningarvinnu sem eru stofnaðar munu hafa að geyma þær upplýsingar sem þú skilgreinir hér og stýrðri talningarvinnu er stjórnað á grundvelli þessa stigs.

Ef þú tengir áætlanir fyrir reglulega talningu við vinnusniðmát með því að nota valmöguleikann **Vinnulínuskil** er reiturinn **Regluleg talning að hluta** valinn fyrir reglulega talningarvinnu sem stofnuð er og margar vinnulínur fyrir reglulega talningu eru stofnaðar á grundvelli skilgreiningarinnar á vinnusniðmátinu.

Áður en vinna við reglulega talningu að hluta getur farið í ferli verður þú að minnsta kosti að velja **Birta vörunúmer** fyrir valmyndaratriði fartækja sem hluta af uppsetningu reglulegrar talningar. Starfsmaður í vöruhúsi verður beðinn að skrá aðeins talningarupplýsingar sem tengjast talningarlínum (vörunúmer og afurðarvíddir). Allar aðrar efnislegar lagerbirgðir verða hunsaðar fyrir þetta talningarferli.

Fyrir hlutatalningu uppfærist ekki **Síðasta reglulega talning** dagsetning/tími fyrir staðsetninguna, jafnvel þó svo að allar vörur í birgðum á staðsetningunni séu taldar. Hlutatalning telur ekki með færibreytuna **Dagar á milli reglulegrar talninga** á síðunni **Áætlanir um reglulega talningu**. Hlutatalning styður ekki samtímis talningar á mörgum vörum á sama stað. Hlutatalning getur leitt til þess að sama staðsetning sé talin mörgum sinnum fyrir vöru þegar **Vinna úr áætlun um reglulega talningu** er keyrð. Til að koma í veg fyrir þessar aðstæður skal tilgreina síur í reitnum **Velja staðsetningar**.

> [!NOTE]
> Vöruhúsaforritið gefur ekki upp -hnappinn **Bæta við númeraplötu eða vöru** þegar regluleg talning að hluta er notuð.

## <a name="example"></a>Dæmi

Í þessu dæmi þarf aðeins að telja vörunúmer A0001 í vöruhúsi 61.

1. Nýtt vinnusniðmát fyrir reglulega talningu er stofnað. Valmöguleikinn **Vinnulínuskil** er notaður til að flokka talningarlínur eftir vörunúmerum. Þar af leiðandi mun sú reglulega talningarvinna sem stofnuð er hafa línur á hvert vörunúmer. Einnig er hægt að flokka línurnar eftir afurðarafbrigðisnúmeri.
1. Ný áætlun fyrir reglulega talningu er stofnuð sem vísar í vinnusniðmátið sem var verið að stofna. Áætlun fyrir reglulega talningu inniheldur allar staðsetningar í vöruhúsi 61 (fyrirspurnin **Velja staðsetningar**) sem geyma birgðir fyrir vörunúmer A0001. Val á tilteknum vörum er skilgreint í hlutanum **Afurðarval fyrir reglulega talningu**.
1. Hægt er að velja vörur fyrir reglulega talningu með því að stilla **Tómar staðsetningar** reitinn á **Taka ekki með tómar**. Þegar regluleg talning er framkvæmt er hlutatalning fyrir vörunúmer A0001 stofnuð. Hægt er að framkvæma raunverulegt talningarferli með því að nota valmyndaratriði í fartæki fyrir stýrða reglulega talningu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Regluleg talning](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]