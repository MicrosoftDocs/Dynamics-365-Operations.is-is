---
title: Sjálfgefnar fjárhagsvíddir í fjárhagsbókum
description: Þessi grein lýsir reglunum sem skilgreina það hvernig fjárhagsvíddargildi eru stillt í færslum sem eru færðar inn í gegnum fjárhagsbækur. Þar er einnig að finna upplýsingar um aðstæður þar sem fastar víddir eru notaðar.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d0fcf836e22207baae562801fb082d735df0f96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907923"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Sjálfgefnar fjárhagsvíddir í fjárhagsbókum

[!include [banner](../includes/banner.md)]

Þessi grein lýsir reglunum sem skilgreina það hvernig fjárhagsvíddargildi eru stillt í færslum sem eru færðar inn í gegnum fjárhagsbækur (en ekki í gegnum birgða- eða verkbækur). Þar er einnig að finna upplýsingar um aðstæður þar sem fastar víddir eru notaðar.

## <a name="symptom"></a>Einkenni

Fjárhagsvíddargildi eru ekki stillt eins og gert er ráð fyrir á lykli eða mótlykli í fjárhagsbók. Eftirfarandi eru tvö dæmi um aðstæður:

Fylgiskjal er fært inn í færslubók eða almenna færslubók. Lykillinn er lánardrottnalykill og mótlykillinn er bankareikningur. Fjárhagsvíddir lánardrottins eru færðar inn sjálfgefið á lyklinum en fjárhagsvíddir bankans eru ekki færðar inn sjálfgefið á mótlyklinum. Þess í stað eru víddargildin frá lyklinum færð inn sjálfgefið á mótlyklinum.

Viðskiptavinur er með sjálfgefin fjárhagsvíddargildi úthlutuð og aðallykill tekna er með fast víddargildi úthlutað fyrir fjárhagsvídd deildar. Fylgiskjal er fært inn í almenna færslubók.  Lykillinn er viðskiptavinurinn og mótlykillinn er fjárhagslykill, sérstaklega tekjulykillinn með fasta víddargildið. Fasta víddin er ekki stillt á mótlyklinum fyrir aðallykil tekna. Þess í stað er hún stillt á víddargildi deildar lykilsins sem fengið er frá viðskiptavininum.  Þegar búið er að bóka fylgiskjalið er fasta víddargildið notað á bókuðu bókhaldsfærsluna en fylgiskjalið sýnir áfram deildargildi viðskiptavinarins á tekjulyklinum. 

Hvaða reglum er fylgt varðandi fjárhagsvíddargildi sem eru stillt á fylgiskjölum í færslubók?

## <a name="resolution"></a>Upplausn

Eftirfarandi reglum er fylgt til að færa inn fjárhagsvíddargildi sjálfgefið í línum fylgiskjals í fjárhagsbókum, t.d. í almennri færslubók eða reikningabók lánardrottins. 

1. **Færslubókarhaus**

   - Víddir færslubókarhauss eru færðar inn sjálfgefið úr víddum færslubókarheitis.

2. **Lykill færslubókarlínu**

   - Lyklavíddir færslubókarlínu eru færðar inn sjálfgefið úr víddum færslubókarhauss.
   - Ef einhverjar fjárhagsvíddir eru auðar eru gildi þeirra færð inn sjálfgefið frá viðskiptavini, lánardrottni, banka, eign, verki eða fjárhagsvíddum.

     - Ef gerð lykils er **fjárhagslykill** er farið með eign á fjárhagslykli sem sjálfgefna vídd við skráningu færslu.
     - Ef gerð lykils er **viðskiptavinur**, **lánardrottinn**, **banki**, **eign** eða **verk** er ekki hægt að ákvarða aðallykilinn. Þess vegna verður föst vídd aldrei færð sjálfgefið inn fyrir lykilinn.

