---
title: Tvöfaldur gjaldmiðill
description: Þetta umræðuefni veitir upplýsingar um tvöfaldan gjaldmiðil þar sem skýrslugjaldmiðillinn er notaður sem annar bókhaldsgjaldmiðill fyrir Microsoft Dynamics 365 Finance.
author: kweekley
manager: AnnBe
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 8b71b571b03e8fa2648c90258bbcaa020baeabc0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444228"
---
# <a name="dual-currency"></a>Tvöfaldur gjaldmiðill

[!include [banner](../includes/banner.md)]

Virkni sem kynnt var í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.1 (október 2018) gerir kleift að endurskipuleggja skýrslugjaldmiðilinn og nota sem annan bókhaldsgjaldmiðill. Þessi virkni er vísað til sem *tvöfalds gjaldmiðils*. Ekki er hægt að slökkva á breytingum fyrir tvöfaldan gjaldmiðil með skilgreiningarlykli eða færibreytu. Vegna þess að skýrslugjaldmiðillinn er notaður sem annar bókhaldsgjaldmiðill, breytist leiðin sem skýrslugjaldmiðillinn er reiknaður með bókunarrökunum.

Að auki hafa nokkrar einingar verið endurbættar til að fylgjast með, tilkynna og nota skýrslugjaldmiðilinn í ýmsum ferlum. Einingarnar sem verða fyrir áhrifum eru meðal annars:

- Fjárhagur 
- Fjárhagsskýrslugerð 
- Viðskiptaskuldir
- Viðskiptakröfur 
- Reiðufjár- og bankastjórnun 
- Eignir 
- Samstæður

Eftir uppfærslu verður þú að ljúka sérstökum skrefum fyrir reiðufjár- og bankastjórnun og eignir. Passaðu því að lesa og skilja viðeigandi hluta þessa efnis.

## <a name="posting-process"></a>Bókunarferli

Bókunarrökum hefur verið breytt í öllum færslum sem skapa bókhaldsfærslu til fjárhags. Hér er hvernig skýrslugjaldmiðill var reiknaður áður:

Færslugjaldmiðilsupphæð \> bókhaldsgjaldmiðilsupphæð \> skýrslugjaldmiðilsupphæð

Til dæmis er færsla færð í Kanadadalur (CAD) gjaldmiðil. CAD upphæð er þýdd í bókhaldsgjaldmiðli, sem er Bandaríkjadal (USD). USD upphæðin er síðan þýdd í skýrslugjaldmiðilinn, sem er evru (evrur). Því gengi krónunnar verður að vera á milli CAD og USD, og á milli USD og EUR.

Hér er nýr útreikningur:

Færslugjaldmiðilsupphæð \> bókhaldsgjaldmiðilsupphæð

Færslugjaldmiðilsupphæð \> skýrslugjaldmiðilsupphæð

Vegna þessa breytinga verður gengi nú að vera á milli CAD og USD og á milli CAD og EUR.

## <a name="reports-and-inquiries"></a>Skýrslur og fyrirspurnir

Ýmsar skýrslur og fyrirspurnir sýna nú bæði skýrslugjaldmiðilsupphæðir og bókhaldsgjaldmiðilsupphæðir. Ekki hefur verið uppfært í öllum skýrslum og fyrirspurnum. Til dæmis hafa skýrslur sem aðeins sýna upphæð í færslugjaldmiðli ekki breyst.

Breytingarnar fylgja einum af tveimur mynstri:

- Ef skýrslan eða fyrirspurnin átti nóg pláss til að sýna upphæðir bæði í bókhaldsgjaldmiðli og skýrslugjaldmiðli, var bókhaldsgjaldmiðilsupphæðunum bætt við.
- Ef skýrslan eða fyrirspurnin hafði ekki nóg pláss til að sýna magn í báðum gjaldmiðlum var valkostur bætt þannig að notendur geti valið hvaða gjaldmiðil er sýndur.

