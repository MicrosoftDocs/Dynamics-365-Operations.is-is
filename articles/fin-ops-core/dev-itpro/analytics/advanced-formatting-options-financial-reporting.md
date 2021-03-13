---
title: Ítarlegir sniðsvalkostir í fjárhagsskýrslugerð
description: Þetta efnisatriði lýsir ítarlegum sniðsaðgerðum, þ.m.t. síum, takmörkunum, línum sem ekki eru prentaðar og skilyrtar setningar í útreikningum.
author: panolte
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f0417ac1007fc94431aeb11d2464ee699e3f3441
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093163"
---
# <a name="advanced-formatting-options-in-financial-reporting"></a>Ítarlegir sniðsvalkostir í fjárhagsskýrslugerð

[!include [banner](../includes/banner.md)]

Þegar skýrsla er stofnuð í fjárhagsskýrslu, eru tiætækar aukalegar aðgerðir fyrir snið, þar með talið síur fyrir víddir, takmarkanir fyrir dálka og eining skipurits, línur sem ekki á að prenta og IF/THEN/ELSE-yrðingar í útreikningum.

Eftirfarandi tafla útskýrir aðgerðir fyrir ítarleg snið sem eru tiltækar við skýrsluhönnun.

| Aðgerð                   | Lýsing |
|----------------------------|-------------|
| Víddarsía           | Hægt er að nota víddir í línuskilgreiningunni og dálkskilgreiningunni til að fá aðgang að tilgreindum gagnasamstæðum. Margar skýrslur nota aðeins meginhluta í línusniði. Hins vegar hægt að breyta línum þannig að þær hafi víddargildi. Afmörkun vídda er notuð í dálkskilgreiningunni til að fá aðgang að tilgreindum gagnasamstæðum. |
| Takmörkun einingar skipurits | Hægt er að setja upp skýrsluröð þannig að hún sýni einungis upplýsingar sem er tengdar ákveðinni einingu skipurits. |
| Línur sem ekki eru til prentunar (NP)     | Línur sem ekki eru til prentunar geta verið gagnlegar í mörgum skýrslum. Ef nota þarf nokkra útreikninga til að fá út gildi er hægt að fela þessa útreikninga á prentuðu skýrslunni. Línur sem ekki eru til prentunar eru einnig ganglegar við hönnun úrræðaleitarskýrslna og fyrir ítarlega staðsetningu hólfa. |
| Dálktakmörkun         | Dálktakmörkun í línuskilgreiningu er gagnleg til að fela gildi sem hafa aðeins þýðingu fyrir sumar línur í skýrslunni. Þegar hlutfallsútreikningar eru gerðir fyrir línu kemur þessi dálktakmörkun í veg fyrir að samtöludálkar eða aðrir dálkar verði prentaðir ef þær tölur eiga ekki við. |
| Dálkaskil               | Þú getur bætt dálkaskilum í línuskilgreiningu að sýna skýrsluupplýsingar hlið við hlið. Hægt er að bæta mörgum dálkaskilum í eina línuskilgreiningu og dálkfyrirsagnir eru endurteknar efst í hverjum dálki eftir dálkaskil. Athugasemdir fyrir skýrslu eru sýndar á milli dálkaskila. |
| IF/THEN/ELSE-yrðing     | Hægt er að breyta útreikningum í línuskilgreiningu eða skilgreiningu dálks. |
| Notaðu einfaldar gæsalappir („“) og og-merkið (&) fyrir víddargildi | Þú getur notað víddargildi, þ.m.t. og-merkið fyrir skýrsluhönnun. |

## <a name="advanced-cell-placement"></a>Ítarleg staðsetning hólfa

Ítarleg staðsetning hólfa, eða *þannig*, felur í sér staðsetningu á tilgreindum gildum í tilgreindum reitum. Til dæmis er þvingum oft notuð til að flytja rétta stöðu í sjóðstreymisyfirlit. Hægt er að nota þvingun í eftirfarandi tilgangi:

