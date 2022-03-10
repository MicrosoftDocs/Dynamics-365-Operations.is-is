---
title: Hætta við vinnu í vörugeymslu fyrir meðhöndlun frávika
description: Þetta efnisatriði lýsir virkni Hætta við vinnu sem gerir vöruhússtjórum kleift að meðhöndla lokaða vinnu.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: af0c147eefbfe22cb6b6d531f514e6f293d66689
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572410"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Hætta við vinnu í vörugeymslu fyrir meðhöndlun frávika

[!include [banner](../includes/banner.md)]

Virknin Hætta við vinnu í Microsoft Dynamics 365 Supply Chain Management leyfir stjórnanda að hætta við tiltekna vöruhúsavinnu sem er í gangi en henni er lokað af kerfinu eða ekki hægt að ljúka því vegna sérstakra aðstæðna. Þessi virkni er aðlaðandi og öruggur valkostur við SQL leiðréttingarforskriftir sem laga ósamræmd gögn. En þó að þessara forskrifta sé venjulega krafist af fagfólki í upplýsingatækni, þá geta notendur í fyrirtækinu notað virknina Hætta við vinnu sem hafa stjórnunarréttindi.

Þú getur fengið aðgang að virkni Hætta við vinnu í **Vöruhúsastjórnun** \> **Reglubundin verkefni** \> **Hreinsið upp \> Hætt við vinnu**. Í valmyndinni **Hætta við vinnu** tilgreinirðu vinnukenni sem á að hætta við og veldu síðan **Í lagi**.

## <a name="warehouse-work-that-can-be-canceled"></a>Vöruhúsavinnsla sem hægt er að hætta við

Meðan á vöruhússaðgerðum stendur gæti starfskraftur lent í aðstæðum þar sem viðkomandi hefur skráð magn sem tiltekið af geymslustað yfir á notendastað sinn, en þá getur viðkomandi ekki skráð söluaðgerðina. Ósamræmd gögn um vöruhús eru oft, en ekki alltaf, ástæðan fyrir því að vinna er lokuð.

Ólíkt venjulegri Hætta við virkni sem hægt er að nálgast með því að nota hnappinn **Hætta við** á vinnuhausnum krefst virknin Hætta við vinnu þess ekki að síðasta vinnulínan sé vinnulína af gerðinni **tiltekt**. Með öðrum orðum, fyrir virkni Hætta við vinnu, er hægt að keyra afbókunarrök jafnvel þótt vörumagn á vinnulínu sé á notendastað.

> [!NOTE]
> Fyrir vinnu sem verður að hætta við af rekstrarástæðum verða notendur vöruhúss að halda áfram að nota venjulegu virknina Hætta við á vinnusíðunni.

Aðeins er hægt að hætta við vinnu af gerðinni **Sala**, **Flutningsútgáfa**, **Tiltekt hráefnis** eða **Áfylling** með því að nota virknina Hætta við vinnu. Afturköllunarrök verða ekki keyrð fyrir frátektarvinnu frysts hráefnis eða vinnu sem hægt er að hætta við með því að nota venjulega Hætta við virkni (sjá fyrri athugasemd).

Til að opna verkið hættir kerfið öllum vinnulínum sem eftir eru og lagfærir vöruhúsgögnin sem eru tengd vinnukenninu sem notandinn tilgreindi. Allar venjulegar aðgerðir meðhöndlunar í vöruhúsi sem fela í sér vörumagn sem verða fyrir áhrifum geta síðan haldið áfram.

Til að setja vöruna á tiltekinn stað eftir að vinnunni er aflýst, verður notandinn að nota birgðahreyfingu eða magnleiðréttingaraðgerð í fartæki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]