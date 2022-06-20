---
title: Fjárhagsvíddir og bókanir
description: Þegar þú áætlar og setur upp bókhaldslykil, þarftu að íhuga hvernig hinir ýmsu hlutar koma til með að vinna saman þegar þú bókar skjal eða færslu. Á meðal þessara hluta eru lykilskipulag, ítarlegar reglur, og afstemmdar og fastar víddir. Þessi grein útskýrir hvað hver íhluti er og hvernig íhlutirnir vinna saman.
author: aprilolson
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a165c4084a9f2075a54c99a7e4913a4e3c3dfe55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910114"
---
# <a name="financial-dimensions-and-posting"></a>Fjárhagsvíddir og bókanir 

[!include [banner](../includes/banner.md)]

Þegar þú áætlar og setur upp bókhaldslykil, þarftu að íhuga hvernig hinir ýmsu hlutar koma til með að vinna saman þegar þú bókar skjal eða færslu. Á meðal þessara hluta eru lykilskipulag, ítarlegar reglur, og afstemmdar og fastar víddir. Þessi grein útskýrir hvað hver íhluti er og hvernig íhlutirnir vinna saman.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Bókhaldslykill og hlutar fjárhagsvídda

Ríkulegt, reglubundið kerfi er nota til að skilgreina gildar samsetningar aðallykla og fjárhagsvíddargilda. Þessi kafli inniheldur stutt yfirlit yfir virkni hvers hluta fyrir sig og útskýrir hvar má finna hlutann.

### <a name="account-structures"></a>Lykilskipulag

Krafist er lykilskipulags þegar þú setur upp fjárhaginn þinn. Nauðsynlegt er að skilgreina og virkja að minnsta kosti eitt lykilskipulag og úthluta því til fjárhagsins. Lykilskipulagið verður að innihalda aðallykil. Hægt er að skilgreina þá röð hluta sem virkar best fyrir fyrirtækið. Eftir að aðallykill hefur verið skilgreindur, getur kerfið ákvarðað hvaða lykilskipulag skal nota. Með því að setja aðallykilinn fremst eða nálægt fremsta hluta skipulags, geturðu hjálpað til við að takmarka gildin og einnig aðstoðað kerfið við að nota síðasta þekkta gildið sem sjálfgildi. Hægt að hafa allt að 10 fjárhagsvíddir aukalega í lykilskipulaginu. Lykilskipulagið skilgreinir hvaða víddargildi eru gild í samsetningu þeirra og annarra gilda. Það skilgreinir einnig hvort færa þarf inn víddargildin.

### <a name="advanced-rules"></a>Ítarlegar reglur

Ítarlegar reglur eru valfrjáls hluti þegar þú setur upp bókhaldslyklana. Hægt er að bæta við lykilskipulagið eins mörgum ítarlegum reglum og þú vilt. Ítarlegar reglur eru oft notaðar til að fást við tilfelli þar sem ákveðin skilyrði eru uppfyllt og nauðsynlegt verður að rekja auka fjárhagsvíddir. Ef þú notar t.d. reikning fyrir ferðakostnað, gætirðu viljað rekja aukalegar upplýsingar t.d. um þann viðburð sem ferðalag starfsmannsins snýst um. Ef ítarlegu reglurnar eru margar, raðast þær upp í stafrófsröð, út frá heitum reglnanna. Þeim hlutum sem reglur bæta við er aðeins hægt að úthluta á eftir hlutum lykilskipulagsins.

### <a name="balancing-dimension"></a>Afstemming víddar

Það er valfrjálst að skilgreina Afstemmingu fjárhagsvíddar. Á síðunni **Fjárhagur** er hægt að skilgreina fjárhagsvíddina sem á að afstemma. Hvenær sem færslur eru síðan bókaðar í þá fjárhagsvídd, stofnar og bókar kerfið sjálfkrafa færslur til að afstemma fjárhagsvíddina.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Sjálfgefin/föst fjárhagsvídd á aðallyklinum

