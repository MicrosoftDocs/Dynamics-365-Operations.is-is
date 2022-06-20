---
title: Hlaða upp og þjóna föstum skrám
description: Þessi grein lýsir því hvernig á að hlaða upp kyrrstæðum skrá inn í Microsoft Dynamics 365 Commerce vefsmiður, og hvernig á að búa til sérsniðna vefslóð og skráarheiti sem hægt er að nota til að biðja um þá skrá.
author: StuHarg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a1b14feba1466c3a5efc3b0ea66f20e9e818a8a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885323"
---
# <a name="upload-and-serve-static-files"></a>Hlaða upp og þjóna föstum skrám

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að hlaða upp kyrrstæðum skrá inn í Microsoft Dynamics 365 Commerce vefsmiður, og hvernig á að búa til sérsniðna vefslóð og skráarheiti sem hægt er að nota til að biðja um þá skrá.

Sumir tenglar þriðja aðila krefjast þess að skrá sé hýst og henni sé miðlað á svæði fyrir rafræn viðskipti. Þessir tenglar búast við því að skránni verði skilað með beiðnum á tiltekna vefslóð svarhringingar og skráarheiti. Þess vegna útskýrir þessi grein hvernig á að hlaða upp og birta kyrrstæða skrá sem hefur notandaskilgreinanlega vefslóð og skráarheiti á Dynamics 365 Commerce rafræn viðskipti síða.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Stofna vefslóð svæðis sem skilar fastri skrá

Til að búa til URL svæðis sem skilar fastri skrá í vefsmið Commerce skal fylgja þessum skrefum.

1. Farið á miðlasafn vefsvæðis og hlaðið upp skránni sem á að birtast fyrir beiðnir á URL sem er skilgreint. Ef þú hefur þegar hlaðið upp skránni geturðu sleppt þessu skrefi.
1. Opnaðu **vefslóð** fyrir vefsvæðið þitt.
1. Veljið **Nýtt \> Ný vefslóð**.
1. Í svarglugganum **Ný vefslóð** skal velja **Miðlasafn**.
1. Í reitinn **Vefslóð** skal slá inn vefslóðina. Hafðu skráarheitið með í slóðinni.
1. Veljið **Næst**. Miðlasafnið er opnað og sýnir allar miðlaeignir af gerðinni **skjal** sem hefur verið hlaðið upp.
1. Veljið skrána sem á að nota fyrir beiðnir á vefslóðina sem var skilgreind í skrefi 5.
1. Veljið **Vista**.

Á þessu stigi hefur vefslóðin sem var stofnuð stöðuna drög. Skránni sem vefslóðin bendir á verður ekki skilað fyrr en vefslóðin er birt. Áður en vefslóðin er birt er hægt að staðfesta að hún skili réttum gögnum.

## <a name="validate-and-publish-a-url"></a>Villuleita og birta vefslóð

Til að villuleita vefslóð áður en hún er birt skal fylgja þessum skrefum.

1. Opnaðu **vefslóð** fyrir svæðið þitt og veldu vefslóðina sem á að skoða.
2. Á eiginleikasvæðinu hægra megin, fyrir neðan hnappinn **Breyta**, skal velja réttan tengil ULR. Nýr vafragluggi opnast og villan 404 ætti að birtast.
3. Bætið við **?preview=inprogress** fyrirspurnarstrengnum á URL (til dæmis `https://yoursite.com/callback.html?preview=inprogress`) og endurhlaðið síðuna. Skráin sem var hlaðið upp í miðlasafnið ætti að vera skilað í svarinu.

Þegar vefslóð hefur verið staðfest er hægt að birta hana.

1. Opnaðu **vefslóð** fyrir svæðið þitt og veldu vefslóðina.
2. Á skipanastikunni skal velja **Birta**.

## <a name="update-the-file-that-a-url-points-to"></a>Uppfærið skrána sem vefslóðin bendir á

Eftir að vefslóðin hefur verið birt er hægt að uppfæra hana þannig að hún vísar í aðra skrá. Að öðrum kosti er hægt að uppfæra vefslóðina þannig að hún bendir á aðra gerð tilfanga, eins og lýst er í næsta hluta. Til dæmis er hægt að láta vefslóð vísa á innri síðu eða framsendingu.

Til að uppfæra skrána sem vefslóðin bendir á skal fylgja þessum skrefum.

1. Farið á **Vefslóð** fyrir svæðið og veljið vefslóðina sem á að uppfæra.
1. Í eiginleikastikunni hægra megin skal velja **Breyta**.
1. Undir **Úthlutun vefslóðar** skal velja reitinn **Skref 2** og síðan velja nýtt skjal úr miðlasafninu.
1. Veljið **Bæta við**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Uppfæra eignagerðina sem vefslóðin bendir á

Einnig er hægt að uppfæra vefslóðin þannig að hún vísar í aðra gerð eignar (tilfang), t.d. innri síðu eða framsendingu.

Til að uppfæra eignagerð sem vefslóðin bendir á skal fylgja þessum skrefum.

1. Farið á **Vefslóð** fyrir svæðið og veljið vefslóðina sem á að uppfæra.
1. Í eiginleikastikunni hægra megin skal velja **Breyta**.
1. Undir **Úthlutun vefslóðar**, undir **Skref 1**, skal velja aðra eignagerð.
1. Veljið gátreitinn **Skref 2** og veljið síðan nýju eignina.
1. Veljið **Bæta við**.

## <a name="change-the-url-path"></a>Breyta vefslóð

Þegar búið er að stofna vefslóð er ekki hægt að breyta slóð hennar. Ef nauðsynlegt er að breyta vefslóð sem þjónar skrá eða öðrum gerðum tilfanga þarf að stofna nýja vefslóð, varpa henni á fyrirliggjandi skrá eða önnur tilföng, taka hana úr birtingu og eyða svo gömlu vefslóðinni.

Til að breyta vefslóð skal fylgja þessum skrefum.

1. Til að búa til nýja vefslóð og varpa henni við núverandi skrá eða aðra auðlind skaltu fylgja leiðbeiningunum í [Búðu til vefslóð sem skilar kyrrri skrá](#create-a-site-url-that-returns-a-static-file) kafla fyrr í þessari grein.
1. Velja skal nýju vefslóðina og velja **Birta** á skipanastikunni. Nýja vefslóðin er birt.
1. Til að opna gömlu vefslóðina skal velja hana og velja svo **Taka úr birtingu** á skipanastikunni. Nú er hægt að eyða eldri vefslóð ef óskað er.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit stjórnunar stafrænna eigna](dam-overview.md)

[Hlaða upp myndum](dam-upload-images.md)

[Hlaða upp myndskeiðum](dam-upload-video.md)

[Hlaða upp skrám öðrum en myndum og myndböndum](dam-upload-files.md)

[Skera myndir](dam-crop-images.md)

[Sérstilla áherslupunkta myndar](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]