- Flytja gildi úr Microsoft Excel inn í tiltekna reiti.
- Harðkóða tilgreind gildi inn í skýrslu.
- Breyta táknum með því að afrita gildi úr fyrra hólfi og margfalda með -1.

> [!NOTE]
> Í mörgum tilvikum þarf að skilgreina skýrsluskilgreiningu þannig að útreikningar eru framkvæmdir fyrir línuútreikninga. Fylgið eftirfarandi skrefum til að ljúka þessum skilgreiningum.
>
> 1. Opnið skýrsluskilgreiningu í Skýrsluhönnun.
> 2. Á flipanum **Stillingar** undir **Útreikningsforgangur**, velurðu **Framkvæma dálkaútreikning fyrsta og síðan línuna**.

## <a name="designing-the-report"></a>Hönnun skýrslunnar

Við hönnun skýrslu skal fyrst stofna allar ítarupplýsingalínur til að tryggja að gildin séu tekin inn í þeirri röð sem vænta má . Svo skal bæta við **NP** (engin prentun) sniðhnekkingu til að fela ítarupplýsingarnar sem innihalda lokagildin.

> [!IMPORTANT]
> Þegar sniðkóðinn **CAL** er notaður í línuskilgreiningu er ekki hægt að kafa niður í ítarupplýsingar um færslu.

Fyrir þvingun nota formúlur eftirfarandi snið: &lt;viðtökudálkur&gt;=&lt;upprunadálkur&gt;.&lt;línukóði&gt; Aðskilja allar viðbótarstaðsetningar eftir línu með kommu og bili. Hér er dæmi: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Dæmi um ítarlega sniðsvalkosti

Eftirfarandi dæmi sýna hvernig á að sníða línuskilgreiningu og skilgreiningu dálks til að þvinga fram grunnskýrslu um sjóðstreymi (dæmi 1) og tölfræðiskýrslu (dæmi 2).

### <a name="example-1-basic-forcing"></a>Dæmi 1: Grunnþvingun

Eftirfarandi tafla sýnir dæmi um línuskilgreiningu sem notar grunnþvingun.

| Línukóði |           lýsing            | Sniðkóði | Tengdar formúlur/línur/einingar |        Línubreyting        | Tengill í fjárhagsvíddir |
|----------|----------------------------------|-------------|-----------------------------|----------------------------|------------------------------|
| 100      | Lausafé við upphaf tímabils (NP) |             |                             | Breyting á reikningi = \[/BB\] | +Segment2 = \[1100\]         |
| 130      | Reiðufé í upphafi tímabils      | CAL         | C=C.100,F=D.100             |                            |                              |
| 160      |                                  |             |                             |                            |                              |
| 190      |                                  |             |                             |                            |                              |

> [!NOTE]
> Tómir dálkar voru fjarlægðir úr fyrri töflu til kynningar: Hnekking sniðs, Venjuleg staða, Prentstýringar, Takmarkanir dálka dálkar eru ekki sýndir.

Eftirfarandi tafla sýnir dæmi um línuskilgreiningu sem notar grunnþvingun í línunni.

|           Snið             | A   | V    | K        | D      | E      | F    |
|------------------------------|-----|------|----------|--------|--------|------|
| Haus 1                     |     |      |          |        |        |      |
| Fyrirsögn 2                     | A   | V    | K        | D      | E      | F    |
| Fyrirsögn 3                     |     |      |          |        |        |      |
| Dálkgerð                  | ROW | DESC | FD       | FD     | FD     | CALC |
| Bókarkóði/Eigindaflokkur |     |      | ACTUAL   | ACTUAL | ACTUAL |      |
| Fjárhagsár                  |     |      | BASE     | BASE   | BASE   |      |
| Tímabil                       |     |      | BASE     | BASE   | BASE   |      |
| Tímabil sem er tekið með              |     |      | PERIODIC | YTD/BB | YTD    |      |
| Formúla                      |     |      |          |        |        | E-D  |
| Dálkbreidd                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Dæmi 2: Tölfræðiskýrslur

