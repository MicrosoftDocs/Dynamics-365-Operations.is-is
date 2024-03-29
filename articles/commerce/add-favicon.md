---
title: Bæta við táknmynd
description: Þessi grein útskýrir hvernig á að bæta favicon við síðuna þína.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 41d6d8f823c7364f9206fd0f7588e35b6f0a018a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270438"
---
# <a name="add-a-favicon"></a>Bæta við táknmynd

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að bæta favicon við síðuna þína.

Táknmynd er lítil myndaskrá sem er sýnd á flipa vafra, á heimilisfangsstikunni, í vafraferlinum og meðal annars í bókamerkjum eða uppáhaldi. Við mælum með að þú bætir táknmynd við vefinn þinn vegna þess að það táknar og styrkir vörumerkið þitt og hjálpar til við að greina vefsíðuna frá öðrum síðum sem viðskiptavinir þínir heimsækja.

Þó að þú getir bætt mörgum favicons af ýmsum stærðum og skráargerðum við síðuna þína, sýnir þessi grein hvernig á að bæta við einu favicon. Hins vegar er sama ferli og staðsetning notuð til að bæta fleiri táknmyndum við.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Hladdu upp táknmynd í eignasafn vefsvæðisins

Til að hlaða upp táknmynd í eignasafn vefsvæðisins skaltu fylgja þessum skrefum.

1. Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.
1. Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.
1. Í glugga skráavafrans skal fara í myndaskrá táknmyndarinnar sem á að hlaða upp, velja hana og velja síðan **Opna**.
1. Í valmyndinni **Hlaða upp margmiðlun** slærðu inn nauðsynlegan titil og annan texta.
1. Ef ætlunin er að birta myndina strax eftir upphleðslu skal velja gátreitinn **Birta margmiðlunaratriði eftir upphleðslu**.

    > [!NOTE]
    > Ef gátreiturinn **Birta margmiðlunaratriði eftir upphleðslu** er ekki valinn er nauðsynlegt að fara aftur á síðuna **Margmiðlunarefni** og birta táknmyndina handvirkt seinna.

1. Veljið **Í lagi**.
1. Afritaðu opinberu vefslóð hugbúnaðarins í eiginleikaglugganum til hægri. Þú munt nota þessa vefslóð síðar.

## <a name="create-the-html-for-your-favicon"></a>Búa til HTML fyrir táknmynd

Til að búa til HTML fyrir táknmyndina skal nota eftirfarandi HTML-streng. Fyrir **href** eigindina skal skipta út **Opin\_vefslóð\_fyrir\_þína\_táknmynd** fyrir opnu vefslóðina sem var afrituð á undan.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Búa til brot sem inniheldur lýsimerki fyrir táknmyndina þína

Til að búa til brot sem inniheldur lýsimerki fyrir táknmyndina þína skal fylgja þessum skrefum.

1. Farðu í **Brot** og veldu **Nýtt**.
1. Í svarglugganum **Nýtt brot** skal velja **Lýsimerki** sem eininguna sem brotið byggir á.
1. Sláðu inn heiti fyrir brotið og veldu svo **Í lagi**.
1. Í trjástigveldi brotsins skal velja undireininguna **Sjálfgefin lýsimerki**.
1. Í svæðinu hægra megin, undir **Lýsimerki**, skal velja **Bæta við** og síðan slá inn HTML-strenginn sem var áður búinn til fyrir táknmyndina. 
1. Veldu **Ljúka við breytingar** og síðan **Birta** til að birta brotið.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Bæta broti lýsimerkis við HTML-haus síðanna þinna

Til að bæta broti lýsimerkis við **haus** HTML-svæðis síðanna þinna skal fylgja þessum skrefum.

1. Farðu í **Sniðmát**, opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta táknmyndinni þinni við og veldu síðan **Breyta**.
1. Í trjástigveldi sniðmátsins skal velja hnapp úrfellingarmerkis (**...**) hægra megin við hólfið **HTML-haus** og velja síðan **Bæta við broti**.
1. Í svarglugganum **Velja brot** skal velja síðubrot lýsimerkis sem var áður búið til og velja síðan **Í lagi**.
1. Veldu **Ljúka við breytingar** og síðan **Birta** til að birta sniðmátið.

> [!NOTE]
> Ef svæðið þitt notar meira en eitt sniðmát þarftu að bæta broti lýsismerkjanna við þau öll.

Þegar síður, sem byggja á sniðmátinu sem brot lýsimerkjanna var bætt við, eru forskoðaðar ættir þú að sjá táknmyndina í vafraglugganum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við lógói](add-logo.md)

[Velja þema svæðis](select-site-theme.md)

[Unnið með CSS hnekkiskrám](css-override-files.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
