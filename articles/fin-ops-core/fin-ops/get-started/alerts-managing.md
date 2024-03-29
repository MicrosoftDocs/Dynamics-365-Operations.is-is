---
title: Runuvinnsla viðvarana
description: Þessi grein gefur upplýsingar um runuvinnslu viðvarana.
author: RichdiMSFT
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: ba17ebe1bdd95b8780b99b8f82b566bf527aca89
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860069"
---
# <a name="batch-processing-of-alerts"></a>Runuvinnsla viðvarana

[!include [banner](../includes/banner.md)]

Viðvaranir eru unnar í runuvinnslu. Nauðsynlegt er að setja upp runuvinnslu fyrir ferlið og afhenda viðvaranir.

Runuvinnsluvirkni styður tvennskonar tilvik:

- Atvik ræst af breytingabyggðum atvikum. Einnig er vísað í þessi atvik sem stofna/eyða og uppfæra atvik.
- Viðburðir sem eru kveikt með skiladögum.

Þú getur sett upp runuvinnslur fyrir hverja gerð af atviki.

## <a name="batch-processing-for-change-based-events"></a>Runuvinnsla fyrir breytingabyggð atvik

Kerfið les öll breytingabyggð tilvik sem hafa átt sér stað frá því að runuvinnsla var síðast keyrð. Breytingabyggð atvik uppfærslurnar á svæði, eyðingu færslna og stofnun færslna. Þessi tilvik eru borin saman við skilyrðin sem eru settar upp í viðvörunarreglum. Þegar atvik passar við skilyrðin í reglu býr runuvinnslan til viðvörun.

### <a name="frequency-for-change-based-events"></a>Tíðni breytingabyggðra atvika

Hægt er að setja upp runuvinnslu fyrir breytingabyggð atvik sem kveikir vinnslu viðvörunar fljótlega eftir að kerfið skráir atvikið. Ef þú setur upp runuvinnsluna svo hún endurtaki sig, fá notendur viðvaranir fyrr eftir að breytingar hafa átt sér stað. Hins vegar gæti há tíðni á runuvinnslu haft neikvæð áhrif á afköst kerfisins.

Á hinn bóginn getur runuvinnsla sem endurtekur sig sjaldnar, og er tímasett þegar álag á kerfinu er lítið, hjálpað til við að bæta afköst kerfisins. Hins vegar getur lág tíðni á runuvinnslu hugsanlega ekki mætt kröfum notenda um tímanlegar viðvaranir.

Þ.a.l. þegar þú setur upp tíðni runuvinnslu fyrir breytingabyggð atvik skaltu íhuga jafnvægið á milli tímasetninga á viðvörunum og afköstum kerfisins. Þetta mun skipta meira máli eftir því sem að notendum fjölgar sem búa til viðvörunarreglur. Tíðnin hefur ekki áhrif á fjölda tilvika sem kerfið vinnur úr. Ef fleiri notendur búa til reglur verða hins vegar fleiri athuganir gerðar í ferlinu. Þessi gerð af gagnaskiptum getur haft áhrif á afköst kerfisins.

#### <a name="the-risks-of-low-batch-frequency"></a>Hætturnar á lágri runutíðni

Ef þú setur upp lága tíðni fyrir runuvinnslu á breytingabyggðum atvikum getur gögnum sem tengjast skilyrðum viðvörunarreglna verið breytt fyrir vinnslu. Því gætirðu misst viðvaranir.

Til viðvörunarregla er til dæmis sett á til að kvikna þegar atvikið er **breytingar á tengilið viðskiptavinar** og skilyrðin eru **viðskiptavinur = BB**. Með öðrum orðum, þegar tengilið viðskiptavinar er breytt fyrir viðskiptavin BB, skráir ferlið tilvikið. Hins vegar er runuvinnslukerfið sett upp þannig að runuvinnsla á sér stað sjaldnar en gagnaskráning. Ef nafn viðskiptavinar er breytt úr **BB** í **AA** áður en unnið er úr atvikinu, samsvara gögnin í gagnagrunninum ekki lengur skilyrðunum í reglunni, **viðskiptavinur = BB**. Þannig að þegar loksins er unnið úr atvikinu er engin viðvörun sett af stað.