Eftirfarandi tafla sýnir dæmi um línuskilgreiningu sem notar þvingun fyrir tölfræðiskýrslu.

| Línukóði | Lýsing               | Sniðkóði | Tengdar formúlur/línur/einingar     | Hnekkja sniði      | Eðlileg staða | Tengill í fjárhagsvíddir               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|--------------------------------------------|
| 50       | Tölfræðilegar upplýsingar   | REM         |                                 |                      |                |                                            |
| 100      | Starfsmannafjöldi - US            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 115      | Starfsmannafjöldi - Alþjóðlegt | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 130      |                           |             |                                 |                      |                |                                            |
| 190      | Bandarísk sala                  |             |                                 |                      | K              | +Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Alþjóðleg sala       |             |                                 |                      | K              | +Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |                                            |
| 280      |                           |             |                                 |                      |                |                                            |
| 310      | Bandarísk sala                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |                                            |
| 340      | Alþjóðleg sala       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |                                            |

> [!NOTE]
> Tómir dálkar voru fjarlægðir úr fyrri töflu til kynningar: Prentstýringar, Takmarkanir dálka og Línubreyting dálkar eru ekki sýndir.

Eftirfarandi tafla sýnir dæmi um dálkskilgreiningu sem notar þvingun fyrir tölfræðiskýrslu.

|    Snið                    | A   | V    | K      | D            | E     | F            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Haus 1                     | A   | V    | K      | D            | E     | F            |
| Fyrirsögn 2                     | -   | -    | ÁÁ    | Árleg sala | Starfsmaður | $ eftir einstaklingum |
| Fyrirsögn 3                     |     |      |        |              |       |              |
| Gerð dálks                  | ROW | DESC | FD     | CALC         | CALC  | CALC         |
| Bókarkóði/Eigindaflokkur |     |      | ACTUAL |              |       |              |
| Fjárhagsár                  |     |      | BASE   |              |       |              |
| Tímabil                       |     |      | BASE   |              |       |              |
| Tímabil sem er tekið með              |     |      | YTD    |              |       |              |
| Formúla                      |     |      |        |              |       | E-D          |
| Dálkbreidd                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Takmarka línu við tiltekna einingu skipurits.

Þegar skýrslulína takmarkast við ákveðna einingu skipurits, sýnir sú lína tengd gögn aðeins fyrir nefnda einingu skipurits og hunsar gögn fyrir aðrar einingar skipurits í skipuritinu. Til dæmis er hægt að stofna línu sem veitir upplýsingar um heildarkostnað við rekstur tiltekinnar deildar. Skýrslan gæti innihaldið tvítekin gögn ef skýrslan inniheldur bæði skipurit og línuskilgreiningu sem hefur fleiri en einungis meginreikning. Til dæmis ef notandi er með skipurit sem tilgreinir allar sex deildirnar innan fyrirtækis og er einnig með línuskilgreiningu sem tilgreinir tiltekna samsetningu reiknings og deildar í línunni. Þegar skýrslan er mynduð er hin tiltekna samsetning reiknings og deildar prentuð á öll þrep skipuritsins, jafnvel þótt sú deild samsvari ekki því sem er í skipuritinu. Þetta gerist vegna þess að línan hnekkir því sem yfirleitt er afmarkað út með skýrsluskilgreiningunni. Ein leið til að forðast tvítekningu gagna er að takmarka línu við tilgreinda einingu skipurits.

> [!NOTE]
> Ef lína inniheldur víddir, og þú takmarkar þá línu við undireiningu skipurits, er línuupphæðin höfð með í þeirri undireiningu og yfireiningum hennar en enging tvítekning á sér stað.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Takmörkun línu við einingu skipurits

