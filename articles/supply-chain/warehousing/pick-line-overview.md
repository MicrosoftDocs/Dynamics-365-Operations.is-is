---
title: Setja upp valmyndaratriði fartækis til að birta yfirlit yfir val á línu
description: Þetta efnisatriði útskýrir hvernig á að skilgreina þegar listi yfir allar vinnulínur verður sýndur starfsmönnum vöruhúss sem eru að vinna úr vöruhúsavinnu í fartæki. Þessi möguleiki getur gagnast starfsmönnum vöruhúss sem þurfa oft að sjá yfirlit yfir tínslulínur í vinnupöntun þannig að þeir geti hagrætt tínsluröðinni.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 433ed2152c47dbe698a640b099cb34727fe63452
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989694"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Setja upp valmyndaratriði fartækis til að birta yfirlit yfir val á línu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig skilgreina á valkosti sem tengjast yfirliti tiltektarlínu fyrir valmyndaratriði fartækis sem eru notuð til að vinna úr tiltektarvinnu. Yfirlit tiltektarlínu gerir starfsmönnum vöruhúss kleift að skoða og velja úr lista yfir allar vinnulínur sem tengjast núverandi verki. Þessi möguleiki getur hjálpað starfsmönnum að hagræða tínsluröðinni. Þessi eiginleiki býður upp á valmöguleika sem koma í staðinn fyrir hefðbundna hnappinn **Sleppa** sem gerir starfsmönnum kleift að fara á milli línanna eina í einu í ákveðinni röð. (Hins vegar er valkosturinn til að nota þann hnapp enn tiltækur.)

Stjórnendur geta skilgreint hvert valmyndaratriði út af fyrir sig til að stjórna því hvernig, hvenær og hvar vöruhúsaforritið sýnir yfirlit tínslulína.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Kveikja á eiginleika fyrir yfirlit yfir tiltektarlínu vinnu

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** _Vöruhúsakerfi_
- **Heiti eiginleika:** _Yfirlit yfir tiltektarlínu vinnu_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Skilgreina valmyndaratriði til að birta lista yfir allar vinnulínur

Til að setja upp valmyndaratriði fartækis til að birta yfirlit yfir tiltektarlínur skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Veljið eða búið til valmyndaratriði sem tengist tiltektarvinnu og stillið eftirfarandi gildi:

    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Já*
    - **Stýrt af:** *Notandastýrt* eða *Kerfisstýrt*

    Frekari upplýsingar um hvernig á að búa til valmyndaratriði og nota ýmsar stillingar sem eru í boði á síðunni **Valmyndaratriði fartækis** er að finna í [Setja upp fartæki fyrir vinnu vöruhúss](configure-mobile-devices-warehouse.md).

1. Í flýtiflipanum **Almennt** skal skilgreina eiginleikann með því að stilla reitinn **Sýna vinnulínulista** á eitt eftirfarandi gilda:

    - **Sýna aðeins við beiðni** – Starfsmenn geta valið að skoða tínslulínulista með því að velja hnappinn **Fara í** í vöruhúsaforritinu.
    - **Sýna við upphaf hverrar tiltektar** – Starfsmenn sjá listann í hvert sinn sem þeir hefja eða ljúka tiltektarlínu. Einnig er hægt að skoða listann aftur með því að velja hnappinn **Fara í** í vöruhúsaforritinu.
    - **Sýna eingöngu við upphaf fyrstu tiltektar** – Starfsmenn sjá listann í hvert sinn sem þeir hefja nýja tiltektarvinnu, en ekki eftir hverja línu. Einnig er hægt að skoða listann aftur með því að velja hnappinn **Fara í** í vöruhúsaforritinu.
    - **Sýna aldrei** – Hefðbundni hnappurinn **Sleppa** birtist í vöruhúsaforritinu og slökkt er á skjámyndinni fyrir vinnulínulista. Hnappurinn **Sleppa** gerir starfsmönnum kleift að fara á milli línanna eina í einu í ákveðinni röð. Einnig er hægt að fara í gegnum listann eins oft og þarf til, þar til búið er að vinna úr öllum línum.

1. Í aðgerðarúðunni skal velja **Vista**.

    Ef reiturinn **Sýna vinnulínulista** er stilltur á eitthvað gildi fyrir utan *Sýna aldrei* verður hnappurinn **Reitalisti** á aðgerðasvæðinu tiltækur.

1. Veljið **Reitalisti** á aðgerðasvæðinu.
1. Á síðunni **Reitalisti** skal skilgreina upplýsingarnar sem vöruhúsaforritið sýnir fyrir hverja línu í listanum.

    - Reiturinn **Aðalstýring** er alltaf stilltur á *LineNum*. Hver lína í listanum hefst þar af leiðandi á línunúmeri.
    - Notið eftirstandandi reitina **Upplýsingasvæði** til að bæta við allt að sjö upplýsingasvæðum til viðbótar eftir þörfum. Í reitnum **Upplýsingasvæði** skal velja heiti vinnulínureits. Hver lína sýnir svo gildi fyrir þann reit. Gildin verða sýnd í pöntuninni sem er valin hér. Hægt er að skilja nokkra af reitunum **Upplýsingasvæði** eftir auða ef ekki reynist þörf á öllum sjö gildunum.

1. Á aðgerðasvæðinu skal velja **Vista** og síðan loka síðunni **Reitalisti**.
