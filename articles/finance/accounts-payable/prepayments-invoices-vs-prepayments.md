---
title: Fyrirframgreiðslureikningar samanborið við fyrirframgreiðslur
description: Þessi grein lýsir og ber saman aðferðirnar tvær sem fyrirtæki geta notað fyrir fyrirframgreiðslu (fyrirframgreiðslur).
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f828b93075c134778da280243c0875edf99300
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715830"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Fyrirframgreiðslureikningar samanborið við fyrirframgreiðslur

[!include [banner](../includes/banner.md)]

Þessi grein lýsir og ber saman aðferðirnar tvær sem fyrirtæki geta notað fyrir fyrirframgreiðslu (fyrirframgreiðslur). Önnur aðferðin stofnar fyrirframgreiðslureikning sem tengist innkaupapöntun. Hin aðferðin stofnar fylgiskjöl fyrirframgreiðslu með því að stofna færslur í færslubók og merkja þær sem fylgiskjöl fyrirframgreiðslna.

Fyrirtæki gæti gefið út fyrirframgreiðslur (fyrirframgreiðsla) til lánardrottna fyrir vörur eða þjónustu áður en þær vörur eða þjónustu hafa verið uppfylltar. Hægt er að nota tvær aðferðir til að gefa út fyrirframgreiðslur til lánardrottna. Til að lágmarka áhættu, er hægt að rekja fyrirframgreiðslur með því að skilgreina fyrirframgreiðslu á innkaupapöntun. Fyrir þessa aðferð, verður að stofna fyrirframgreiddum reikningi sem er tengd innkaupapöntun. Þessi aðferð er kallað reikningsfærsla fyrirframgreiðslu. Fyrirtæki sem vilja ekki rekja fyrirframgreiðslur jafn náið eða fá ekki fyrirframgreiðslureikning frá lánardrottni þeirra geta nota fylgiskjöl fyrirframgreiðslna í stað reikningsfærsluaðferð fyrirframgreiðslu. Hægt er að stofna færslubókafylgiskjöl fyrirframgreiðslu með því að stofna færslur í færslubók og merkja þær sem fylgiskjöl fyrirframgreiðslna. Fyrir þessa aðferð er ekki hægt að rekja hvaða fyrirframgreiðslu til lánardrottins eru gerðar á móti hvaða innkaupapantanir. Hins vegar er hægt að merkja bókaða fyrirframgreiðslu fyrir jöfnun á móti innkaupapöntun.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Hvenær á að nota reikningsfærslu fyrirframgreiðslu miðað við fyrirframgreiðslur

| Fyrirframgreiðslurreikningsfærsla                                                                | Fyrirframgreiðslur                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Skilgreina gildi fyrirframgreiðslu í innkaupapöntuninni.                                    | Ekkert fyrirframgreiðslugildi er skilgreint í innkaupapöntuninni.                    |
| Fyrirframgreiðslureikning og endanlegan reikning verður að bóka.                       | Engin fyrirframgreiðslureikning verður að bóka.                                    |
| Skuld fyrir fyrirframgreiðsluna er geymt í lykli fyrirframgreiðslu, ekki AP lykli. | Skuld fyrir fyrirframgreiðsluna er geymt í AP lykil.                  |
| Staða lánardrottins endurspeglar ekki gildi fyrirframgreiðslu í gegnum ferlið.     | Staða lánardrottins endurspeglar gildi fyrirframgreiðslu í gegnum ferlið. |
| reikningsfærsla Fyrirframgreiðslu er aðeins tiltæk í Viðskiptaskuldir.                         | Fyrirframgreiðslur eru tiltækar í viðskiptaskuldum og viðskiptakröfum.    |

## <a name="overview-of-the-prepayment-process"></a>Yfirlit yfir fyrirframgreiðsluferlið
Bókhaldsvenjur í mörgum löndum/svæðum krefjast þess að fyrirframgreiðslur frá viðskiptavini eða til lánardrottins séu ekki bókaðar á venjulega safnlykla viðskiptavinar eða lánardrottins. Í staðinn eru þessar greiðslur bókaðar á sérstakan fjárhagslykil fyrir fyrirframgreiðslur. Þegar sölupöntun eða innkaupapöntun er gerð er reikningur gefinn út á viðskiptavin eða lánardrottin. Við greiðslu reikningsins er fyrirframgreiðslan og fyrirframgreiðsla VSK á fjárhagslyklum fyrirframgreiðslu bakfærðar og reikningsupphæðirnar eru sjálfvirkt bókaðar á venjulega safnlykla. Til að stofna fyrirframgreiðslu skal fylgja eftirfarandi skrefum:

1.  Setja upp bókunarreglur fyrir fyrirframgreiðslur
2.  Í Færibreytur viðskiptakrafna og Færibreytur lánardrottna, undir **Fjárhags og virðisaukaskatts**, veljið nýja bókunarreglu með því að nota **Bókunarregla með fyrirframgreiðslu fyrir greiðslubók** færibreyta.
3.  Stofnið greiðslubók og síðan nýja greiðslu.
4.  Hægt er að merkja greiðsluna sem fyrirframgreiðslu. Ef greiðsla er merkt sem fyrirframgreiðsla, greiðslan er bókuð í fjárhagslyklana sem eru skilgreindar í bókunarreglu sem er sett upp í skrefum 1 og 2. Þar að auki eru skattar reiknaðir, ef greiðsla er merkt sem fyrirframgreiðsla. Sumar yfirvöld krefjast þess að skattar séu greiddir þegar fyrirframgreiðsla er skráð, jafn vel þó enginn sé reikningurinn.
5.  Bókið fyrirframgreiðsluna
6.  Valfrjálst: Hægt er að jafna fyrirframgreiðsla við innkaupapöntun eða sölupöntun áður en reikningurinn er stofnaður. Á sölupöntun eða innkaupapöntun síðu skal nota **Jafna færslur** á aðgerðasvæðinu.
7.  Skrá reikning eftir ap lánardrottinn skilar vörum eða þjónustu. Ef fyrirframgreiðsla er jöfnuð við innkaupapöntun eða sölupöntun í skrefi 6, er fyrirframgreiðsla sjálfkrafa jaöfnuð við reikning sem þú stofnaðir. Ef fyrirframgreiðsla er ekki jöfnuð við innkaupapöntun eða sölupöntun, geturðu jafnað handvirkt við reikninginn með því að nota **Jafna færslur** síðu viðskiptavinar eða lánardrottins. Upphæð fyrirframgreiðslu er síðan bakfærð úr tímabundna AP/AR fjárhagslykli. Þar að auki, ef skattar voru reiknuð eru þeir bakfærðar, vegna þess að reikningurinn hefur raunverulega skatta.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Yfirlit yfir reikningsfærsluferli fyrirframgreiðslu
Fyrirframgreiðslureikningar er algengur viðskiptaháttur. Lánardrottinn gefur út fyrirframgreiðslureikning til að krefjast innistæðu á kaupunum áður en innkaupapöntun er uppfyllt. Til dæmis gætu súmir lánardrottnar krafist fyrirframgreiðslu fyrir sérsniðna vörur eða þjónustu. Ef lánardrottni gefur út reikning sem biður um fyrirframgreiðslu, er hægt að nota eiginleikann reikningsfærslur fyrirframgreiðslu. Hægt er að skilgreina gildi fyrirframgreiðslu í innkaupapöntuninni, fyrirframgreiðslureikning er skráð og greidd, og síðan fyrirframgreiddum reikningi beitt á lokareikningur. Til að stofna fyrirframgreiðslu skal fylgja eftirfarandi skrefum:

1.  Innkaupaaðilinn stofnar staðfestir og sendir svo hefur innkaupapöntun sem lánardrottinn hefur beðið um fyrirframgreiðslu fyrir. fyrirframgreiðslugildi er skilgreint í innkaupapöntuninni. sem hluti af samkomulaginu.
2.  Lánardrottinn sendir inn fyrirframgreiðslureikning.
3.  Samræmingaraðili viðskiptaskulda skráir fyrirframgreiðslureikning gagnvart innkaupapöntun, og síðan er fyrirframgreiðslureikningur greiddur.
4.  Lánardrottinn sendir beiðni um greiðslu, sem vísað er til sem staðlaður reikningur lánardrottins. Eftir að lánardrottinn afhendir vörum eða þjónustu, og tengdir staðlaðir reikningar lánardrottna hafa borist, beitir samræmingaraðili viðskiptaskulda upphæð fyrirframgreiðslu sem var þegar greidd gegn staðlaða reikningnum.
5.  Samræmingaraðili viðskiptaskulda greiðir og jafnar eftirstandandi upphæð staðlaða reikningsins.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Setja upp færibreytur til að virkja reikningsfærsluferli fyrirframgreiðslu
Tilgreina verður lykil fyrirframgreiðslu í flipanum **Innkaupapöntun** á síðunni **Birgðabókun** (**Birgðastjórnun \> Uppsetning \> Bókun \> Bókun**). Fyrirframgreiðslulykillinn verður uppfærður, yfirleitt debetfærður, þegar fyrirframgreiðslureikningurinn er bókaður. Inneign á fyrirframgreiðslulyklinum verður bakfærð þegar venjulegi reikningurinn sem notaður er í fyrirframgreiðslureikningi er bókaður. Ef fyrirframgreiðslureikningur er ekki jafnaður við greiðslu áður en fyrirframgreiðslureikningurinn er notaður sem staðlaður reikningur, verða bókhaldsfærslurnar úr bókuðum fyrirframgreiðslureikningi bakfærðar þegar staðlaði reikningurinn er bókaður.

