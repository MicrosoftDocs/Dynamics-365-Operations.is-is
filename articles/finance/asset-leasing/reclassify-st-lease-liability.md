---
title: Endurflokka skammtímahluta leiguskuldbindingar
description: Þessi grein útskýrir hvernig á að stofna mánaðarlega færslubókarfærslu til að endurflokka hluta af leiguskuldbindingunni sem skammtíma.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c7c3f86aa5d24e9aeed89526a4b7317699e9a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886343"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Endurflokka skammtímahluta leiguskuldbindingar

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að stofna mánaðarlega færslubókarfærslu til að endurflokka hluta af leiguskuldbindingunni sem skammtíma. Þegar áætlunin sem er valin í runuvinnslunni er **endurflokkun skammtíma leiguskuldbindingar** er færslubókarfærsla stofnuð. Þessi færsla er notuð til að bóka núverandi hluta leiguskuldarinnar á síðasta degi mánaðarins. Á sama tíma er bakfærsla bókuð frá fyrsta degi næsta mánaðar.

Skammtímahluti leiguskuldbindingar er sýndur í afskriftaráætlun skuldar. Þegar færslubókarfærslan er bókuð verður dálkurinn **Endurflokkunarbók skuldar stofnuð** tiltækur og færslubókarkennið er einnig fyllt út í áætluninni.

Til að stofna og bóka færslu í endurflokkunarbók skammtímaskuldar skal fylgja þessum skrefum.

1. Opnið **Eignarleiga \> Reglubundið \> Stofnun runubókar**.
2. Í svarglugganum **Stofnun runubókar**, á svæðinu **Velja áætlun** skal velja **Endurflokkun skuldbindingar skammtímaleigu**.
3. Í reitnum **Leigusamningsflokkur** skal velja leigusamningsflokk. Einnig er hægt að velja bókarkennið í reitnum **Bókarkenni** .
4. Kveikja skal á færibreytunni **Bóka**. Einnig er hægt að stofna færsluna en ekki bóka hana með því að hafa slökkt á þessari færibreytu.
5. Veljið **Í lagi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