### <a name="set-up-processing-for-change-based-alerts"></a>Setja upp vinnslu fyrir viðvaranir byggðar á breytingum

1. Farðu í **Kerfisstjórnun** &gt; **Reglubundin verkefni** &gt; **Viðvaranir** &gt; **Viðvaranir byggðar á breytingum**.
2. Sláðu inn viðeigandi upplýsingar í svargluggann **Viðvaranir byggðar á breytingum**.

## <a name="batch-processing-for-due-date-events"></a>Runnuvinnsla fyrir skiladagaatvik

Kerfið ber kennsl á öll atvik sem orsakast af skiladögum og þessi atvik eru borin saman við skilyrðin sem sett eru upp í viðvörunarreglum. Runuvinnslan býr til viðvörun þegar atvik passar við skilyrði í reglu.

### <a name="frequency-for-due-date-events"></a>Tíðni á skiladagaatvikum

Fyrir skiladagaatvikum gætirðu viljað setja upp runuvinnslur sem eru keyrðar að nóttu til eða á tilteknum tímum dags til að halda jafnvægi á álagi kerfisins. Við mælum með að þú setjir upp runuvinnsluna þannig að hún sé keyrð að minnsta kosti einu sinni á dag. Ef viðvaranir verða sendar eins fljótt og auðið er skal setja upp runuvinnslu þannig að hún eigi sér stað strax eftir að kerfisdagsetningunni hefur verið breytt. Ef þú vilt búa til viðvaranir vegna skiladagaatvika sem eiga sér stað eftir að runuvinnsla hefur þegar unnið úr viðvörunum getur þú keyrt runuvinnsluna aftur á sama degi.

Til dæmis hefur runuvinnsla verið keyrð á tilteknum degi. Þú býrð síðan til innkaupapöntun sem hefur skiladaga sem ætti að kalla á viðvörun á þessum sama degi. Til að fá viðvörunina á þessum degi verður þú að keyra runuvinnsluna aftur eftir að innkaupapöntunin hefur verið búin til. Hins vegar, ef þú keyrir ekki runuvinnsluna aftur á þeim degi, ber runuvinnsla næsta dags kennsl á öll skiladagaatvikin sem ekki var unnið úr daginn áður.

> [!NOTE]
> Jafnvel þegar runuvinnslan er keyrð oftar en einu sinni á dag, eru viðvaranir ekki endurteknar fyrir sama skiladagaatvik og skilyrði. Viðvaranir eru aðeins búnar til fyrir dagsetningar sem eru komnar á skiladag vegna breytinga sem áttu sér stað í kerfinu eftir að síðasta runuvinnsla var keyrð.

### <a name="batch-processing-window"></a>Runuvinnslugluggi

Hægt er að stöðva vinnslu viðvörunarreglna í fyrirtæki af ýmsum ástæðum. Þessar ástæður eru meðal annars frí, kerfisvillur eða önnur vandamál sem koma í veg fyrir að runuvinnslurnar séu keyrðar um nokkurt skeið.

Til að koma í veg fyrir að viðvaranir skiladaga úreldist vegna þess að runuvinnsla hefur ekki verið keyrð í nokkra daga, getur þú sett upp runuvinnsluglugga. Hægt er að nota runuvinnsluglugga til að koma í veg fyrir að runuvinnsla sé keyrð í tiltekinn fjölda daga.

Ef þú setur upp runuvinnsluglugga er viðvörun send þegar unnið er úr viðvörunarreglunni, jafnvel þó að viðvörunin fari fram úr tímamörkunum sem eru skilgreind í skilyrðum skiladags. Viðvörun er áfram send svo lengi sem ekki er farið fram yfir tímabilið sem er skilgreint af þessum tímamörkum ásamt runuvinnsluglugganum. Þegar tímabilið fer yfir gildi sem er skilgreint af tímamörkunum ásamt runuvinnsluglugganum, er viðvörun ekki lengur send.

### <a name="set-up-processing-for-due-date-alerts"></a>Setja upp vinnslu fyrir skiladagaviðvörun

1. Farðu í **Kerfisstjórnun** &gt; **Reglubundin verkefni** &gt; **Viðvaranir** &gt; **Skiladagaviðvaranir**.
2. Í svarglugganum **Skiladagaviðvaranir** skal færa inn viðeigandi upplýsingar.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