Mótfærslulykill fyrir samantekt viðskiptaskulda er skilgreindur í **Bókunarreglu lánardrottins**. Til að skilgreina sjálfgefnar bókunarforstillingar skal smella á **Viðskiptaskuldir \>Uppsetning \> Færibreytur viðskiptaskulda \>Flipi fjárhags og söluskatts \> Bókunarregla með fyrirframgreiddum reikningi lánardrottins**.

**Regla um notkun fyrirframgreiðslu** gefur til kynna hvort kerfið muni sjálfkrafa nota jafnaða fyrirframgreiðslureikninga í lokareikningnum sem var stofnaður handvirkt. Reikningar sem eru búnir til með gagnaeiningu vísa ekki í **Reglu um notkun fyrirframgreiðslu**. Setja þarf handvirkt jafnaða fyrirframgreiðslureikninga á reikninga sem voru búnir til með gagnaeiningu. Til að skilgreina regluna skal fara í **Viðskiptaskuldir \>Uppsetning \> Færibreytur viðskiptaskulda \> Flipi fjárhags og söluskatts \> Regla um notkun fyrirframgreiðslu**. Ef reiturinn **Regla um notkun fyrirframgreiðslu** er stilltur á **Sjálfvirkt** verður fyrirframgreiðslureikningurinn sjálfkrafa merktur fyrir jöfnun við lokareikninginn. Ef reiturinn er stilltur á **Tilkynningu** birtist merki um að fyrirframgreiðslureikningur sé tiltækur til notkunar þegar lokareikningur er stofnaður.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Stofna innkaupapöntun sem inniheldur upplýsingar um fyrirframgreiðslureikning
Þegar lánardrottinn segir þér að hann krefjist fyrirframgreiðslu fyrir vörur og þjónustu sem er í innkaupapöntun verður að skilgreina fyrirframgreiðsluvirði fyrir tengda innkaupapöntun. Opnið **Viðskiptaskuldir \> Almennt \> Innkaupapantanir \> Allar innkaupapantanir** og finnið innkaupapöntun lánardrottins. Á aðgerðasvæðinu skal velja flipann **Innkaup** og síðan velja **Fyrirframgreiðsla**. Færið inn upplýsingar um fyrirframgreiðsluna, þar með talið lýsingu, virði fyrirframgreiðslunnar, hvort fyrirframgreiðsla er föst upphæð eða prósenta og kenni fyrirframgreiðslu tegund. 

Athugið að margar skilgreiningar fyrirframgreiðslu í innkaupapöntun eru ekki leyfðar. Ef leyfa þarf margar fyrirframgreiðslur í innkaupapöntun skal bóka greiðslurnar með greiðslubókinni í stað fyrirframgreiðslureiknings.

Fyrirframgreiðslan kann að vera fjarlægð úr innkaupapöntuninni nema þú hafir þegar jafnað greiðslu á móti bókuðum fyrirframgreiðslureikningi eða bókuðum stöðluðum reikningi. Til að fjarlægja upplýsingar um fyrirframgreiðslu úr innkaupapöntuninni skal velja **Viðskiptaskuldir \> Almennt \> Innkaupapantanir \> Allar innkaupapantanir** og finnið innkaupapöntun lánardrottins. Á aðgerðasvæðinu skal velja flipann **Innkaup** og síðan velja **Fjarlægja fyrirframgreiðslu**.