3. **Mótlykill færslubókarlínu**

 - Fyrst eru víddir mótlykils færslubókarlínu sjálfgefið úr lyklavíddum færslubókarlína.

 - Ef einhverjar fjárhagsvíddir eru auðar er næsta sjálfgefna færsla fengin úr sjálfgefnum víddum viðskiptavinar, lánardrottins, banka, eigna, verks eða fjárhags.
   1. Ef gerð mótlykils er **Fjárhagslykill** er farið með eign á fjárhagslykli sem sjálfgefna vídd við skráningu færslu. Ef víddargildi var þegar fært sjálfgefið inn af lyklinum hnekkir sjálfgefin eða föst vídd aðallykilsins ekki fyrirliggjandi gildi.
   2. Ef gerð mótlykils er **viðskiptavinur**, **lánardrottinn**, **banki**, **eignir** eða **verk** er aðallykillinn enn óþekktur og því verður föst vídd aldrei sjálfgefin fyrir mótlykilinn.

4. **Bókun**

    1. Þegar bókun er gerð er aðallykill hverrar línu bókhaldsfærslunnar (bæði fyrir lykilinn og mótlykilinn) metinn til að ákvarða hvort fast víddargildi sé til staðar. Ef fast víddargildi er skilgreint kemur það í stað allra fyrirliggjandi og auðra gilda.

        Fasta víddargildið birtist **ekki** í færslubókarlínunum eftir bókun. Þess í stað birtist það í bókhaldsfærslunni þegar fylgiskjalið er skoðað eftir bókun þess.

    2. Engin önnur víddargildi eru færð sjálfgefið inn við bókun, þ.m.t. viðbótarfjárhagslyklar sem kann að vera bætt við þegar bókað er, t.d. aurasléttunarlyklar og gjalddagalyklar innan samstæðu. Sjálfgefnar víddarfærslur annarra fjárhagslykla er fengnar frá lykli eða mótlyklum.

Hvað viðkemur því að færa víddargildi sjálfgefið inn getur sjálfgefið færslubókarferli ekki ákvarðað hvort autt víddargildi sé autt af ásettu ráði eða hvort sjálfgefna færslan hafi ekki átt sér stað. Ef víddargildi er autt af ásettu ráði er hugsanlegt að gildi verði samt fært sjálfgefið inn með sjálfgildisröðinni sem var lýst hér á undan. Sé þess krafist að vídd hafi autt gildi gæti þurft að búa til vídd með gildið **0** (núll) eða **autt** svo að hægt sé að nota viðkomandi vídd í staðinn fyrir auða vídd.

Yfirfara skal eftirfarandi aðstæður til að sjá dæmi um sjálfgildisröð fjárhagsvídda.

### <a name="scenario-1"></a>Aðstæður 1

