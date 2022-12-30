---
title: Hætta við vinnu í vörugeymslu fyrir meðhöndlun frávika
description: Þessi grein lýsir afturköllunaraðgerð vinnu sem gerir eftirlitsaðilum kleift að meðhöndla útilokaða vinnu.
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
ms.openlocfilehash: b1e2036e4e7a8a47d6df029f285df7aca0fa74e6
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404433"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Hætta við vinnu í vörugeymslu fyrir meðhöndlun frávika

[!include [banner](../includes/banner.md)]

Afturköllunaraðgerð vinnu í Microsoft Dynamics 365 Supply Chain Management gerir stjórnanda kleift að hætta við tiltekna vöruhúsavinnu sem er í gangi, en sem er útilokuð af kerfinu eða er ekki hægt að ljúka vegna óvenjulegra kringumstæðna. Þessi virkni er aðlaðandi og öruggur valkostur við SQL leiðréttingarforskriftir sem laga ósamræmd gögn. Hins vegar er yfirleitt óskað eftir þessum skriftum hjá fagfólki í upplýsingatækni, en stjórnendur í fyrirtækinu geta notað þessa virkni til að hætta við vinnu.

Hægt er að fá aðgang að afturköllunaraðgerð vinnu í **Vöruhúsakerfi** \> **Reglubundin verk** \> **Hreinsa \> Hætta við vinnu**. Í valmyndinni **Hætta við vinnu** tilgreinirðu vinnukenni sem á að hætta við og veldu síðan **Í lagi**.

## <a name="warehouse-work-that-can-be-canceled"></a>Vöruhúsavinnsla sem hægt er að hætta við

Meðan á vöruhússaðgerðum stendur gæti starfskraftur lent í aðstæðum þar sem viðkomandi hefur skráð magn sem tiltekið af geymslustað yfir á notendastað sinn, en þá getur viðkomandi ekki skráð söluaðgerðina. Ósamræmd gögn um vöruhús eru oft, en ekki alltaf, ástæðan fyrir því að vinna er lokuð.

Ólíkt venjulegri afturköllunaraðgerð sem hægt er að opna með því að nota hnappinn **Hætta við** í vinnuhausnum krefst afturköllunaraðgerð vinnu ekki að síðasta lokna vinnulínan sé vinnulína af gerðinni **frágangur**. Þ.e. fyrir afturköllunaraðgerð vinnu er hægt að keyra afturköllunarrök jafnvel þótt vörumagnið í vinnulínu sé í staðsetningu notanda.

> [!NOTE]
> Fyrir vinnu sem þarf að hætta við af rekstrarlegum ástæðum verða starfsmenn vöruhúss að halda áfram að nota venjulega afturköllunaraðgerð á vinnusíðunni.

Aðeins er hægt að hætta við vinnu af gerðinni **Sala**, **Flutningsútgáfa**, **Tiltekt hráefnis** eða **Áfylling** með því að nota afturköllunaraðgerð vinnu. Afturköllunarrökin munu ekki vera keyrð fyrir tiltekt á frosnu hráefni eða vinnu sem hægt er að hætta við með því að nota venjulegu afturköllunaraðgerðina (sjá athugasemdina hér á undan).

Til að opna verkið hættir kerfið öllum vinnulínum sem eftir eru og lagfærir vöruhúsgögnin sem eru tengd vinnukenninu sem notandinn tilgreindi. Allar venjulegar aðgerðir meðhöndlunar í vöruhúsi sem fela í sér vörumagn sem verða fyrir áhrifum geta síðan haldið áfram.

Til að setja vöruna á tiltekinn stað eftir að vinnunni er aflýst, verður notandinn að nota birgðahreyfingu eða magnleiðréttingaraðgerð í fartæki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]