1. Smellt er á **Línuskilgreiningar** í Skýrsluhönnun og línuskilgreining sem á að breyta því næst valin.
2. Þá er tvísmellt á viðeigandi hólf fyrir **Tengdar formúlur/línur/einingar**.
3. Í svarglugganum **Einingaval skipurits** í reitnum **Skipurit** skal velja tréð sem hefur verið úthlutað í skilgreiningu skýrslunnar.
4. Eining skipurits er valin og síðan er smellt á **Í lagi**. Takmörkunin er birt í hólfi línuskilgreiningar.
5. Tvísmella skal á hólfið í dálkinum **Tengill á fjárhagsvíddir** í takmörkuðu línunni og því næst færa inn tengil á fjárhagsgagnakerfið.

## <a name="selecting-print-control-in-a-row-definition"></a>Velja prentstjórnun í línuskilgreiningu

Hægt er að tilgreina kóða stillingar fyrir prentun fyrir hvern dálk með því að nota hólfið **Prentstýringar**.

### <a name="add-print-control-codes-to-a-report-row"></a>Kóða stillingar fyrir prentun bætt við skýrslulínu

1. Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.
2. Tvísmellið á hólfið **Stilling fyrir prentun**.
3. Í svarglugganum **Prentstýringar** skal velja kóða stillinga fyrir prentun eða styðja á og halda niðri Ctrl-lykli til að velja marga kóða. Einnig er hægt að færa kóða stillinga fyrir prentun beint inn í hólfið **Prentstýringar**. Aðskiljið marga kóða stillinga fyrir prentun með kommum.
4. Veljið hvers kyns skilyrta prentvalkosti.
5. Smelltu á **Í lagi**.

### <a name="regular-print-control-codes"></a>Kóðar fyrir venjulega stillingu fyrir prentun

Eftirfarandi tafla lýsir venjulegum kóðum stillinga fyrir prentun fyrir línuskilgreiningu.

| Kóði fyrir stillingu prentunar | Túlkun kóða stillinga fyrir prentun         | Lýsing |
|--------------------|--------------------------------------------------|-------------|
| NP                 | Lína sem ekki er til prentunar                                 | Koma í veg fyrir upphæðir í línunni séu prentaðar í skýrslunni og útiloka upphæðir frá útreikningi. Til að taka dálk sem ekki er til prentunar með í útreikningi er vísað beint til dálksins í útreikningsformúlunni. Til dæmis er lína 240 sem ekki er til prentunar innifalin í eftirfarandi útreikningi: **230+240+250**. Hins vegar er lína 240, sem ekki er ætluð til prentunar, ekki tekin með í eftirfarandi útreikningi: **230:250**. |
| CS                 | Gjaldmiðilstákn; nota gjaldmiðilssnið í þessari línu | Hafa gjaldmiðilstáknið með í öllum upphæðum sem ekki eru prósenta. Prósentugildi fá aldrei gjaldmiðilstákn. |
| XD                 | Lína falin í upplýsingaskýrslu reiknings            | Fela birta lykla í upplýsingaskýrslum um lykla og skýrslum um færsluupplýsingar. Þessar prentstýringar eru gagnlegar þegar lína inniheldur marga reikninga sem ekki á að birta í upplýsingaskýrslu um reikning eða skýrslu um færsluupplýsingar. |
| X0                 | Lína falin ef hún inniheldur bara núll                        | Útiloka línu frá skýrslunni ef öll hólf í þeirri línu eru annaðhvort tóm eða innihalda núll. Þessi prentstýring hefur einungis merkingu þegar valkosturinn um að fela núllstöðu er ekki valinn í skýrsluskilgreiningunni. |
| B0                 | Núlldálkar hafðir auðir                         | Skilja dálka eftir auða í línu sem inniheldur núllupphæðir. |
| XR                 | Samantekt falin                                  | Felur samantekt. Ef notað er skipurit í skýrslunni eru upphæðirnar í þessari línu ekki teknar saman í yfirhnútum sem á eftir koma. |
| SR                 | Sléttun falin                                | Koma í veg fyrir að upphæðir í þessari línu séu sléttaðar. |
| XT                 | Lína falin í skýrslu um færsluupplýsingar        | Fela færslur í skýrslum um færsluupplýsingar. Þessar prentstýringar eru gagnlegar þegar lína inniheldur marga reikninga sem ekki á að birta í skýrslu um færsluupplýsingar. |

