---
title: Smásöluuppgjör
description: Þessi grein lýsir því hvernig yfirlýsingar eru búnar til og birtar.
author: ashishmsft
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0717c1198171f411e3c52233200ecfcc213dc13f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878458"
---
# <a name="retail-statements"></a>Smásöluuppgjör

[!include [banner](includes/banner.md)]

Í Dynamics 365 Commerce, er bókunarferli uppgjörs notað til að gera grein fyrir færslum sem koma upp í sölustað í skýi eða Modern POS (MPOS). Uppgjörsbókunarferlið notast við dreifingaráætlunina til að sækja safn sölustaðarfærslna í höfuðbiðlara (HQ). Færibreytur sem skilgreindar eru á síðunum **Færibreytur Commerce** og **Verslanir** eru notaðar til að velja færslurnar sem eru sóttar í einstök uppgjör.

Eftirfarandi skýringarmynd sýnir uppgjörsbókunarferlið. Í þessu ferli eru færslur sem eru skráðar á sölustað sendar til biðlara með því að nota verkraðara Commerce. Eftir að biðlari tekur við færslunum, er hægt að stofna, reikna og bóka færsluuppgjör fyrir verslunina.

[![Uppgjörsbókunarferli.](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Stofna og bóka uppgjör

Hægt er að stofna uppgjör handvirkt eða með því að nota runuvinnslur sem þú setur upp til að keyra reglubundið allan daginn. Í báðum tilvikum eftirfarandi skref eru notaðar til að stofna og bóka uppgjör.

### <a name="create-the-statement"></a>Stofna yfirlitið

Þetta skref auðkennir uppgjör er stofnað handvirkt fyrir verslun. Ef skilgreina runuvinnslu sjálfvirkt er hægt að stofna uppgjör fyrir allar verslanir samkvæmt áætlun sem skilgreina.

### <a name="calculate-the-statement"></a>Reikna yfirlitið

Í þessu þrepi eru færslulínur valdar eftir skilyrðum sem eru skilgreind fyrir hverja verslun á síðunum **Færibreytur Commerce** og **Verslanir**. Á þessum síðum skilgreinir þú skilyrði og tilgreinir hvernig færslurnar eru reiknaðar. Til að skoða lista yfir færslur sem eru teknar með í uppgjörinu áður en uppgjör er reiknað út skal nota síðuna **Færslur**.

Útreikningur uppgjörs notar skiptimyntartalningu frá afgreiðslukössunum sem talda upphæð. Einnig er hægt að færa talda upphæð inn handvirkt. Uppgjörið sýnir muninn á milli söluupphæðar fyrir færslur og raunverulegrar talinnar upphæðar í öllum greiðsluháttum. Uppgjörið bókast ef þessi mismunur er minna en hámarksbókunarmismunur sem er skilgreind fyrir verslunina.

> [!NOTE]
> Útreikningur yfirlits ferlið notar altæka númeraröð.

Þegar þú reiknar út yfirlýsingu, felur útreikningurinn í sér eftirfarandi verkefni:

- Merktu færslur fyrir valið tímabil sem voru ekki með í fyrri útreikningi uppgjörs.
- Reiknaðu út heildarupphæðir sem tekið var við í völdum færslum. Niðurstöðurnar eru birtar á uppgjörslínum, eftir uppgjörsaðferðinni:

    - Ef uppgjörsaðferðin er **Samtala**, er lína stofnuð fyrir hvern greiðslumáta í völdum færslum.
    - Ef uppgjörsaðferðin er **Starfsmaður**, er lína stofnuð fyrir hvern greiðslumáta í færslum sem voru framkvæmdar af völdum starfsmönnum.
    - Ef uppgjörsaðferðin er **Afgreiðslukassi**, er lína stofnuð fyrir hvern greiðslumáta í færslum sem voru framkvæmdar í völdum afgreiðslukössum.
    - Ef uppgjörsaðferðin er **Vakt**, er lína stofnuð fyrir hvern greiðslumáta í færslum sem voru framkvæmdar á vakt.

Ef gátreiturinn **Skipta eftir uppgjörsaðferð** er valinn á síðunni **Verslanir**, er sérstakt uppgjör stofnað eftir gildinu sem valið er í reitnum **Uppgjörsaðferð**.

Ef afgreiðslutími verslunar þinnar er lengur en fram yfir miðnætti, er hægt að stilla uppgjörsbókun þannig að hún sé í lok viðskiptadags frekar en í lok almanaksdags.

Á síðunni **Verslanir**, í flýtiflipanum **Uppgjör/lokun**, í reitnum **Lok viðskiptadags** skal færa inn tímann sem síðasta færslan verður að vera skráð til að vera tekin með í uppgjöri viðskiptadags. Veldu gátreitinn **Bóka sem viðskiptadag** til að bóka færsluna innan sama viðskiptadags. Þegar uppgjör er bókað, er hægt að hafa færslur sem skráðar eru innan sama viðskiptadags á sömu sölupöntun, þrátt fyrir að einhverjar færslur eigi sér stað fyrir miðnætti og aðrar færslur eigi sér stað eftir miðnætti.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Dæmi: Bókaðu yfirlýsing fyrir viðskiptadag sem nær yfir tvö almanaksdagar

Verslun er opin milli 8:00 og 3:00 og gátreiturinn **Bóka sem viðskiptadag** er valinn í stillingum verslunarinnar. Þann 31. maí skráir verslunin færslur milli 8:00 og miðnættis. Verslunin skráir einnig færslur milli 0:01 og 3:00 þann 1. júní.

Þegar verslunin bókar uppgjör sitt fyrir lok viðskiptadagsins, inniheldur framkölluð sölupöntun allar færslur sem skráðar voru á opnunartímanum 8:00 til 3:00, þrátt fyrir að færslurnar hafi átt sér stað á tveimur dögum, 31. maí og 1. júní.

Ef gátreiturinn **Bóka sem viðskiptadag** er hreinsaður fyrir sömu verslun, eru aðskildar sölupantanir framkallaðar þegar verslunin bókar uppgjör sitt fyrir lok viðskiptadagsins. Ein sölupöntun inniheldur færslur sem voru skráðar á opnunartímanum 8:00 til miðnættis þann 31. maí og önnur sölupöntun inniheldur færslur sem skráðar voru á opnunartímanum 0:01 til 3:00 þann 1. júní.

> [!NOTE]
> Áður en hægt er að stofna uppgjör, ætti að loka vaktir á tímabili yfirlitsins.

### <a name="post-the-statement"></a>Bókið uppgjörið.

Þegar yfirlit er bókað, eru sölupantanir og reikninga stofnaðir fyrir sölu í yfirlitinu.

- Staðgreiddum sölum er safnað saman í eina sölupöntun og eru reikningsfærðar fyrir sjálfgefinn viðskiptavin sem úthlutaður er versluninni.
- Sala þar sem viðskiptavinur var bætt við færslu í POS mynda sérstaka sölupantanir og reikninga, einn fyrir hvert einkvæmt kenni viðskiptavinar.

Greiðslubækur eru sjálfkrafa stofnaðar fyrir greiðslur í uppgjörinu og á birgðirnar eru uppfærðar fyrir verslun á sölustaður.


[!INCLUDE[footer-include](../includes/footer-banner.md)]