Sjálfgefnar víddir koma frá ýmsum stöðum, eins og aðalfærslur (t.d. viðskiptamanna- eða lánadrottnafærslum), skjalahausum og aðallyklinum. Þessi grein fjallar um sjálfgefnar víddir á aðalreikningi eftir lögaðila. Hægt er að skilgreina hvort aðallykill hefur **Ekki fast** eða **Fast** gildi fyrir hverja fjárhagsvídd sem er notuð í öllu lykilskipulagi fyrir fjárhaginn. Ef fjárhagsvídd er **Ekki fast** nota hún sjálfgildi, en það gildi er hægt að skrifa yfir. Þessi hegðun á við öll sjálfgildi í kerfinu, jafnvel sjálfgildi sem koma frá aðalfærslum. Ef fjárhagsvídd er stillt á **Fast** gildi, er það gildi alltaf notað, hvort sem það kom einhversstaðar frá sem sjálfgildi eða notandinn færði það inn.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Sjálfgefnar víddir eru notaðar í ákveðinni röð á meðan bókun stendur

Fólk spyr gjarnan um röðina sem ýmsir hlutar eru keyrðir í. Mikilvægt er að þú skiljir röðina sem sjálfgefnar víddir eru notaðar í, því að þessi hegðun hefur áhrif á þá nálgun sem þú beitir í uppsetningu.

> [!NOTE]
> Þessar upplýsingar eiga aðeins við notkun sjálfgefinna vídda í forritinu. Ef flutt eru inn gögn með því að nota Microsoft Excel eða Data Management Framework, verður hegðunin mismunandi.

### <a name="example-1"></a>Dæmi 1

**Lykilskipulag**

| Aðallykill            | Viðskiptaeining           | Deild              | Kostnaðarstaður             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Öll gildi eru leyfð | Öll gildi eru leyfð | Öll gildi eru leyfð | Öll gildi eru leyfð |

**Aðallykill**

| Aðallykill | Nafn          | Lögaðili | Deild                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Afurðarsala | USMF         | Fast – 022 Sölu- og markaðsdeild |

Eftirfarandi myndskýring sýnir fasta sjálfgefna vídd sem er stillt á aðallykil 401100.

[![Sjálfgefnar fjárhagsvíddir.](./media/default-dimensions.png)](./media/default-dimensions.png)

Í þessu mjög svo einfalda dæmi, munum við færa inn almenna færslubók þar sem vídd deildarinnar er stillt á notkun sjálfgildisins **023** (Operations). Við munum færa inn og bóka fjárhagslykil. Eftirfarandi myndskýring sýnir fasta sjálfgefna fjárhagsvídd á fjárhagshausnum.

[![Almennar færslubækur.](./media/general-journal.png)](./media/general-journal.png)

Sjálfgefna víddin á færslubókarhausnum mun valda því að deild 023 verður notuð að sjálfgefnu í sölureikningslínunni. Eftirfarandi myndskýring sýnir línu almennrar færslubókar þar sem **023** sjálfgefið víddargildi frá hausnum er notað.

[![Fylgiskjal færslubókar.](./media/journal-voucher.png)](./media/journal-voucher.png)

Aftur á móti, þegar línan er bókuð, er fasta víddin notuð, og línan er bókuð til deildar 022. Eftirfarandi myndskýring sýnir bókað fylgiskjal, þar sem fasta víddin er notuð fyrir sölureikninginn.

