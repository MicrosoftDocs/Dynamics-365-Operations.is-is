---
title: Mælieiningu og birgðareglur
description: Þessi grein lýsir því hvernig sjálfgefnar einingar, röðunarflokkar eininga og umreikningur eininga eru notaðar í vöruhúsaferlum.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aee5885da05b3ae46b8c4c2e0eb143708b921817
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993829"
---
# <a name="unit-of-measure-and-stocking-policies"></a>Mælieiningu og birgðareglur

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig sjálfgefnar einingar, röðunarflokkar eininga og umreikningur eininga eru notaðar í vöruhúsaferlum.

Eining röðunarflokks tilgreinir röð einingar sem hægt er að nota í vöruhúsaaðgerðir. Þær eru stofnaðar á síðunni **Röðunarflokkar eininga**. Röðin sýnir sambandið á milli ýmissa eininga. Til dæmis þú geymir bretti sem innihalda reiti sem innihalda einstök stykki af vörum. Í þessu tilfelli verður að veita þriggja ólíkra eininga og röklega röðun laga. Röðunarflokkar eininga gerir þér mögulegt að skilgreina reglur fyrir flokkun á númeraplötum, og sjálfgefnar einingar sem á að nota fyrir ýmis vöruhúsaferli . Þessi skrá á bæði við ítarlega vöruhúsalausn sem er tiltæk í vöruhúsakerfi og einfaldari vöruhúsalausn sem er tiltæk í birgðastjórnun.

## <a name="unit-sequence-groups-for-released-products"></a>röðunarflokkar eininga fyrir útgefnar afurðir
Ef óskað er að nota útgefin afurð í vinnuferlum vöruhúss, þarf að úthluta röðunarflokki eininga til þeirra. Ef að þú villuleitar afurð sem tengist geymsluvíddaflokk, og **Nota vöruhúsakerfisferli** valkosturinn fyrir  geymsluvíddaflokkinn er stillt á **Já**, færðu villuskilaboð ef Auðkenni röðunarflokks einingar er ekki skilgreind fyrir vöruna. Ef röðunarflokks einingarinnar sem þú ert að nota inniheldur margar línur (og þar af leiðandi margar einingar), verður að setja upp einingaumreikning milli eininga. Þessari uppsetningu er lokið á síðunni **Umreikningur eininga**. Lægsta eining röðunarflokks sem hægt er að tengja við útgefna afurð verður að samsvara birgðaeiningunni sem er skilgreint til úr samsvarandi afurð. Birgðaeiningin er einingin sem er notað fyrir grunnútreikning á birgðum á lager. Einnig er hægt að setja upp mælieiningarumreikninga fyrir afurðarafbrigði fyrir afurðarsniðmát með því að nota í **Virkja umreikning mælieiningar** valkost.

## <a name="license-plate-grouping"></a>Flokkun númeraplötu
Hægt er að tilgreina hvort flokka skuli innhreyfingar sem eru meiri en tiltekin eining á eina númeraplötu eða skipta þeim á númeraplötu fyrir hverja einingu. Til að setja upp þessa hegðun, notaðu **flokkun númeraplötu** valkostinn á í **Línuupplýsingar** flipanum á **röðunarflokkur Einingar** síðu. Ef óskað er að nota flokkun númeraplötu þegar verk er unnið með fartæki, þarf að veja **númeraplötu flokk** valkost á **fartæki** valmyndaratriði. Til dæmis þú ert að nota fartæki til að skrá vöru sem tengist röðunarflokks einingarinnar sem er með tvær línur. Fyrsta línan er fyrir Stykki, og **flokkun númeraplötu** valkostur er stilltur á **Já**. Önnur línan er fyrir vörubrettaeiningu, og **flokkun númeraplötu** valkostur er stilltur á **Nei**. Í þessu tilfelli getur kerfið sjálfvirkt leiðbeina fyrir skipti og stofnun númeraplatna á 100 stykki.

## <a name="units-for-cycle-counting"></a>einingar fyrir reglulega talningu
Til að skilgreina hvaða einingar skuli notað sem hluti af reglulega talningaferli skal velja **Nota einingu við reglulega talningu** valkostinn á í **röðunarflokka Eininga** síðu. Hægt er að velja mest fjórar einingar í röð. Ef valið er fleiri en fjórir einingar, munu aukalegu einingarnar ekki verða sýnd í fartækinu.

## <a name="default-units-for-mobile-device-receiving-processes"></a>sjálfgefnar einingar fyrir innhreyfingaferli fartækis
Til að setja sjálfgefin einingarnar sem nota á fyrir móttökuferli í fartækjum, skal virkja **Sjálfgefin eining fyrir innkaup og flutninga** og **Sjálfgefin framleiðslueining** kosturinn á **röðunarflokka Eininga** síðu. Til dæmis er hægt að tilgreina að, sjálfgefið, eigi kerfið að nota Brettamagn þegar birgðir á lager fyrir fyrir innkaupapöntun er móttekin með farsíma, en a' lagergeymslueining ætti að vera Stykki. Til að fá umreikning fyrir þann fjölda stykkja sem hvert bretti inniheldur, verður að skilgreina einingaumreikning, eins og 100 stykki = 1 PL.

## <a name="default-order-settings"></a>Sjálfgefnar pöntunarstillingar
Sem hluti af stofnun útgefnar afurðir, verður að velja sjálfgefnar einingar fyrir innkaup, sölu og birgðir til að vinna ýmsar pantanir. Hægt er að stilla sjálfgefið eininga og magn fyrir mismunandi upprunaskjöl með því að nota í **Sjálfgefnar pöntunarstillingar** og **Pöntunarstillingar tengdar staðsetningum** síður. Hægt er að opna þessar síður frá á **Útgefnum afurðum** síðu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]