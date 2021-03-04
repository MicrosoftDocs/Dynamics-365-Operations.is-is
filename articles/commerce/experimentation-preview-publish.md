---
title: Forskoða og birta tilraun
description: Þetta efnisatriði lýsir því hvernig á að forskoða og birta tilraun úr Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/22/2020
ms.locfileid: "4413297"
---
# <a name="preview-and-publish-an-experiment"></a>Forskoða og birta tilraun

Þetta efnisatriði lýsir því hvernig á að forskoða og birta tilraunir þínar í Dynamics 365 Commerce eftir að þú hefur [tengt tilraunina þína og breytt afbrigðunum](experimentation-connect-edit.md). Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Önnur skref eru afgreidd í aðskildum efnisatriðum.

[ ![Ferli tilraunanotanda - Forskoða og birta](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Skoða afbrigði tilrauna
Hægt er að skoða afbrigðin og halda áfram að breyta þeim þar til þau líta út eins og til er ætlast.

Til að forskoða tilraunarafbrigðin í Commerce svæðasmíð skal fylgja þessum skrefum.

1. Í fellivalmynd afbrigða fyrir neðan skipanastikuna skal velja efnið sem á að forskoða. 
1. Á skipanastikunni skal velja **Forskoða**. Forskoðun á því hvernig efnið mun líta út þegar það verður birt.
1. Til að forskoða annað afbrigði skal velja það úr fellivalmynd afbrigða og velja **Forskoða** aftur.

## <a name="publish-your-experiment"></a>Birta tilraun
Ef ekki er notaður birtingarhópur til að tímasetja hvenær tilraunin á að fara á netið og ætlunin er að birta hana strax, skal velja **Birta** í skipanastikunni. Öll afbrigði sem tilheyra tilrauninni verða birt.
    
> [!IMPORTANT]
> Ef síðan er með óbirta vefslóð þarf fyrst að birta vefslóðina, annars verður hún ekki sýnileg notendum vefsvæðisins. Frekari upplýsingar er að finna í [Vista, forskoða og birta síðu](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Nota birtingarhópa til að tímasetja hvenær tilraunin á að fara á netið
Hægt er að tímasetja afbrigði til birtingar sem búin eru til í vefsmiðnum með því að nota birtingarhóp. Innan birtingarflokks er hægt að tengja síðu eða brot við tilraunina með því að velja **Tilraunir** í vinstra yfirlitssvæði. Einnig er hægt að gera þetta með því að velja **Síður** eða **Brot** og fylgja leiðbeiningunum í [Tengja tilraun og breyta afbrigðum](experimentation-connect-edit.md). Upplýsingar um birtingarhópa er að finna í [Vinna með birtingarhópa](publish-groups.md).

Þegar birtingarhópar eru notaður með tilraunum, þarf að huga að nokkrum mikilvægum atriðum.
- Þegar síðu eða broti, sem er með tilraun í gangi, er bætt við birtingarhóp, verður tilraunin fjarlægð af síðunni eða brotinu í birtingarhópnum.
- Tilraunir sem eru tengdar við síður á virku vefsvæði eru ekki í boði fyrir síður innan birtingarhópa og öfugt. Á sama hátt verða síður sem eru með tilraunir í gangi á virku vefsvæði ekki í boði fyrir aðrar tilraunir í birtingarhópnum og öfugt.
- Þegar birtingarhópur er birtur eða tímasettur, verður allt efni í birtingarhópnum birt, óháð því hvort tilraun er tengd við birtingarhópinn.
- Vegna þess að birtingarhópur verður áfram til eftir að hann hefur verið birtur á virku vefsvæði, halda tilraunir í birtingarhópnum áfram að vera til. Þess vegna er ekki hægt að tengja aðrar tilraunir við sömu síðu eða brot. Til að koma í veg fyrir þessa takmörkun skal eyða öllum birtingarhópum með viðvarandi tilraunum. Á sama hátt, ef eyða á tilraun á virku svæði sem einnig er til í birtingarhóp, skal eyða henni úr birtingarhópnum fyrst.

## <a name="previous-step"></a>Fyrra skref
[Tengja og breyta tilraun](experimentation-connect-edit.md)

## <a name="next-step"></a>Næsta skref
[Keyra og fylgjast með tilraun](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]