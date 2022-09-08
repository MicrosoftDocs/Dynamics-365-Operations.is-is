---
title: Hætta við vinnu í vörugeymslu fyrir meðhöndlun frávika
description: Þessi grein lýsir hætti við vinnu sem gerir vöruhúsaumsjónarmönnum kleift að sjá um læsta vinnu.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404433"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Hætta við vinnu í vörugeymslu fyrir meðhöndlun frávika

[!include [banner](../includes/banner.md)]

Hætta við vinnu virkni í Microsoft Dynamics 365 Supply Chain Management leyfir stjórnandanotandanum að hætta við tiltekna vöruhúsavinnu sem er í gangi, en það er lokað af kerfinu eða er ekki hægt að ljúka því vegna óvenjulegra aðstæðna. Þessi virkni er aðlaðandi og öruggur valkostur við SQL leiðréttingarforskriftir sem laga ósamræmd gögn. Hins vegar, þó að venjulega sé beðið um þessar forskriftir frá upplýsingatæknisérfræðingum, geta notendur í fyrirtækinu sem hafa stjórnandaréttindi notað aðgerðina til að hætta við vinnu.

Þú getur fengið aðgang að hætta við vinnu á **Vöruhússtjórnun** \> **Reglubundin verkefni** \> **Hreinsaðu til \> Hætta við vinnu**. Í valmyndinni **Hætta við vinnu** tilgreinirðu vinnukenni sem á að hætta við og veldu síðan **Í lagi**.

## <a name="warehouse-work-that-can-be-canceled"></a>Vöruhúsavinnsla sem hægt er að hætta við

Meðan á vöruhússaðgerðum stendur gæti starfskraftur lent í aðstæðum þar sem viðkomandi hefur skráð magn sem tiltekið af geymslustað yfir á notendastað sinn, en þá getur viðkomandi ekki skráð söluaðgerðina. Ósamræmd gögn um vöruhús eru oft, en ekki alltaf, ástæðan fyrir því að vinna er lokuð.

Ólíkt venjulegri hætta við virkni sem hægt er að nálgast með því að nota **Hætta við** hnappinn á vinnuhausnum krefst hætta við vinnu ekki að síðasta verklínan sem var lokið sé vinnulína **setja** tegund. Með öðrum orðum, fyrir hætt við vinnu virkni, er hægt að keyra afturköllunarrökfræði jafnvel þótt vörumagn á vinnulínu sé á notendastaðsetningu.

> [!NOTE]
> Fyrir vinnu sem þarf að hætta við af rekstrarástæðum verða notendur vöruhúsa að halda áfram að nota venjulega afpöntunarvirkni á vinnusíðunni.

Aðeins vinna **Sala**, **·**, **·**, eða **Áfylling** tegund er hægt að hætta við með því að nota hætta við vinnu virkni. Afpöntunarrökfræði verður ekki keyrð fyrir fryst hráefnistínsluvinnu eða vinnu sem hægt er að hætta við með því að nota venjulega afturköllunaraðgerðina (sjá athugasemdina á undan).

Til að opna verkið hættir kerfið öllum vinnulínum sem eftir eru og lagfærir vöruhúsgögnin sem eru tengd vinnukenninu sem notandinn tilgreindi. Allar venjulegar aðgerðir meðhöndlunar í vöruhúsi sem fela í sér vörumagn sem verða fyrir áhrifum geta síðan haldið áfram.

Til að setja vöruna á tiltekinn stað eftir að vinnunni er aflýst, verður notandinn að nota birgðahreyfingu eða magnleiðréttingaraðgerð í fartæki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]