### <a name="conditional-print-control-codes"></a>Kóðar fyrir skilyrtar stillingar fyrir prentun

Eftirfarandi tafla lýsir kóðum fyrir skilyrtar stillingar fyrir prentun fyrir línuskilgreiningu.

| Kóði fyrir stillingu prentunar | Lýsing                                  |
|--------------------|----------------------------------------------|
| (ekkert)             | Hreinsar skilyrta prentvalið.       |
| DR                 | Prenta eingöngu debetstöður fyrir þessa línu.  |
| CR                 | Prenta eingöngu kreditstöður fyrir þessa línu. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Dálktakmörkunarhólf í línuskilgreiningu

Hólfið **Dálktakmörkun** í línuskilgreiningu hefur margvíslegan tilgang. Tegund línu segir til um hvort hægt er að nota hólfið **Dálktakmörkun** til að tilgreina eina af eftirfarandi aðgerðum:

- Hólfið getur takmarkað prentun línuupphæða í tiltekinn dálk. Þessi aðgerð er gagnleg stofnun efnahagsreiknings á töflusniði.
- Hólfið getur tilgreint upphæðadálkinn sem á að raða.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Útreikningsformúla notuð í línuskilgreiningu

Reikniformúla í línuskilgreiningu getur innihaldið reiknimerkin **+**, **-**, **\**_, og _*/** og einnig **IF/THEN/ELSE**-yrðingar. Þar að auki getur útreikningur varðað einstök hólf og raunupphæðir (rauntölur sem hafðar eru í formúlunni). Hver formúla getur innihaldið allt að 1.024 stafi. Ekki er hægt að beita útreikningum á línur sem innihalda hólf af tegundinni **Tengill í fjárhagsvíddir** (FD). Hins vegar er hægt að taka með útreikninga á samfelldar línur, fela prentun þessara lína og finna síðan samtölu þessara útreikningslína.

### <a name="operators-in-a-calculation-formula"></a>Virkjar í reikniformúlu

Reikniformúla notar flóknari virkja en formúla fyrir línusamtölu. Hins vegar hægt að nota reiknimerkin **\**_ og _*/** ásamt frekari reiknimerkjum til að margfalda (\*) og deila (/) upphæðum. Til að nota svið eða samtölu í reikniformúlu verður að nota á-merkið (@) framan við alla línukóða, nema verið sé að nota dálk í línuskilgreiningunni. Ef til dæmis á að bæta upphæðinni í röð 100 við upphæðina í röð 330 er hægt að nota formúlu fyrir línusamtölu **100+330**, eða reikniformúluna **@100+@330**.

> [!NOTE]
> Nota verður á-merkið (@) á undan hverjum línukóða sem notaður er í reikniformúlu. Annars er talan lesin sem raunupphæð. Til dæmis bætir reikniformúlan **@100+330** 330 USD við upphæðina í línu 100. Þegar vísað er til dálks í reikniformúlu er ekki þörf fyrir á-merkið (@).

### <a name="create-a-calculation-formula"></a>Reikniformúla stofnuð

1. Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.
2. Tvísmellið á hólfið **Sniðkóði** og veljið síðan **CAL**.
3. Í hólfinu **Tengdar formúlur/línur/einingar** er slegin inn reikniformúla.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Dæmi um útreikningsformúlu fyrir tilteknar línur

Í þessu dæmi merkir reikniformúlan **@100+@330** að upphæðin í línu 100 er bætt við línu 330. Formúlan fyrir línusamtölu **340+370** bætir upphæðinni í línu 340 við upphæðina í línu 370, sem inniheldur upphæðina úr reikniformúlunni. (Línupphæðin í línu 370 er upphæðin úr reikniformúlunni.)

