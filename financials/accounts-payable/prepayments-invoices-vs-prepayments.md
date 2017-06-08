---
title: "Fyrirframgreiðslureikninga miðað við fyrirframgreiðslur"
description: "Þessi grein veitir lýsir og ber saman aðferðirnar tvær sem fyrirtæki geta notað fyrir fyrirframgreiðslu (fyrirframgreiðslur). Með annarri aðferðinni er stofnaður fyrirframgreiðslureikningur sem er tengdur innkaupapöntun. Með hinni aðferðinni eru stofnuð fylgiskjöl fyrirframgreiðslu með því að stofna færslur í færslubók og merkja þær sem fylgiskjöl fyrirframgreiðslna."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4f127007cea1d8ccd0b4e9ea637f0674775278d
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="prepayment-invoices-vs-prepayments"></a>Fyrirframgreiðslureikninga miðað við fyrirframgreiðslur

[!include[banner](../includes/banner.md)]


Þessi grein veitir lýsir og ber saman aðferðirnar tvær sem fyrirtæki geta notað fyrir fyrirframgreiðslu (fyrirframgreiðslur). Með annarri aðferðinni er stofnaður fyrirframgreiðslureikningur sem er tengdur innkaupapöntun. Með hinni aðferðinni eru stofnuð fylgiskjöl fyrirframgreiðslu með því að stofna færslur í færslubók og merkja þær sem fylgiskjöl fyrirframgreiðslna.

Fyrirtæki gæti gefið út fyrirframgreiðslur (fyrirframgreiðsla) til lánardrottna fyrir vörur eða þjónustu áður en þær vörur eða þjónustu hafa verið uppfylltar. Hægt er að nota tvær aðferðir til að gefa út fyrirframgreiðslur til lánardrottna. Til að lágmarka áhættu, er hægt að rekja fyrirframgreiðslur með því að skilgreina fyrirframgreiðslu á innkaupapöntun. Fyrir þessa aðferð, verður að stofna fyrirframgreiddum reikningi sem er tengd innkaupapöntun. Þessi aðferð er kallað reikningsfærsla fyrirframgreiðslu. Fyrirtæki sem vilja ekki rekja fyrirframgreiðslur jafn náið eða fá ekki fyrirframgreiðslureikning frá lánardrottni þeirra geta nota fylgiskjöl fyrirframgreiðslna í stað reikningsfærsluaðferð fyrirframgreiðslu. Hægt er að stofna færslubókafylgiskjöl fyrirframgreiðslu með því að stofna færslur í færslubók og merkja þær sem fylgiskjöl fyrirframgreiðslna. Fyrir þessa aðferð er ekki hægt að rekja hvaða fyrirframgreiðslu til lánardrottins eru gerðar á móti hvaða innkaupapantanir. Hins vegar er hægt að merkja bókaða fyrirframgreiðslu fyrir jöfnun á móti innkaupapöntun.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Hvenær á að nota reikningsfærslu fyrirframgreiðslu miðað við fyrirframgreiðslur
| Fyrirframgreiðslurreikningsfærsla                                                                | Fyrirframgreiðslur                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Skilgreina gildi fyrirframgreiðslu í innkaupapöntuninni.                                    | Ekkert fyrirframgreiðslugildi er skilgreint í innkaupapöntuninni.                    |
| Lykill: Fyrirframgreiðslureikning  og endanlegam reikning verður að bóka.                       | Engin fyrirframgreiðslureikning verður að bóka.                                    |
| Skuld fyrir fyrirframgreiðsluna er geymt í lykli fyrirframgreiðslu, ekki AP lykli. | Skuld fyrir fyrirframgreiðsluna er geymt í AP lykil.                  |
| Staða lánardrottins endurspeglar ekki gildi fyrirframgreiðslu í gegnum ferlið.     | Staða lánardrottins endurspeglar gildi fyrirframgreiðslu í gegnum ferlið. |
| reikningsfærsla Fyrirframgreiðslu er aðeins tiltæk í Viðskiptaskuldir.                         | Fyrirframgreiðslur eru tiltækar í viðskiptaskuldum og viðskiptakröfum.    |

