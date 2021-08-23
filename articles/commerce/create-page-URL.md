---
title: Búa til síðuvefslóð
description: Þetta efni fjallar um grunnhugtök og verklagsreglur við að búa til vefslóð á síðuna þína.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 923723ce6e3f92c5186cd8a562a6e3fee3fdf70dfe8db29c86192cb1db515b1a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717724"
---
# <a name="create-a-page-url"></a>Búa til síðuvefslóð

[!include [banner](includes/banner.md)]

Þetta efni fjallar um grunnhugtök og verklagsreglur við að búa til vefslóð á síðuna þína.

Vefslóðin í heild eða alger sem vísar á síðu á vefsvæðinu þínu samanstendur af aðskildum hlutum. Til dæmis slóðin hefur `https://www.contoso.com/en-us/contactus` eftirfarandi hluta:

- `https://www.contoso.com` - HTTP samskiptareglur og lén svæðisins.
- `/en-us`- Tungumálaslóð vefsvæðisins.
- `/contactus` - Tengd slóð fyrir síðuna **Hafa samband**. Tengd slóð er einnig þekkt sem slóð *snigill*.

Þú setur upp lén vefsvæðisins og valfrjálsa tungumálaslóð þegar þú setur vefsvæðið upp. Þú getur bætt við fleiri lénum og tungumálaslóðum á vefsvæðið í gegnum netverslunarsíðu í stillingum vefsvæðisins.

Slóðarsnigill fyrir síðu er til sem sjálfstæð eining í höfundarumhverfi. Vefslóð síðu samanstendur af tveimur hlutum: heiti sem táknar slóðarsnigil og bendil á síðu á annaðhvort vefsvæðinu eða utanaðkomandi síðu. Einnig er hægt að stilla vefslóð síðu til að virka sem tilvísun á aðra síðu á annaðhvort vefsvæðinu eða utanaðkomandi vefsvæði.

## <a name="create-a-page-url"></a>Búa til síðuvefslóð

Það eru tvær leiðir til að búa til vefslóðir:

- Sjálfkrafa þegar þú býrð til síðu
- Handvirkt af síðunni **Vefslóðir**

### <a name="create-a-page-url-when-you-create-a-page"></a>Stofna vefslóð síðu þegar þú býrð til síðu

Ef þú gefur upp heiti í reitinn **Vefslóð** þegar þú býrð til nýja síðu verður vefslóð síðu sem vísar á þá síðu sjálfkrafa stofnuð á síðunni **Vefslóðir**. Eftir að þú hefur birt slóðina og síðuna sem hún vísar á geta notendur vefsvæða (viðskiptavinir þínir) fengið aðgang að síðunni sem er tengd slóðinni.

> [!NOTE]
> Ef þú birtir vefslóð án þess að birta síðuna sem hún vísar á fá notendur vefsvæðis 404-villu þegar þeir reyna að komast á síðuna. Ef þú birtir síðu án þess að birta slóðina sem vísar á hana er ekki hægt að komast á síðuna með því að nota slóð.

### <a name="manually-create-a-page-url"></a>Stofna síðuvefslóð handvirkt

Þegar þú stofnar nýjar síður þarf ekki að tilgreina vefslóð síðu. Ef þú skilur vefslóðarreitinn eftir auðan er síðan búin til í óbundinni stöðu. Í þessu tilfelli geta viðskiptavinir ekki fengið aðgang að síðunni, jafnvel þó að hún sé birt. Til að gera síðuna aðgengilega verður þú að búa til slóðina handvirkt og tengja hana við síðuna.

Fylgdu þessum skrefum til að búa til síðuslóðina á handvirkan hátt.

1. Á síðunni **Vefslóðir** skal velja **Nýtt**.
1. Veljið síðu á vefsvæði til að tengja við vefslóðina.
1. Sláðu inn slóðarsnigilinn og veldu síðan **Í lagi**.

Á þessum tímapunkti er vefslóðin í drögum. Það verður að birta áður en notendur vefsvæða geta nálgast viðkomandi síðu.

## <a name="update-a-page-url"></a>Uppfæra síðuvefslóð

Fylgdu þessum skrefum til að uppfæra markmiðasíðu síðuvefslóðar.

1. Á síðunni **Vefslóðir** velurðu slóðina sem á að uppfæra.
1. Í eiginleikaglugganum til hægri velurðu úrfellingarhnappinn (**...**) við hliðina á marksíðureitnum.
1. Í svarglugganum velurðu aðra síðu og velur síðan **Í lagi**.
1. Vistaðu og birtu vefslóðina.

## <a name="redirect-a-page-url"></a>Framsendingarslóð síðu

Stundum gætirðu viljað að viðskiptavinir þínir skoði aðra síðu þegar þeir biðja um sérstaka slóð. Í þessum tilvikum er besta og auðveldasta aðferðin oft að breyta síðunni sem vefslóð síðunnar bendir á. Hins vegar gætir þú haft réttmætar ástæður fyrir því að nota tilvísanir HTTP 301 eða 3023 til að beina beiðnum um vefslóð yfir á aðra slóð.

Fylgdu þessum skrefum til að beina vefslóðinni yfir á aðra slóð.

1. Á síðunni **Vefslóðir** velurðu slóðina sem á að uppfæra.
1. Í eiginleikaglugganum til hægri velurðu **Framsenda**.
1. Veldu áfangastað fyrir framsendinuna:

    - Til að benda á aðra síðu á vefsvæðinu velurðu **Innri vefslóð**, velur sporbaugshnappinn (**...**) og velur síðan slóðina sem á að framsenda á.
    - Til að benda á síðu á ytra vefsvæði velurðu **Ytri vefslóð** og velur síðan fulla vefslóð fyrir þá síðu. Vertu viss um að hafa samskiptareglur með. Til dæmis er slegið inn `https://domain.com/new/page`. Ef vefslóðin framsendir þegar á innri vefslóð verður þú að velja **Hreinsa val** áður en þú getur slegið inn ytri slóð.

1. Veldu framsendingargerð:

    - **Varanleg tilvísun (301)** - Veldu þennan valkost þegar þú veist að innihaldið er að flytja til frambúðar og mun ekki snúa aftur á fyrri slóðina. Leitarvélar munu úthluta SEO-gildi leitarvélabestunar framsendingarslóðarinnar á vefslóðina sem framsent er á og uppfæra skrár til að sýna nýju slóðina. 
    - **Tímabundin framsending (302)** - Veldu þennan valkost til að framsenda umferð án þess að uppfæra leitarvélar. Þessi aðferð er venjulega notuð ef innihaldið mun brátt snúa aftur til fyrri slóðina.

1. Þegar þú ert tilbúin/n til að framkvæma framsendinguna skaltu vista og birta slóðina.

## <a name="additional-resources"></a>Frekari upplýsingar

[Sérstilla yfirlit svæðis](customize-site-navigation.md)

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