| Línukóði | Lýsing                 | Sniðkóði | Tengdar formúlur/línur/eining | Stilling fyrir prentun | Línubreyting | Tengill í fjárhagsvíddir |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Reiðufé í upphafi tímabils |             |                            | NP            | BB           | +Reikningur=\[1100:1110\]       |
| 370      | Reiðufé í upphafi árs   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Reiðufé í upphafi tímabils | TOT         | 340+370                    |               |              |                              |

Þegar línu í línuskilgreiningu er með sniðkóðann **CAL**, og notandi færir inn reikniformúlu í hólfið **Tengdar formúlur/línur/einingar** verður einnig að færa inn staf tengda dálksins og línunnar í skýrslunni. Til dæmis færirðu inn **A.120** til að tákna dálk A, línu 120. Einnig er hægt að nota á-merkið (@) til að tilgreina allra dálka. Til dæmis færirðu inn **@120** til að tákna alla dálka í línu 120. Allar reikniformúlur sem eru ekki með dálkstaf eða @-tákn teljast vera tölustafur.

> [!NOTE]
> Ef línukóðamerki er notað til að vísa í línu verður að nota punkt (.) sem skiltákn milli dálkstafs og merkis (t.d. **A.GROSS\_MARGIN/A.SALES**). Ef nota á-merki (@) er skiltákn óþarfi (t.d. **\@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Dæmi um útreikningsformúlu fyrir tiltekinn dálk

Í þessu dæmi merkir reikniformúlan **E=C.340** að útreikningurinn í hólfinu í dálki C, línu 340, nái aðeins til dálks E.

> [!NOTE]
> Þegar vísað er til dálks í reikniformúlu er ekki þörf fyrir á-merkið (@).

| Línukóði | Lýsing                 | Sniðkóði | Tengdar formúlur/línur/eining | Stilling fyrir prentun | Línubreyting | Tengill í fjárhagsvíddir |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Reiðufé í upphafi tímabils |             |                            | NP            | BB           | +Reikningur=\[1100:1110\]       |
| 370      | Reiðufé í upphafi árs   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Reiðufé í upphafi tímabils | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Breyta númeri í völdum dálkum

Þegar verið er að breyta tölu eða útreikningi í einum dálk í tiltekinni línu en ekki á að hafa áhrif á aðra dálka í skýrslunni er hægt að tilgreina **CAL** (útreikning) í dálknum **Sniðkóða** í línuskilgreiningunni.

- Ef framkvæma á útreikning á öllum skýrsludálkum (**FD**) skal ekki færa inn dálkúthlutun.
- Til að takmarka formúlu við tiltekna dálka skal færa inn dálkstafinn ásamt samasemmerki (**=**) og síðan formúluna.
- Hægt er að tilgreina marga dálka. Þegar notað er á-merki (@) með tiltekinni staðsetningu í dálki tengist á-merkið @ línunni.
- Hægt er að færa inn margar dálkformúlur í einni línu. Aðskiljið formúlur með kommum.

### <a name="calculation-examples"></a>Dæmi um útreikning

| Útreikningur            | Aðgerð sem er stofnuð                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Fyrir hvern dálk er gildi í línu 130 margfaldað með 0.75. Síðan eru niðurstöðurnar settar í núgildandi línu í hverjum dálki. |
| B=@130\*.75            | Sami útreikningur er einungis gerður á dálki B.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF/THEN/ELSE-yrðingar í línuskilgreiningu

Hægt er að bæta **IF/THEN/ELSE**-yrðingum við alla gilda útreikninga og nota þær með sniðinu **CAL**. Færa skal inn **IF/THEN/ELSE**-reikniformúlur í hólfið í dálkinum **Tengdar formúlur/línur/einingar**. **IF/THEN/ELSE**-reikniformúlur nota eftirfarandi snið: IF &lt;sönn/ósönn yrðing&gt; THEN &lt;formúla&gt; ELSE &lt;formúla&gt; **ELSE &lt;formúlu&gt;**-hluti yrðingarinnar er valfrjáls.

#### <a name="if-statements"></a>IF-yrðingar

Yrðingin sem kemur á eftir **IF**-yrðingunni getur verið hvaða yrðing sem er sem hægt er að meta sem sanna eða ósanna. Uppgjörið sem fylgir **IF**-yrðingunni gæti falið í sér einfalt mat eða verið flókin yrðing sem innihéldi margar segðir. Hér eru nokkur dæmi:

- **IF A.200&gt;0** (Einfalt mat)
- **IF A.200&gt;0 OG A.200&lt;10.000** (flókin yrðing)
- **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (flókin yrðing sem inniheldur margar segðir)

Hugtakið **Tímabil** í **IF**-yrðingu stendur fyrir fjölda tímabila fyrir skýrsluna. Þetta hugtak er oft notað við útreikninga á meðaltali það sem af er ári. Til dæmis, þegar skýrsla er keyrð fyrir tímabilið 7 YTD þýðir yrðingin **B.150/Tímabil** að gildið í línu 150 í dálki B er deilt með 7.

#### <a name="then-and-else-formulas"></a>THEN- og ELSE-formúlur

**THEN** og **ELSE**-formúlur geta verið hvaða gildir útreikningar sem er, allt frá afar einföldum úthlutuðum sjálfgildum yfir í flóknar formúlur. Til dæmis þýðir yrðingin **IF A.200&gt;0 THEN A=B.200** að „ef gildið í hólfinu í dálki A í línu 200 er hærra en núll skal setja gildið úr hólfinu í dálki B í línu 200 inn í hólfið í dálki A í þessarar línu.“ **IF/THEN**-yrðingin hér að ofan setur gildi í einn dálka þessarar línu. Hins vegar er einnig hægt að nota @-táknið í annaðhvort TRUE/FALSE-mati eða í formúlunni til að tákna alla dálka. Hér eru önnur dæmi sem er lýst er í eftirfarandi hlutum:

- **EF A.200 &gt;0 ÞÁ B.200**: Þegar gildið í reitnum A.200 er jákvætt er gildið í reitnum B.200 sett í alla dálka á gildandi línu.
- **IF A.200 &gt;0 THEN @200**: Ef gildið í reitnum A.200 er jákvætt er gildið í reitnum B.200 sett í alla dálka á gildandi línu.
- **IF @200 &gt;0 THEN @200**: Ef gildið í reitnum A.200 er jákvætt er gildið í reitnum B.200 sett í alla dálka á gildandi línu.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Útreikningur takmarkaður við einingu skipurits í línuskilgreiningu

Ef takmarka á útreikning við staka einingu í skipuriti svo að upphæðin sem út kemur sé ekki færð upp á einingu á hærra stigi er hægt að nota kóðann **\@Unit** í hólfinu **Tengdar formúlur/línur/einingar** í línuskilgreiningunni. Í **\@Unit** kóði hefur verið skráður í dálkur B skýrslugerð trés **Einingarnafn**. Þegar kóðinn **\@Unit** er notaður eru gildin ekki færð upp en útreikningurinn er metinn á hverju stigi skipuritsins.

> [!NOTE]
> Ef nota á þessa aðgerð verður skipuritið að vera tengt línuskilgreiningunni.

Útreikningslínan getur vísað til útreikningslínu eða fjárhagsgagnalínu. Útreikningurinn er skráður í hólfið **Tengdar formúlur/línur/einingar** í línuskilgreiningunni ásamt takmörkunum fjárhagsgagnagerða. Útreikningurinn verður að nota skilyrtan útreikning sem hefst á **IF @Unit**. Hér er dæmi: EF @Unit(SALES) SÍÐAN @100 ELSE 0 Þessi útreikningur felur í sér upphæðina úr línu 100 í hverjum dálki í skýrslunni, en eingöngu fyrir SALES-einingar. Ef margar einingar heita SALES birtist upphæðin í hverri þessara eininga. Auk þess gæti lína 100 verið fjárhagsgagnalína og skilgreind sem ekki til prentunar. Í þessu tilfelli er komið í veg fyrir að upphæðin birtist í öllum einingum í trénu. Einnig er hægt að takmarka upphæðina við stakan dálk í skýrslunni með því að nota dálkatakmarkanir, eins og dálk H, til að prenta gildið eingöngu í þessum dálk skýrslunnar. Hægt er að taka **OR**-samsetningar með í **IF**-yrðingu. Hér er dæmi: IF @Unit(SALES) OR @Unit(SALESWEST) THEN 5 ELSE @100 Hægt er að tilgreina einingu í takmörkun af útreikningsgerð á einn af eftirfarandi háttum:

- Færa inn heiti einingar til að taka með samsvarandi einingar. Til dæmis býður **IF @Unit(SALES)** upp á að reikna út fyrir hverja einingu sem kallast SALES, jafnvel þótt nokkrar einingar með heitinu SALES séu í skipuritinu.
- Færið inn heiti fyrirtækis og einingar til að takmarka útreikninginn tilgreindar einingar í tilgreindu fyrirtæki. Til dæmis færirðu inn **EF @Unit (ACME: VSK**) til að takmarka útreikning í SALES-eininga í ACME fyrirtækisinu.
- Færið inn fullan stigveldiskóðann úr skipuritinu til að takmarka útreikninginn við tiltekna einingu. Til dæmis færirðu inn **EF @Unit (SAMANTEKT ^ ACME ^ WEST COAST ^ VSK)**.

> [!NOTE]
> Til að finna fulla stigveldiskóðann skal hægrismella á skilgreiningu skipuritsins og velja síðan **Afrita kenni einingar skipurits (H-kóði)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Útreikningur takmarkaður við einingu skipurits

1. Smellið á **Línuskilgreiningar** í Report Designer og opnið svo línuskilgreininguna sem á að breyta.
2. Tvísmellið á hólfið **Sniðkóði** og veljið síðan **CAL**.
3. Smellið á hólfið **Tengdar formúlur/línur/einingar** og færið síðan inn skilyrta útreikninginn sem byrjar á **IF @Unit**.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF/THEN/ELSE-yrðingar í dálkskilgreiningu

**IF/THEN/ELSE**-yrðing býður upp á að allir útreikningar séu gerðir háðir niðurstöðum úr öðrum dálkum. Hægt er að vísa í aðra dálka en ekki í skýrsluhólf í **IF**-yrðingunni. Allir útreikningar verða að gilda fyrir allan dálkinn. Til dæmis táknar yrðingin **IF B&gt;100 THEN B ELSE C\*1,25** að „Ef upphæðin í dálki B er hærri en 100 skal færa gildið úr dálki B inn í dálkinn **CALC**. Ef upphæðin í dálki B er ekki hærri en 100 skal margfalda gildið í dálki C með 1,25 og færa niðurstöðuna inn í dálkinn **CALC**.“ **IF**-yrðingu skal ævinlega fylgja rökyrðing sem hægt er að meta sem sanna eða ósanna. Formúlurnar sem notaðar eru fyrir bæði **THEN**-setninguna og **ELSE**-klausuna geta innihaldið tilvísanir í hvaða fjölda dálka sem er og þessar formúlur geta verið eins flóknar og hver kýs.

> [!NOTE]
> Ekki er hægt að setja niðurstöður úr útreikningi í neinn annan dálk. Niðurstöðurnar verða að vera í þeim dálki sem inniheldur formúluna.

#### <a name="use-single-quotes-and-an-ampersand-for-dimension-values-in-a-row-column-or-tree"></a>Notaðu einfaldar gæsalappir og og-merkið fyrir víddargildi í röð, dálki eða skipuriti

Hægt er að hanna skýrslur með því að nota víddargildi sem inniheldur og-merkið (&).

Inn í hvaða **Tengja við fjárhagsvídd** reit er hægt að slá inn gildi á borð við **'P&L'**. Að hafa með einfaldar gæsalappir (' ') báðum megin við víddargildið gefur til kynna að verið sé að nota bókstaflegt gildi, t.d. að hafa með (&) og-merkið.