## <a name="overview-of-the-prepayment-process"></a>Yfirlit yfir fyrirframgreiðsluferlið
Bókhaldsvenjur í mörgum löndum/svæðum krefjast þess að fyrirframgreiðslur frá viðskiptavini eða til lánardrottins séu ekki bókaðar á venjulega safnlykla viðskiptavinar eða lánardrottins. Í staðinn eru þessar greiðslur bókaðar á sérstakan fjárhagslykil fyrir fyrirframgreiðslur. Þegar sölupöntun eða innkaupapöntun er gerð er reikningur gefinn út á viðskiptavin eða lánardrottin. Við greiðslu reikningsins er fyrirframgreiðslan og fyrirframgreiðsla VSK á fjárhagslyklum fyrirframgreiðslu bakfærðar og reikningsupphæðirnar eru sjálfvirkt bókaðar á venjulega safnlykla. Til að stofna fyrirframgreiðslu skal fylgja eftirfarandi skrefum:

1.  Setja upp bókunarreglur fyrir fyrirframgreiðslur
2.  Í Færibreytur viðskiptakrafna og Færibreytur lánardrottna, undir **Fjárhags og virðisaukaskatts**, veljið nýja bókunarreglu með því að nota **Bókunarregla með fyrirframgreiðslu fyrir greiðslubók** færibreyta.
3.  Stofnið greiðslubók og síðan að stofna nýja greiðslu.
4.  Hægt er að merkja greiðsluna sem fyrirframgreiðslu. Ef greiðsla er merkt sem fyrirframgreiðsla, greiðslan er bókuð í fjárhagslyklana sem eru skilgreindar í bókunarreglu sem er sett upp í skrefum 1 og 2. Þar að auki eru skattar reiknaðir, ef greiðsla er merkt sem fyrirframgreiðsla. Sumar yfirvöld krefjast þess að skattar séu greiddir þegar fyrirframgreiðsla er skráð, jafn vel þó enginn sé reikningurinn.
5.  Bókið fyrirframgreiðsluna
6.  Valfrjálst: Hægt er að jafna fyrirframgreiðsla við innkaupapöntun eða sölupöntun áður en reikningurinn er stofnaður. Á sölupöntun eða innkaupapöntun síðuskal nota **Jafna færslur** á aðgerðasvæðinu.
7.  Skrá reikning eftir ap lánardrottinn skilar vörum eða þjónustu. Ef fyrirframgreiðsla er jöfnuð við innkaupapöntun eða sölupöntun í skrefi 6, er fyrirframgreiðsla sjálfkrafa jaöfnuð við reikning sem þú stofnaðir. Ef fyrirframgreiðsla er ekki jöfnuð við innkaupapöntun eða sölupöntun, geturðu jafnað handvirkt við reikninginn með því að nota **Jafna færslur** síðu viðskiptavinar eða lánardrottins. Upphæð fyrirframgreiðslu er síðan bakfærð úr tímabundna AP/AR fjárhagslykli. Þar að auki, ef skattar voru reiknuð eru þeir bakfærðar, vegna þess að reikningurinn hefur raunverulega skatta.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Yfirlit yfir reikningsfærsluferli fyrirframgreiðslu
Fyrirframgreiðslureikningar er algengur viðskiptaháttur. Lánardrottinn gefur út fyrirframgreiðslureikning til að krefjast innistæðu á kaupunum áður en innkaupapöntun er uppfyllt. Til dæmis gætu súmir lánardrottnar krafist fyrirframgreiðslu fyrir sérsniðna vörur eða þjónustu. Ef lánardrottni gefur út reikning sem biður um fyrirframgreiðslu, er hægt að nota eiginleikann reikningsfærslur fyrirframgreiðslu. Hægt er að skilgreina gildi fyrirframgreiðslu í innkaupapöntuninni, fyrirframgreiðslureikning er skráð og greidd, og síðan fyrirframgreiddum reikningi beitt á lokareikningur. Til að stofna fyrirframgreiðslu skal fylgja eftirfarandi skrefum:

1.  Innkaupaaðilinn stofnar staðfestir og sendir svo hefur innkaupapöntun sem lánardrottinn hefur beðið um fyrirframgreiðslu fyrir. fyrirframgreiðslugildi er skilgreint í innkaupapöntuninni. sem hluti af samkomulaginu.
2.  Lánardrottinn sendir inn fyrirframgreiðslureikning.
3.  Samræmingaraðili viðskiptaskulda skráir fyrirframgreiðslureikning gagnvart innkaupapöntun, og síðan er fyrirframgreiðslureikningur greiddur.
4.  Eftir að lánardrottinn afhendir vörum eða þjónustu,  og tengdar reikningar lánardrottna hafa borist, beitir samræmingaraðili viðskiptaskulda upphæð fyrirframgreiðslu sem var þegar greidd gegn reikningnum.
5.  Samræmingaraðili viðskiptaskulda greiðir og jafnar eftirstandandi upphæð reikningsins.