Fyrir ýmsar skýrslur og fyrirspurnir var rökum einnig bætt við til að bæla gjaldeyrisupphæðirnar ef skýrslugjaldmiðillinn er sá sami og bókhaldsgjaldmiðillinn, eða ef skýrslugjaldmiðillinn var ekki skilgreindur í fjárhagnum fyrir lögaðilann.

## <a name="financial-journals"></a>Fjárhagsbækur

Fjárhagsbækur, svo sem færslubók og reikningabók lánardrottins, hafa verið uppfærðar þannig að þær innihaldi viðbótarupplýsingar um skýrslugjaldmiðilinn. Heildarupphæð fyrir fylgiskjal og færslubók eru nú sýndar í skýrslugjaldmiðlinum. Auk þess, upplýsingar um gengi skýrslugjaldmiðilsins birtist nú á **Almennt** flipanum á færslubókarlínunum. Þess vegna getur þú hnekkt gengi gjaldmiðilsins í skýrslugjaldmiðli þegar þú slærð inn færslur.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Reikningar lánardrottna, sölupantanir og sölusamningar
Reikningar lánardrottna, sölupantanir og sölusamningar hafa verið uppfærð til að taka með fast gengi fyrir skýrslugjaldmiðilinn. Hægt er að skilgreina fast gengi fyrir bæði skýrslugjaldmiðil og bókhaldsgjaldmiðil þegar gjaldmiðill færslu er annar. Þegar bókhaldsgjaldmiðill og skýrslugjaldmiðill eru eins verður föstu gengi haldið í samstillingu með því að nota fast gengi bókhaldsgjaldmiðilsins sem fast gengi skýrslugjaldmiðilsins. Ekki er hægt að breyta föstu gengi skýrslugjaldmiðils fyrir þessa skilgreiningu. Þegar bókhaldsgjaldmiðill og skýrslugjaldmiðill eru mismunandi er hægt að skilgreina fast gengi fyrir bæði bókhaldsgjaldmiðil og skýrslugjaldmiðil við innslátt færslu. Ef skýrslugjaldmiðillinn hefur ekki verið skilgreindur í fjárhag er reiturinn **Fast gengi skýrslugjaldmiðils** ekki virkur og upphæð skýrslugjaldmiðils er reiknuð.

## <a name="module-changes"></a>Einingar breytingar

Eftirfarandi einingar nota skýrslugjaldmiðilinn sem annan bókhaldsgjaldmiðil:

