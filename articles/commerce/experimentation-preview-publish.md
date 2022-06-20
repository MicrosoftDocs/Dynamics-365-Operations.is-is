---
title: Forskoða og birta tilraun
description: Þessi grein lýsir því hvernig á að forskoða og birta tilraun frá Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 5da7a4e3c17057278d02ebd45702d1de404f0dc6
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946134"
---
# <a name="preview-and-publish-an-experiment"></a>Forskoða og birta tilraun

Þessi grein lýsir því hvernig á að forskoða og birta tilraunina þína í Dynamics 365 Commerce eftir að þú hefur [tengdi tilraunina þína og breytti tilbrigðum þínum](experimentation-connect-edit.md). Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Fjallað er um fleiri skref í aðskildum greinum.

[ ![Tilraunaferli notanda - Forskoða og birta.](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

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

### <a name="force-variations-for-testing"></a>Þvingaðu afbrigði til að prófa

Þegar tilraunin er komin í loftið geturðu bætt tilraunaauðkenninu og afbrigðisauðkenninu við sjálfgefna vefslóð síðunnar til að þvinga fram afbrigði í prófunar- eða sjálfvirknitilgangi. Til dæmis, ef sjálfgefna vefslóð síðunnar er`https://fabrikam.com/modern/homepage`, þú getur þvingað fram afbrigði með vefslóð eins og `https://fabrikam.com/modern/homepage?exp=18012910471|18024360464`. Þú getur fengið tilraunaauðkenni og afbrigðisauðkenni fyrir tilraunaafbrigðið þitt á forskoðunarslóðinni í **Forskoðun** reynslu sem lýst er hér að ofan.

## <a name="previous-step"></a>Fyrra skref
[Tengja og breyta tilraun](experimentation-connect-edit.md)

## <a name="next-step"></a>Næsta skref
[Keyra og fylgjast með tilraun](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