## <a name="create-and-post-a-prepayment-invoice"></a>Stofna og bóka fyrirframgreiðslureikning
Til að skrá fyrirframgreiðslureikning lánardrottins skal fara á síðuna **Reikningur lánardrottins** með því að velja valkostinn **Fyrirframgreiðslureikningur** á síðunni **Innkaupapantanir** (**Viðskiptaskuldir \> Almennt \> Innkaupapantanir \> Allar innkaupapantanir \> Reikningsflipi \> Fyrirframgreiðslureikningur**). Færið inn upplýsingar fyrir fyrirframgreiðslureikninginn, þ.m.t. reikningsnúmerið. Ekki er hægt að breyta magni fyrir fyrirframgreiðslureikning. Ef lánardrottinn hefur reikningsfært upphæð að hluta til fyrir virði fyrirframgreiðslunnar sem skilgreint er í innkaupapöntuninni er hægt að uppfæra einingarverðið til að endurspegla hlutavirðið.

Þegar fyrirframgreiðslureikningurinn er bókaður verður inneign lánardrottins og lykill fyrirframgreiðslunnar uppfært. Virðið fyrir **Nota í fyrirframgreiðslu** í skilgreiningu fyrirframgreiðslunnar sem er að finna í innkaupapöntuninni verður einnig uppfært. Sjálfgefnar fjárhagsvíddarfærslur fyrir bókaða fylgiskjal fyrirframgreiðslunnar verið tekið úr upplýsingum í haus innkaupapöntunarinnar.

Ef **Læsa fjárhagsvíddum í reikningslínum á fyrirframgreiðslureikningi lánardrottins** eiginleikinn á síðunni **Eiginleikastjórnun** er virkur er ekki hægt að uppfæra víddir í haus eða línum fyrirframgreiðslu. 

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Bóka og jafna greiðslur fyrir fyrirframgreiðslureikning
Næst verður fyrirframgreiðslureikningurinn greiddur af síðunni **Greiðslubók**. Til að opna greiðslubækur skal smella á **Viðskiptaskuldir \> Færslubækur \> Greiðslur \> Greiðslubók**. Þegar jöfnun greiðslunnar hefur verið bókuð á fyrirframgreiðslureikninginn verður virðið fyrir **Eftirstöðvar fyrirframgreiðslu** í innkaupapöntuninni uppfært.

Áður en staðlaði reikningurinn er bókaður fyrir fyrirframgreiðslureikninginn er hægt að bakfæra jöfnunina á greiðslunni í gegnum fyrirframgreiðslureikninginn. Hinsvegar, þegar staðlaður reikningur er notaður í fyrirframgreiðslureikningnum, verður ekki hægt að bakfæra greiðslujöfnunina í gegnum fyrirframgreiðslureikninginn.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Bóka staðlaðan reikning lánardrottins fyrir innkaupapöntunina og notið fyrirframgreiðslureikninginn á staðlaða reikninginn
Skrá venjulegan reikning frá lánardrottni. Sem hluti af þessu ferli er hægt að nota jafnaðan fyrirframgreiðslureikning í reikning lánardrottins þannig að virði reikningsins verður minnkað um upphæðina sem hefur þegar verið greidd. Ef fyrirframgreiðslureikningurinn er notaður í reikningi lánardrottins mun það tryggja að bókhaldsfærslur úr fyrirframgreiðslureikningnum verði bakfærðar.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Notkun fyrirframgreiðslureikningsins eftir bókun staðlaða reikningsins
Ef gleymist að nota fyrirframgreiðsluna í stöðluðum reikningi lánardrottins þegar reikningur lánardrottins er bókaður, verður jöfnuð fyrirframgreiðsla tiltæk til notkunar á öðrum reikningum frá þessum lánardrottni á síðunni **Lánardrottnar** (**Viðskiptaskuldir \> Almennt \> Lánardrottnar \> Allir lánardrottnar \> Reikningsflipi \> Nota**).

## <a name="reversal-of-the-prepayment-application-process"></a>Bakfærsla á notkunarferli fyrirframgreiðslu
Ef þarf að ójafna eða bakfæra notkun fyrirframgreiðslureiknings í gegnum staðlaðan reikning skal velja aðgerðina **Bakfæra** á síðunni **Lánardrottnar** (**Viðskiptaskuldir \> Almennt \> Lánardrottnar \> Allir lánardrottnar \> Reikningsflipi \> Bakfæra**). Þegar notkun fyrirframgreiðslunnar er bakfærð er hægt að nota fyrirframgreiðsluna á annan staðlaðan reikning. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