- [Fjárhagur](#general-ledger)
- [Fjárhagsskýrslugerð](#financial-reporting)
- [Viðskiptaskuldir](#accounts-payable-and-accounts-receivable)
- [Viðskiptakröfur](#accounts-payable-and-accounts-receivable)
- [Reiðufjár- og bankastjórnun](#cash-and-bank-management)
- [Eignir](#fixed-assets)
- [Samstæður](#consolidations)

### <a name="general-ledger"></a>Fjárhagur

Ef skýrslugjaldmiðill var skilgreindur í fjárhag fylgdi fjárhagurinn þegar gjaldeyrisupphæðum í hverri bókhaldsfærslu. Hins vegar eru þessar fjárhæðir nú þýddar af færslugjaldmiðilsupphæðum.

Eftirfarandi viðbótar breytingar voru gerðar á **Fjárhag** einingu:

- Hægt er að skilgreina aðskilda gengisgerð fyrir skýrslugjaldmiðilinn í fjárhag. Ef fyrirtæki vill ekki nota annan gengisgerð geturðu skilið reitinn fyrir gerð gengis fyrir skýrslugjaldmiðilinn eftir auðann. Að öðrum kosti getur þú valið sömu gengisgerð sem er notuð fyrir bókhaldsgjaldmiðilinn. Ef þú sleppir reitnum velur kerfið gerð gengis fyrir bókhaldsgjaldmiðilinn.
- Ný færslubók, leiðréttingabók skýrslugjaldmiðils, gerir kleift að birta breytingar á fjárhagslyklum aðeins í skýrslugjaldmiðlinum. Þessi færslubók gerir þér kleift að birta aðeins fjárhagslykla. Það styður ekki innan samstæðu og gjaldmiðillinn verður að vera skýrslugjaldmiðill lögaðilans þar sem færslubókin er bókuð. Þegar færslubókin er bókuð er færslugjaldmiðilsupphæðirnar og bókhaldsgjaldmiðilsupphæðirnar 0 (núll) og skýrslugjaldmiðilsupphæðin er bókuð með upphæðinni sem er færðu inn í færsluna. Vegna þess að leiðin sem skýrslugjaldmiðillinn er notaður í einingum **Viðskiptaskuldir**, **Viðskiptakröfur** og **Eignir** hafa breyst, þessa færslubók er hægt að nota til að breyta eftir uppfærslu. Fyrir dæmi sem sýna hvernig hægt er að nota þessa færslubók, sjá kaflann fyrir þá einingar.
- Ferlið við úthlutun tímabila hefur verið uppfært þannig að það úthlutar fjárhæðum í færslunum, bókhaldi og skýrslugjaldmiðlum. Áður voru upphæðir úthlutað í færslugjaldmiðli og bókhaldsgjaldmiðli og síðan var bókhaldsgjaldmiðilsupphæðin þýdd í skýrslugjaldmiðilinn. Þessi hegðun gæti valdið því að staða sé áfram á fjárhagslyklinum í skýrslugjaldmiðlinum. Nú, þegar upphæðir eru reiknaðar og notaðar í bókhaldsfærslunni, er engin þýðing á sér stað.
- Ferlið við endurmetningu erlendra gjaldmiðla hefur þegar verið endurmetið upphæðir í skýrslugjaldmiðlinum. Hins vegar er skýrslugjaldmiðill reiknað nú með færslugjaldmiðilsupphæð, eins og lýst er í kaflanum [Bókunarferli](#posting-process) fyrr í þessu efni.
- Margir skýrslur og fyrirspurnir í fjárhag höfðu þegar skýrslugjaldmiðil, en nokkrir gerðu það ekki. Eitt dæmi er **Prófjöfnuður** listasíðan. Þessi listasíða inniheldur nú dálka bæði fyrir bókhaldsgjaldmiðilinn og skýrslugjaldmiðilinn. Athugaðu að dálkarnir fyrir skýrslugjaldmiðilinn eru falin ef bókhaldsgjaldmiðill og skýrslugjaldmiðill eru þau sömu eða ef engin skýrslugjaldmiðill var skilgreindur í fjárhag.

### <a name="financial-reporting"></a>Fjárhagsskýrslugerð

Aukahlutur í **fjárhagsskýrslugerð** gerir þér kleift að taka upp skýrslugjaldmiðilsupphæðir í fjárhagsskýrslum á tvo vegu. Í dálkskilgreiningunni er hægt að tilkynna beint um skýrslugjaldmiðilsupphæðir sem eru settar í fjárhag (ný virkni). Einnig er hægt að halda áfram að þýða upphæðir frá bókhaldsgjaldmiðlinum til skýrslugjaldmiðilsins (núverandi virkni).

Þessi breyting er í boði í gegnum **Birting gjaldmiðils** stillinguna í dálksskilgreiningunni. Ef þú velur **Skýrslugjaldmiðill úr fjárhag** eru upphæðir í dálknum ekki þýtt. Þess í stað eru þau tilkynnt beint frá fjárhag. Ef þú vilt fá dálkinn til að sýna þýddar upphæðir skaltu velja **Þýða í XXXX** valkostinn, þar sem *XXXX* er skýrslugjaldmiðillinn sem dálkurinn ætti að sýna. Í þessu tilviki verður skýrslugjaldmiðilsupphæðir þýtt í völdu gjaldmiðilinn með því að nota núverandi þýðingu.

### <a name="accounts-payable-and-accounts-receivable"></a>Viðskiptaskuldir og viðskiptakröfur

**Viðskiptaskuldir** og **Viðskiptakröfur** einingar sem nú þegar fylgst með skýrslugjaldmiðilsupphæðum. Hins vegar voru upphæðirnar ekki sýnt eða notað fyrir ýmis ferli. Eftirfarandi breytingar voru gerðar:

- Skýrslugjaldmiðilsupphæðir eru nú sýndar í færslum fyrir bæði viðskiptavini og lánardrottna. Skýrslugjaldmiðilsupphæðir eru einnig sýndar fyrir opnunarstöðu hverrar færslu.
- Aldursferillinn hefur verið uppfærð þannig að fyrirtæki geti skoðað öldrunarkörfurnar í annaðhvort bókhaldsgjaldmiðli eða skýrslugjaldmiðli.
- Ýmsar fyrirspurnir og skýrslur voru uppfærðar þannig að þeir birti skýrslugjaldmiðilsupphæðir. Dæmi eru **Fjárhagsafstemming til viðskiptavinar** og **Fjárhagsafstemming til lánardrottins** skýrslur.
- Ferlið við endurmetningu erlendra gjaldmiðla hefur þegar verið endurmetið upphæðir í skýrslugjaldmiðlinum. Hins vegar er skýrslugjaldmiðilsupphæð reiknað nú með færslugjaldmiðilsupphæð, eins og lýst er í [Bókunarferli](#posting-process) kafla.
- **Uppfærsluatriði:** Áður en uppfærsla er skýrslugjaldmiðilsupphæðin fyrir skjöl (reikninga, greiðslur osfrv.) reiknuð með bókhaldsgjaldmiðlinum. Til dæmis er reikningur bókaður fyrir uppfærslu fyrirtækisins og reikningurinn er ekki greiddur. Við uppfærslu er bókhaldsfærsla reikningsins ekki breytt. Hins vegar, eftir uppfærslu, eru breytingar fyrir tvöfalda gjaldmiðil í gildi. Því þegar greiðsla er tekin fyrir reikninginn er skýrslugjaldmiðill greiðslunnar nú reiknuð með færslugjaldmiðilsupphæðinni. Þegar greiðsla og reikningur eru jafnaðar getur verið reiknaður lítilsháttar mismunur í raunupphæðum ávinnings/tap vegna þess að skýrslugjaldmiðilsupphæðir eru nú reiknaðar á annan hátt. Ef mismunurinn, sem reiknað er með, er talinn verulegur, má nota nýju leiðréttingabók skýrslugjaldmiðils til að breyta stöðu raunupphæða ávinnings/taps og fjárhagslyklum viðskiptaskulda/viðskiptakrafa eingöngu í skýrslugjaldmiðlinum.

### <a name="cash-and-bank-management"></a>Reiðufjár- og bankastjórnun

Áður rakti **Reiðufjár- og bankastjórnun** einingin ekki skýrslugjaldmiðilsupphæðir vegna færslna sem voru bókaðar gegn hverjum bankareikningi. Eftir uppfærslu eru sjálfkrafa skýrslugjaldmiðilsupphæðir raktar fyrir nýjar færslur sem eru bókaðar. Hins vegar verður að bæta skýrslugjaldmiðilsupphæðum við áður bókaðar færslur í undirbók.

- **Uppfærsluatriði:** Vegna þess að færslur bankareikninga höfðu ekki áður fylgst með skýrslugjaldmiðilsupphæðum í undirbók, hefur leiðsagnarforriti verið bætt við þannig að þú getir bætt við skýrslugjaldmiðilsupphæðum við bankareikningsfærslur. Þetta leiðsagnarforrit bókar **ekki** aftur í fjárhag. Þess í stað tekur það skýrslugjaldmiðilsupphæðirnar úr fjárhag og uppfærir í töflum undirbókar.

    - Til að hefja leiðsagnarforritið, veldu **Reiðufjár- og bankastjórnun** \> **Setja upp** \> **Bæta skýrslugjaldmiðilsupphæðum við bankareikningsfærslur** .
    - Leiðsagnarforritið sýnir færslur fyrir alla bankareikninga í núverandi fyrirtæki sem hefur skýrslugjaldmiðilsupphæð 0 (núll). Aðeins færslur sem voru bókaðar fyrir uppfærslu eru innifalin.
    - Fyrir hverja bankareikningsfærslu finnur leiðsagnarforritið samsvarandi bókhaldsfærslur í fjárhag og færir inn sjálfgefna skýrslugjaldmiðilsupphæð. Þó að magn er hægt að breyta, mælum við með að þú **ekki** breyta þeim. Annars gæti verið að þú getir ekki stemmt upphæðir bankareikninganna við fjárhag. Eina skipti sem þú ættir að breyta upphæðinni ætti að vera ef ekki er hægt að finna skýrslugjaldmiðilinn í fjárhag. Í því tilfelli mun leiðsagnarforritið sýna magn 0 (núll) fyrir skýrslugjaldmiðilinn.
    - Ef þú velur **Hætta við** í leiðsagnarforritinu, eru bankareikningafærslur og allar breytingar á skýrslugjaldmiðilsupphæðunum vistuð þangað til næst þegar þú ræsir leiðsagnarforritið. Hins vegar eru skýrslugjaldmiðilsupphæðir ekki uppfærðar á bankareikningafærslunum. Þessi uppfærsla verður aðeins þegar þú velur **Ljúka** í leiðsagnarforritinu. Þú getur keyrt leiðsagnarforritið oft. Þess vegna getur þú lagað allar rangar skýrslugjaldmiðilsupphæðir ef þú gerir mistök.

- Engar ferli í reiðufjár- og bankastjórnun voru breytt, en ýmsar skýrslur og fyrirspurnir voru uppfærðar þannig að þeir birti skýrslugjaldmiðilsupphæðir. Sjóðstreymisspár er undantekning. Þau voru ekki uppfærð til að innihalda skýrslugjaldmiðilsupphæðir.

### <a name="fixed-assets"></a>Eignir

Áður röktu **Eignir** ekki skýrslugjaldmiðilsupphæðir fyrir færslur sem voru bókaðar gegn hverri eignabók. Eftir uppfærslu eru sjálfkrafa skýrslugjaldmiðilsupphæðir raktar fyrir nýjar færslur sem eru bókaðar. Hins vegar verður að bæta skýrslugjaldmiðilsupphæðum við áður bókaðar færslur í undirbók.

Að auki hafa verulegar breytingar verið gerðar á afskriftarferlinu. Þessar breytingar krefjast aðgerðir notanda eftir uppfærslu. Það er mikilvægt að þú lesir og skiljir eftirfarandi breytingar, jafnvel þótt þú hafir ekki enn notað Eignir.

- Leiðin sem afskriftarferlið ákvarðar skýrslugjaldmiðilsupphæðina hefur breyst. Eftirfarandi atburðarás ber saman hvernig afskriftir hafa áður ákvarðað skýrslugjaldmiðilsupphæð og hvernig það ákvarðar skýrslugjaldmiðilsupphæð núna.



    **Afskriftir atburðarás**

    Eign er keypt og bókuð með eftirfarandi upphæðum. Athugaðu að skýrslugjaldmiðilsupphæðin er settur í fjárhag en það er ekki geymt í töflum undirbókar Eignar.

    | Færslugerð | Færsluupphæð | Gengi | Upphæð bókhaldsgjaldmiðils | Gengi | Skýrslugjaldmiðilsupphæð |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Kaup      | 1.000.000 DKK      | 2,0           | 500.000 USD                | 2,5           | 200.000 EUR               |

    **Fyrri afskriftir fyrir skýrslugjaldmiðilinn**

    Í lok árs er afskriftartillaga keyrð og reiknar út eftirfarandi upphæðir.

    | Færslugerð | Færsluupphæð | Gengi | Upphæð bókhaldsgjaldmiðils | Gengi | Skýrslugjaldmiðilsupphæð |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Afskrift     | 50.000 USD         | 1.0           | 50.000 USD                 | 2,6           | 19.230,77 EUR             |

    Þegar afskriftartillaga eru keyrðar reiknar það bókhaldsgjaldmiðilsupphæð með því að nota afskriftaraðferðina. Það þýðir síðan upphæðina í skýrslugjaldmiðilinn með því að nota núverandi gengi á milli USD og EUR. Þessi þýðing veldur vandamálum vegna þess að eignin er ekki hægt að fullu afskrifuð í skýrslugjaldmiðlinum þegar stundargengi er notað.

    **Nýjar afskriftir fyrir skýrslugjaldmiðilinn**

    Afskriftarferlinu hafa verið breytt þannig að skýrslugjaldmiðilsupphæðin er einnig reiknuð með því að nota afskriftaraðferðina. Hér eru niðurstöðurnar þegar afskriftir eru keyrðar á eigninni.

    | Færslugerð | Færsluupphæð | Gengi | Upphæð bókhaldsgjaldmiðils | Gengi                                                       | Skýrslugjaldmiðilsupphæð |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Afskrift     | 50.000 USD         | 1.0           | 50.000 USD                 | 2,5<blockquote>[!NOTE] Þótt þessi gengi sé sýndur er það ekki notað til að þýða í skýrslugjaldmiðilinn.</blockquote> | 20.000 EUR                |

    Þegar afskriftartillaga eru keyrðar reiknar það bæði bókhaldsgjaldmiðilsupphæð og skýrslugjaldmiðilsupphæð með því að nota afskriftaraðferðina. Upphæðirnar eru síðan notaðar í bókhaldsfærslu í fjárhagnum. Engar þýðingar eru gerðar til að ákvarða skýrslugjaldmiðilsupphæðina.

- **Uppfærsluatriði:** Vegna þess að eignabókafærslur höfðu ekki áður fylgst með skýrslugjaldmiðlinum hefur leiðsagnarforriti verið bætt við þannig að þú getir bætt skýrslugjaldmiðilsupphæðum við eignabókafærslur. Þetta leiðsagnarforrit bókar **ekki** aftur í fjárhag. Vegna þess hvernig afskriftartillaga reiknar skýrslugjaldmiðilsupphæð hefur breyst, **verður** leiðsagnarforritið að keyra og lokið fyrir hvert fyrirtæki áður en fyrirtæki getur slegið inn hverja afskriftarfærslu.

    - Til að hefja leiðsagnarforritið, veldu **Eignir** \> **Setja upp** \> **Bæta skýrslugjaldmiðilsupphæðum við eignabækur** .
    - Leiðsagnarforritið sýnir færslur fyrir alla eignarbækur í núverandi fyrirtæki sem hefur skýrslugjaldmiðilsupphæð 0 (núll). Aðeins færslur sem voru bókaðar fyrir uppfærslu eru innifalin.
    - Leiðsagnarforritið tekur **ekki** skýrslugjaldmiðilsupphæðirnar úr fjárhag. Eins og lýst er í fyrri atburðarás voru skýrslugjaldmiðilsupphæðir sem upphaflega voru settar í fjárhag ranglega notaðir á stundargengi. Þessar fjárhæðir ættu ekki að koma fram í undirbók eigna, vegna þess að næsti afskriftarútreikningur mun nota rangar upphæðir. Í staðinn finnur leiðsagnarforritið gengið á fyrsta kaupverði. Það notar þá gengið til að mæla með skýrslugjaldmiðilsupphæðinni sem ætti að vera settur í undirbókina. Til dæmis, hér er það sem leiðsagnarforritið gæti sýnt fyrir fyrri atburðarás.

        | Eign | Bóka      | Færslugerð | Færsludagsetning | Gjaldmiðill | Upphæð í færslugjaldmiðli | Upphæð  | Gengi | Skýrslugjaldmiðilsupphæð |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Kaup      | 6/3/2016         | DKK      | 1.000.000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Afskrift     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Afskrift     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Afskrift     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - Margir viðskiptavinir röktu færsluupplýsingum sína í vinnubókum. Þessar upplýsingar innihalda gengi og upphæðir. Ef þú hefur þessar gögn í vinnubók getur þú búið til sérsniðin gengisgerð og uppfært það með gengi frá vinnubókinni. Þessi gengisgerð verður síðan notuð til að slá inn sjálfgefið gengi á kaupdegi og reikna út skýrslugjaldmiðilsupphæð. Ef gengisgerð er ekki valin, notar leiðsagnarforritið gengið sem var skilgreindur í fjárhag.
    - Hægt er að breyta gengi og skýrslugjaldmiðilsupphæðum. Ef gengi er breytt er skýrslugjaldmiðilsupphæð endurreiknuð með því að nota nýtt gengi.
    - Ef þú velur **Hætta við** í leiðsagnarforritinu eru eignabókarfærslur og allar breytingar á genginu eða skýrslugjaldmiðilsupphæðum vistuð þangað til næst þegar þú ræsir leiðsagnarforritið. Hins vegar eru skýrslugjaldmiðilsupphæðir ekki uppfærðar á eignabókarfærslum. Þessi uppfærsla verður aðeins þegar þú velur **Ljúka** í leiðsagnarforritinu. Þú getur keyrt leiðsagnarforritið oft. Þess vegna getur þú lagað allar rangar skýrslugjaldmiðilsupphæðir ef þú gerir mistök.
    - Þegar skýrslugjaldmiðilsupphæðirnar eru fullkomlega uppfærðar í undirbókinni **þarftu** að setja **Hefurðu uppfært allar upphæðir í skýrslugjaldmiðli í eignabókafærslunum?** valkostur til **Já** og þá velja **Ljúka**. Ekki er hægt að ljúka útreikningi á afskriftum fyrr en þú stillir **Hefurðu uppfært allar upphæðir í skýrslugjaldmiðli í eignabókafærslunum?** valkostur til **Já** . Eftir að þessi valkostur er stilltur á **Já**, er leiðsagnarforritið ekki lengur í boði.
    - Eftir að eignarfærslur í undirbók eru uppfærðar með skýrslugjaldmiðilsupphæðum stemma þessar upphæðir ekki við upphæðirnar sem upphaflega voru settar í fjárhaginn. Hins vegar er hægt að nota leiðréttingarbók skýrslugjaldmiðilsins til að uppfæra afskriftarstöður fjárhagslykla í fjárhagnum þannig að þau samsvari upphæðin sem upphaflega var bókuð.
    - Nýtt **Skýrslugjaldmiðilsupphæðir eignafærslu** eining sem hefur verið bætt í **Gagnastjórnun** vinnusvæði gerir þér kleift að flytja gögnin úr leiðsagnarforritinu. Þú getur síðan notað gögnin til að ákvarða stöðu eignarundirbókarinnar fyrir afskriftarfærslurnar. Þá er hægt að nota þessa stöðu til að ákvarða leiðréttingu skýrslugjaldmiðilsupphæðar í fjárhagnum.

- **Uppfærsluatriði:** Nýjum uppfærslureitum hafa verið bætt við eignir og notuð í útreikning afskrifta. Þú gætir þurft að uppfæra þessi reiti fyrir næsta útreikning afskrifta.

    - Í eignabókinni (**Eignir** \> **Bækur**) hefur **Almennt** flýtiflipinn nýtt **Kaupverð í skýrslugjaldmiðli** reitinn.
    - Í eignabókinni (**Eignir** \> **Bækur**) hefur **Afskriftir** flýtiflipinn nýtt **Áætlað ruslvirði í skýrslugjaldmiðli** reitinn.
    - Í færibreytum eigna (**Eignir** \> **Setja upp** \> **Færibreytur eigna**), **Almennt** flýtiflipinn nýtt **Áætlað rýrnunarvirði í skýrslugjaldmiðli** reitinn.
    - Á bækur (**Eignir** \> **Setja upp** \> **Bækur**), **Almennt** flýtiflipinn hefur tvo nýja reiti: **Slétta afskriftir í skýrslugjaldmiðli** og **Bókað nettóvirði skal vera í skýrslugjaldmiðli**.

- Vegna þess að afskriftartillagan nú reikna út upphæðir bæði í bókhaldsgjaldmiðlinum og í skýrslugjaldmiðlinum hefur færslubók eigna verið uppfærð þannig að hún birti afskriftaupphæðir í skýrslugjaldmiðli. Við afskriftarfærslur er færslugjaldmiðillinn alltaf bókhaldsgjaldmiðillinn. Þess vegna munu þessi upphæðir birtast áfram í **Úttektar** og **Inneignar** dálkunum. Tvær nýir dálkar, **Úttekt í skýrslugjaldmiðli** og **Inneign í skýrslugjaldmiðli**, hefur verið bætt við hnitanetið.

    - Nýju reitin eru aðeins tiltæk þegar færslugerðin er ein af fjórum afskriftartegundum: **Afskrift**, **Leiðrétting afskrifta**, **Óreglulegar afskriftir**, eða **Sérstök heimild til afskriftar**.
    - Ef færslugerð afskriftar er færð í færslubók eigna verða skýrslugjaldmiðilsupphæðir birtar í nýju dálkunum. Þessar fjárhæðir má breyta.
    - Ef bókhaldsgjaldmiðill og skýrslugjaldmiðill í fjárhag eru þau sömu, verður fjárhæðirnar haldið í samstillingu. Ef þú breytir **Inneignar** upphæðinni verður **Inneign í skýrslugjaldmiðli** upphæð sjálfkrafa breytt þannig að það samsvari því.
    - Ef einhver önnur færslugerð er slegin inn í færslubók eigna er **Úttekt í skýrslugjaldmiðli** og **Inneign í skýrslugjaldmiðli** upphæð aldrei sýnd, hvorki fyrir eða eftir bókun. Upphæðir bókhaldsgjaldmiðils og skýrslugjaldmiðils eru enn í boði á fylgiskjali sem sendir til fjárhags.
    
### <a name="consolidations"></a>Samstæður
    
Virkni sem kynnt var í Dynamics 365 Finance útgáfu 10.0.5 (október 2019) gerir kleift að virkja með eiginleikastjórnun fyrir aukinn sveigjanleika fyrir samstæðu og tvöfaldan gjaldmiðil. Til að virkja þessa virkni ferðu í vinnusvæðið **Stjórnun eiginleika** og veldu **Virkja virkni tvöfalds gjaldeyris í samstæðu fjárhags**.

Í samstæðu fjárhags hefur nýjum valkosti verið bætt við til að sameina annaðhvort bókhalds- eða skýrslugjaldeyrisupphæðir úr upprunafyrirtækjunum. Ef bókhalds- eða skýrslugjaldmiðillinn er sá sami og bókhalds- eða skýrslugjaldmiðillinn í samstæðufyrirtækinu verða upphæðirnar afritaðar beint frekar en þýddar.

-  Þú getur nú valið hvort nota á bókhaldsgjaldmiðilinn eða skýrslugjaldmiðilinn frá upprunafyrirtækinu sem viðskiptamynt í samstæðufyrirtækinu.

- Upphæðir bókhalds- eða skýrslugjaldmiðils úr upprunafyrirtækinu verður afritaður beint í upphæðir bókhalds- eða skýrslugjaldmiðils í samstæðufyrirtækinu, ef annar hvor gjaldmiðillinn er sá sami. Fjárhæðir í bókhalds- og skýrslugjaldmiðlum í samstæðufyrirtækinu eru reiknaðar út með gengi ef hvorugur gjaldmiðillinn er sá sami.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]