[![Færslur fylgiskjals með fastar víddir jafnað.](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Dæmi 2

Þetta dæmi notar sömu uppsetningu og það fyrsta. Við munum aftur á móti bæta við öðrum hluta og nota vídd deildarinnar sem afstemmingarvídd. Í eftirfarandi myndskýringu er **Deild** stillt sem afstemming fjárhagsvídd fyrir USMF fjárhaginn.

[![Teikning sem sýnir deild sem afstemmda fjárhagsvídd.](./media/ledger.png)](./media/ledger.png)

Þegar sami færslubókarhaus uppsetning er notuð og sama færslan er bókuð, er fasta víddin notuð fyrst. Síðan er afstemmingarrökleiðsla notuð til að hjálpa til við að tryggja að sérhver deild hafi afstemmda færslu. Eftirfarandi myndskýring sýnir fylgiskjalsfærslur sem innihalda afstemmingarfærsluna eftir að fasta víddin er virkjuð.

.[![Færslur fylgiskjals eftir að mótfærsla er bókuð](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Dæmi 3

Í þessu dæmi munum við bæta ítarlegri reglu við. Ítarlega reglan tilgreinir að ef sölureikningur 401100 og deild 022 (sölu- og markaðsdeild) eru notuð, ætti kerfið að rekja aukahluta sem ber heitið Viðskiptavinur.

Þetta dæmi er mikilvægt vegna raðarinnar. Lykilskipulagið er ákvarðað eftir að búið er að færa inn aðallykilinn. Ef þú vísar í uppsetningu lykilskipulagsins, getur kerfið ákvarðað að aðallykillinn, viðskiptaeining, deild og kostnaðarstaður séu viðeigandi. Á þessum tímapunkti hefur ítarlega reglan ekki verið virkjuð, því að fastar víddir eru ekki notaðar fyrr en sjálfgefnar víddir hafa verið notaðar fyrir færslubókarfylgiskjal á meðan bókun stendur. Í eftirfarandi myndskýringu er Viðskiptavinahlutinn ekki sjáanlegur, vegna þess að skilyrði fyrir ítarlega reglu hafa ekki verið uppfyllt.

[![Fjárhagslykill.](./media/drop-down.png)](./media/drop-down.png)

Bókunin mun ekki heppnast, vegna þess að fasta víddin var notuð í lok ferlisins. Villuleit víddar ákvarðar að viðskiptavinahlutans sé krafist ef aðallykillinn er 401100 og deildin er 022. Bókun getur ekki átt sér stað vegna villu við villuleit. Eftirfarandi myndskýring sýnir skilaboðin sem birtast eftir að villuleit víddar ákvarðar að Viðskiptavinur er nauðsynlegur hluti.

[![Upplýsingar um skilaboð.](./media/message.png)](./media/message.png)

Í þessu dæmi þarf að skrifa yfir sjálfgildið svo að ítarlega reglan sé virkjuð og þú getir fært inn Viðskiptavinahlutann. Þessi lausn er þó ekki alltaf í boði, og sumir notendur vita ekki einu sinni af bókunarreglunum. Þess vegna er mikilvægt að skilja röðina sem sjálfgefnar víddir eru notaðar í þegar þú setur upp bókhaldslyklana þína.

Þú getur breytt grunnstillingunni á nokkra vegu, til að ná fram því sem þú vilt í þessu dæmi. Þú getur t.d. stofnað nýtt lykilskipulag fyrir sölureikninga og látið Viðskiptavinahlutann vera hluta af því skipulagi. Einnig er hægt að bæta við fyrirliggjandi lykilskipulag fleiri línum, og tilgreina aðallykilinn og gild deildargildi. Í viðbótar viðskiptavinaskipulagi gæti síðan verið gagnlegt að hafa annað reikningsskipulag fyrir sölureikninga þar sem Viðskiptavinahlutinn er nálægur.

## <a name="additional-resources"></a>Frekari upplýsingar 

Sum af eftirfarandi tilföngum vísa til fyrri útgáfu af hugbúnaðinum. Stór hluti upplýsinganna um notkun sjálfgefinna vídda og stór hluti hugtakanna eru sá sami og í fyrri útgáfunni og tilvísanirnar eru ennþá gildar.

[Jafnaðar færslubækur fyrir millieiningabókhald](example-balanced-journals-interunit-accounting.md)

[Yfirlit yfir bókhaldslykil](plan-chart-of-accounts.md) 

[Skipulagning bókhaldslykla í AX 2012 blogg](/archive/blogs/axsa/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7) – Þessi hlekkur fer til hluta 1 af sjö-hluta seríu.

[Sjálfgefni vídda í Dreifing á fjárhagsupphæð](/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-in-accounting-distributions-part-1-introduction)

[Sjálfgefni vídda í Víddir rammi](/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-part-1-financial-dimensions-discovery)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