Farið í **fjárhagur \> uppsetning færslubókar \> heiti færslubókar** og veljið færslubókarheitið **GenJrn**. Á flýtiflipanum **Fjárhagsvíddir** skal því næst skilgreina eftirfarandi gildi fyrir sjálfgefnar fjárhagsvíddir:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Síða færslubókaheita](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Farið í **Fjárhagur \> Færslubókarfærslur \> Almenn færslubók** og búið til nýja almenna færslubók sem notar færslubókarheitið **GenJrn**. Víddirnar eru færðar sjálfgefið inn úr færslubókarheitinu (LedgerJournalName tafla) í færslubókarhausinn (LedgerJournalTable tafla) eins og sýnt er á flipanum **fjárhagsvíddir**.

[![Flipinn „Fjárhagsvíddir“ á síðunni „Almennar færslubækur“](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Farið í **línurnar**. Í reitnum **gerð lykils** skal velja **fjárhagur**, svo skal fara í reitinn **lykill** og slá inn **170150**. Ýtið síðan á **dálkalykilinn** til að fara úr reitnum. Víddirnar eru færðar inn sjálfgefið úr færslubókarhausnum. Þess vegna birtist gildið **Lykill** sem **170150-001-024**.

[![Færslubókarlínur fyrir almenna færslubók á síðunni „Færslubókarfylgiskjal“](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Breytið gildi **Lykill** í **170150-001-023**. Færið annaðhvort inn debetupphæð eða upphæð inneignar. Í reitnum **gerð mótlykils** skal velja **fjárhagur**, svo skal fara í reitinn **mótlykill** og slá inn **600150**. Víddargildin eru færð sjálfkrafa inn frá lyklinum. Þess vegna birtist gildið **Mótlykill** sem **600150-001-023**.

### <a name="scenario-2"></a>Aðstæður 2

Notið sömu fjárhagsvíddir og voru skilgreindar fyrir færslubókarheitið í aðstæðum 1. Farið svo í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir** og skilgreinið sjálfgefin fjárhagsvíddargildi fyrir viðskiptavin US-001. Veljið viðskiptavin til að opna upplýsingar um viðskiptavin. Á flipanum **fjárhagsvíddir** skal halda sjálfgildi víddarinnar **BUSINESSUNIT** (**001**). Bætið við víddinni **COSTCENTER** og sláið inn gildið **007**.

Búið til nýja almenna færslubók sem notar færslubókarheitið **GenJrn**. Á flipanum **fjárhagsvíddir** skal breyta sjálfgildi **BUSINESSUNIT** úr **001** í **002**.

Farið í **línurnar**. Á svæðinu **Gerð lykils** skal velja **Viðskiptavinur**, svo skal fara í svæðið **Lykill** og slá inn **US-001**. Til að skoða fjárhagsvíddir fyrir lykla sem eru ekki fjárhagslyklar skal velja **fjárhagsvíddir \> lykill**. Eftirfarandi sjálfgefnar færslur fyrir fjárhagsvíddargildi eru færðar inn:

- **BUSINESSUNIT:** 002 – sjálfgefna færslan kemur úr færslubókarhausnum. Gildið **001** er ekki fært sjálfgefið inn frá viðskiptavini US-001 vegna þess að sjálfgefið gildi var þegar fært inn.
- **COSTCENTER:** 007 – sjálfgefna færslan kemur úr uppsetningu viðskiptavinar US-001.
- **DEPARTMENT:** 024 – sjálfgefna færslan kemur úr færslubókarhausnum.

Nú skal fara aftur í línuna **Gerð mótlykils**, velja **Fjárhagur**, fara svo á svæðið **Mótlykill** og slá inn **600150**. Eftirfarandi sjálfgefin fjárhagsvíddargildi eru færð inn í línunni:

- **BUSINESSUNIT:** 002 – sjálfgefna færslan kemur úr fjárhagsvíddum lykilsins. (Hún var upprunalega færð inn sjálfgefið úr færslubókarhausnum.)
- **DEPARTMENT:** 024 – sjálfgefna færslan kemur úr fjárhagsvíddum lykilsins. (Hún var upprunalega færð inn sjálfgefið úr færslubókarhausnum.)
- **COSTCENTER:** 007 – sjálfgefna færslan kemur úr fjárhagsvíddum lykilsins. (Hún var upprunalega færð sjálfgefið inn frá viðskiptavininum.)

### <a name="scenario-3"></a>Aðstæður 3

Bætið við nýrri línu í sömu færslubók og notuð var í aðstæðum 2. Í reitnum **gerð lykils** skal velja **fjárhagur**, svo skal fara í reitinn **lykill** og slá inn **170150**. Hreinsið sjálfgefin víddargildi svo að aðeins aðallykillinn 170150 sé eftir. Í reitnum **gerð mótlykils** skal velja **viðskiptavinur**, svo skal fara í reitinn **mótlykill** og slá inn **US-001**. Eftirfarandi sjálfgefnar færslur fyrir fjárhagsvíddargildi eru færðar inn:

- **BUSINESSUNIT:** 002 – sjálfgefna færslan kemur úr færslubókarhausnum vegna þess að víddargildi lykils er autt. Gildið **001** er ekki fært sjálfgefið inn frá viðskiptavini US-001 vegna þess sjálfgefið gildi var þegar fært inn úr færslubókarhausnum. Ef gildið **BUSINESSUNIT** var haft autt af ásettu ráði þarf einnig að fjarlægja fjárhagsvíddina á mótlyklinum.
- **COSTCENTER:** 007 – sjálfgefna færslan kemur frá viðskiptavini US-001 vegna þess að víddargildi lykils og víddargildi færslubókarhauss eru auð. Ef gildið **COSTCENTER** var haft autt af ásettu ráði þarf einnig að fjarlægja fjárhagsvíddirnar á mótlyklinum.
- **DEPARTMENT:** 024 – sjálfgefna færslan kemur úr færslubókarhausnum vegna þess að víddargildi lykils er autt. Ef gildið **DEPARTMENT** var haft autt af ásettu ráði þarf einnig að fjarlægja fjárhagsvíddina á mótlyklinum.

### <a name="scenario-4"></a>Aðstæður 4

Notið sömu sjálfgefnu fjárhagsvíddargildi og voru skilgreind fyrir færslubókarheitið og viðskiptavin í aðstæðum 1 og 2. Næst skal skilgreina fast víddargildi fyrir víddina **BUSINESSUNIT** á aðallyklinum 170150. Farðu í **Fjárhag \> Bókhaldslyklar \> Lyklar \> Aðallyklar**. Í reitnum **aðallykill** skal velja **170150**, farið svo á flipann **hnekkingar lögaðila** og veljið **bæta við**. Veljið **USMF** sem lögaðila og veljið svo **bæta við**. Veljið viðkomandi færslu og veljið svo **Sjálfgefnar víddir**. Breytið víddinni **BUSINESSUNIT** í **fast gildi** og sláið inn **003** sem gildið.

Búið til nýja almenna færslubók sem notar færslubókarheitið **GenJrn**. Á flipanum **Fjárhagsvíddir** skal fjarlægja öll sjálfgefin víddargildi.

Farið í **línurnar**. Í reitnum **gerð lykils** skal velja **fjárhagur**, svo skal fara í reitinn **lykill** og slá inn **170150**. Ýtið síðan á **dálkalykilinn** til að fara úr reitnum. Víddargildin eru færð sjálfkrafa inn úr uppsetningu aðallykilsins fyrir reikninginn 170150. Þess vegna birtist gildið **Lykill** sem **170150-003-**.

Breytið gildinu **Lykill** í **170150-004-**. **Færslubókareiginleikinn kemur ekki í veg fyrir að föstu víddargildi sé breytt.** Færið annaðhvort inn debetupphæð eða upphæð inneignar. Í reitnum **Gerð mótlykils** skal velja **Fjárhagur**, svo skal fara í reitinn **Mótlykill** og slá inn **170250**. Fjárhagsvíddargildið 004 er fært inn sem sjálfgefið úr lyklinum. Bókið því næst skjalið. Í færslubókinni skal velja **Fylgiskjal**. Athugið að gildið **BUSINESSUNIT** breyttist aftur í fasta víddargildið **003** við bókunina.

Þegar farið er aftur í fylgiskjal færslubókarinnar endurspeglar **BUSINESSUNIT** víddin **ekki** fasta víddargildið. Hún hefur alltaf sama gildi og birtist á skjánum áður en bókað er. Bókunarferlið breytir engu sem fært er inn í fylgiskjalið. Aðeins bókhaldsfærslunni er breytt við bókun.

## <a name="developer-notes"></a>Athugasemdir fyrir forritara

Ef þú ert forritari og vilt skoða kóðann fyrir sjálfgildisferlið skaltu skoða eftirfarandi aðferðir:

- **LedgerJournalEngine.accountModified()** – þessi aðferð er aðalaðgangsstaðurinn fyrir sjálfgildisferli aðallyklavídda sem eru staðlaðar í öllum færslubókum (og er hnekkt af sumum færslubókargerðum).
- **LedgerJournalEngine.offsetAccountModified()** – þessi aðferð er aðalaðgangsstaðurinn fyrir sjálfgildisferli mótlyklavídda.
