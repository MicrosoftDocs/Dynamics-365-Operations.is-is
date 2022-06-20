---
title: Reglubundin verkefni í Endurteknum samningsreikningum
description: Þessi grein lýsir reglubundnum verkefnum sem eru tiltæk í Endurteknum samningsreikningum.
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904789"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Reglubundin verkefni í Endurteknum samningsreikningum

Þessi grein lýsir reglubundnum verkefnum sem eru tiltæk í Endurteknum samningsreikningum.

## <a name="generate-invoice"></a>Mynda reikning

Nota **Búðu til reikning** síðu til að búa til fjölda mánaðarlega endurtekna reikninga úr upplýsingum sem þú setur upp á **Allar innheimtuáætlanir** og **Skoða innheimtuupplýsingar** síður. Þegar reikningur er stofnaður er vörulýsing fyrir vinnslulínu sölupöntunar uppfærð með vörulýsingu og upphafs- og lokadagsetningum innheimtu fyrir áætlunarlínuna sem er reikningsfærð.

## <a name="generate-invoice-batch-processing"></a>Útbúa runuvinnslu reiknings

Nota **Búðu til lotuvinnslu reikninga** síðu til að búa til endurtekna reikninga í gegnum endurtekið lotuferli. Færibreyturnar sem eru tiltækar eru þær sömu og færibreyturnar á **Búðu til reikning** síðu, en hægt er að vista þær í lotuferli sem hægt er að keyra mörgum sinnum.

## <a name="price-update"></a>Verðuppfærsla

Notaðu Verðuppfærslutólið til að uppfæra verð nokkurra vara á mörgum innheimtuáætlunum í einni aðgerð. Verðin geta verið uppfærð miðað við annað hvort tiltekna prósentu eða tiltekna upphæð. Listi yfir línur sýnir aðeins núverandi einingarverð vörunnar. Það sýnir ekki verðin eftir verðuppfærsluna.

Athugaðu eftirfarandi atriði um verðuppfærslutólið:

- Ef sölupöntun fyrir tiltekið ár hefur þegar verið stofnuð (þ.e. vörurnar hafa verið rukkaðar) hefur það ekki áhrif á verð línunnar.
- Hægt er að nota Verðuppfærslutólið fyrir línur sem hafa stöðuna **Virkur** eða **Á bið**. Fyrir hluti sem eru í biðstöðu, **Stilla áætlun** valkostur verður að hafa verið stilltur á **Nei** þegar gripið var komið fyrir.
- Verðuppfærslutólið er ekki hægt að nota fyrir línur sem eru notkunarvörur, sem nota stigmögnun, áfangareikninga eða tekjuskiptingu.

### <a name="price-update-example"></a>Dæmi um verðuppfærslu

Innheimtuáætlun er búin til og endurnýjunaratriði er bætt við. Einingaverðið er $750. Fyrsta ár hlutarins er greitt 15. desember 2021. Innheimtuáætlunin er búin til fyrir tímabilið frá 1. janúar til 31. desember 2022.

Á endurnýjunartíma er **Búðu til reikning** ferli býr til sölupöntun fyrir árið 2022. Eftir að verðuppfærsluforritið er keyrt er verðið uppfært úr $750 í $800.

Sölupöntun og innheimtuáætlun fyrir árið 2022 hefur ekki áhrif og einingarverð er áfram $750, vegna þess að innheimtuáætlun fyrir árið 2022 hefur þegar verið innheimt. Innheimtuáætlunarlínan og línuupplýsingar fyrir 2023 eru uppfærðar í $800, vegna þess að innheimtuáætlun fyrir 2023 hefur ekki verið innheimt ennþá.

### <a name="update-prices--flat-pricing-method"></a>Uppfærðu verð – Flöt verðlagningaraðferð

Þegar þú uppfærir verð fyrir vörur sem nota flata verðlagningaraðferð geturðu tilgreint prósentu eða upphæð til að hækka verðið.

Til að keyra verðuppfærslutólið fyrir vörur sem nota fasta verðlagningu, fylgdu þessum skrefum.

1. Á **Verðuppfærsla** tólasíðu, veldu **Flat** verðlagningaraðferð.
2. Í **Auka aðferð** reit, veldu hækkunaraðferðina sem er notuð til að uppfæra verð vörunnar.
3. Það fer eftir hækkunaraðferðinni sem þú valdir, tilgreindu prósentuna í **Prósenta** reit eða upphæðin í **Magn** sviði.
4. Á **Skrár til að hafa með** flýtiflipann, notaðu **Sía** hnappinn til að bæta við gagnasíum.
5. Veldu **Skoða forskoðun** til að skoða færslusviðið.
6. Ef þú vilt ekki vinna úr einhverjum línum, merktu þær og veldu síðan **Fjarlægja**.
7. Veldu **Í lagi**.

### <a name="update-prices--standard-pricing-method"></a>Uppfærðu verð – Venjuleg verðlagningaraðferð

Ef verði vöru hefur verið breytt í vöruskránni er hægt að uppfæra það fyrir allar greiðsluáætlunarlínur ef varan notar staðlaða verðlagningaraðferð.

1. Á **Verðuppfærsla** tólasíðu, veldu **Standard** verðlagningaraðferð.
2. Á **Skrár til að hafa með** flýtiflipann, notaðu **Sía** hnappinn til að bæta við gagnasíum.
3. Veldu **Skoða forskoðun** til að skoða færslusviðið.
4. Ef þú vilt ekki vinna úr einhverjum línum, merktu þær og veldu síðan **Fjarlægja**.
5. Veldu **Í lagi**.

## <a name="mass-hold-processing"></a>Fjöldaúrvinnsla biðstöðu

Nota **Messuhald** síðu til að beita biðmöguleikum á nokkrar innheimtuáætlanir á sama tíma.

Til að setja eina innheimtuáætlun eða eina innheimtuáætlunarlínu í bið skaltu opna **Allar innheimtuáætlanir** síðu og veldu **Settu haltu**. Til að fjarlægja bið skaltu nota **Fjarlægðu bið** síðu.

### <a name="put-billing-schedules-on-hold"></a>Settu innheimtuáætlanir í bið

Fylgdu þessum skrefum til að stöðva nokkrar innheimtuáætlanir.

1. Á **Messuhald** síðu, stilltu **Vinnsluvalkostur** sviði til **Notaðu bið**.
2. Í **Ástæðukóði** reit, veldu ástæðukóða.
3. Stilltu **Stilla áætlun** valmöguleiki:

    - **Já** – Ef þú stillir valkostinn á **Já**, tilgreindu biðdagsetningu í **Haltu dagsetningu** sviði. Allar innheimtuáætlunarlínur eftir biðdagsetningu eru fjarlægðar.
    - **Nei** – Innheimtuáætlunarlínum er ekki breytt. Aðeins stöðunni er breytt. Það er uppfært í **Á bið**.

4. Á **Skrár til að hafa með** flýtiflipann, notaðu **Sía** hnappinn til að bæta við gagnasíum.
5. Veldu **Skoða forskoðun** til að skoða færslusviðið.
6. Ef þú vilt ekki vinna úr einhverjum línum, merktu þær og veldu síðan **Fjarlægja**.
7. Veldu **Í lagi**.

Þegar þú ferð aftur í listann yfir innheimtuáætlanir ættirðu að sjá að stöðu innheimtuáætlana hefur verið breytt í **Á bið**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Fjarlægðu bið frá nokkrum innheimtuáætlunum

1. Á **Messuhald** síðu, stilltu **Vinnsluvalkostur** sviði til **Fjarlægðu bið**.
2. Í **Ástæðukóði** reit, sláðu inn ástæðukóða.
3. Í **Fjarlægja dagsetningu** reit, veldu dagsetningu þegar biðin ætti að fjarlægja.
4. Stilltu **Dagsetning endurupptöku** og **Frestunardagur** reiti eins og þú þarfnast. Frestunardagsetningin bætist við allar línur sem eru frestaðhæfar.
5. Á **Skrár til að hafa með** flýtiflipann, notaðu **Sía** hnappinn til að bæta við gagnasíum.
6. Veldu **Skoða forskoðun** til að skoða færslusviðið.
7. Ef þú vilt ekki vinna úr einhverjum línum, merktu þær og veldu síðan **Fjarlægja**.
8. Veldu **Í lagi**.

> [!NOTE]
> Til að fjarlægja bið verður þú að stilla á **Fjarlægja hnekkingu bið notendahóps** gildi á **Endurteknar innheimtufæribreytur samnings** síðu.

Til dæmis hefur innheimtulína upphafsdagsetninguna 1. febrúar 2022 og lokadagsetninguna 28. febrúar 2022. Innheimtuupphæðin er $200. The **Haltu dagsetningu** reiturinn er stilltur á 10. febrúar 2022. Þess vegna er febrúartímabilið leiðrétt til að útiloka hvaða dagsetningu sem er eftir 10. febrúar. Nýja tímabilið er frá 1. febrúar til og með 9. febrúar og upphæðin er $64.29 (með daglegum hlutföllum). Allar innheimtuáætlunarlínur 10. febrúar eða síðar eru fjarlægðar.

Ef **Fjarlægðu bið** ferlinu er lokið og **Fjarlægja dagsetningu** reitinn er stilltur á 10. febrúar 2022, það verða tvö innheimtutímabil. Fyrsta innheimtutímabilið er frá 1. febrúar til 9. febrúar og upphæðin er $64.29. Annað innheimtutímabil er frá 10. febrúar til og með 28. febrúar og upphæðin er $135.71.

## <a name="mass-termination-processing"></a>Úrvinnsla fjöldauppsagnar

Nota **Fjöldauppsögn** síðu til að slíta innheimtuáætlunarlínum sem eru sýndar með því að tilgreina uppsagnardagsetningu.

Ef þú ert að nota frestun tekna og gjalda, innheimtuáætlanir þar sem **Uppsagnardagur** reiturinn er stilltur á **Stilla áætlun** á **Allar innheimtuáætlanir** síðu eru gjaldgeng fyrir endurgreiðslu.

Innheimtuáætlanir sem nota margfeldisúthlutun (MEA) virkni birtast ekki á **Fjöldauppsögn** síðu. Þú getur samt sagt upp einstaka innheimtuáætlun með því að nota uppsagnaraðgerðina á innheimtuáætluninni.

> [!NOTE]
> Innheimtuáætlunarlínur sem nú eru innifalin í a **Búðu til reikning** lotur eru ekki tiltækar fyrir þetta ferli.

Fyrir upplýsingar um hvern reit og ferlið, sjá [Hætta innheimtuáætlunum](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Ferli fjöldasafnvistunar

Nota **Messuskjalasafn** síðu til að geyma margar innheimtuáætlanir. Aðeins er hægt að geyma uppsagnar greiðsluáætlanir.

Eftir að innheimtuáætlun hefur verið sett í geymslu eiga sér stað eftirfarandi atburðir:

- Staðan er breytt í **Sett í geymslu**.
- Innheimtuáætlanir eru varanlega læstar.
- Innheimtuáætlunarlínurnar eru ekki lengur tiltækar á fyrirspurnasíðum.

> [!NOTE]
> Geymsla á innheimtuáætlun er varanleg aðgerð og ekki er hægt að snúa henni við.

Fylgdu þessum skrefum til að setja innheimtuáætlanir í geymslu.

1. Á **Messuskjalasafn** síðu, í **Lokadagur innheimtu** reit, tilgreinið lokadagsetningu innheimtu. Til að skoða allar uppsagnar greiðsluáætlanir skaltu skilja þennan reit eftir auðan.
2. Á **Skrár til að hafa með** flýtiflipann, notaðu **Sía** hnappinn til að takmarka færslurnar sem eru sýndar.
3. Veldu **Skoða forskoðun**.
4. Ef þú vilt ekki setja sumar skrárnar í geymslu skaltu merkja þær og velja síðan **Fjarlægja**.
5. Veldu **Allt í lagi** til að geyma skrárnar á síðunni.

## <a name="mass-stubbing-process"></a>Fjöldavinnsla styttingar

Nota **Massa stubbur** síðu til að merkja allar valdar innheimtuáætlunarlínur sem innheimt (stubbur) eða óinnheimtur (öfugur stubbur). Stubbun eða öfug stubbun er oftast framkvæmd á innfluttum innheimtuáætlunarlínum sem áður voru innheimtar í öðru kerfi. Stubbaðar innheimtuáætlunarlínur birtast sem stubbaðar og munu ekki búa til reikning fyrir viðskiptavininn.

### <a name="stub-records"></a>Stubbaskrár

1. Á **Massa stubbur** síðu, í **Vinnsluvalkostir** reit, veldu **Stubbur**.
2. Í **Lokadagur** reit, stilltu lokadagsetningu til að tilgreina línurnar sem þú vilt nota ferlið á. Aðeins færslur þar sem upphafsdagur innheimtu er á eða fyrir tilgreindan lokadag verða sýndar.
3. Veldu **Skoða forskoðun** til að sýna línurnar sem þú vilt stubba.
4. Til að útiloka línu frá ferlinu skaltu merkja hana og velja síðan **Fjarlægja**.
5. Veldu **Ferli** að stinga línurnar.

### <a name="reverse-stub-records"></a>Snúið stubbaskrár

1. Á **Massa stubbur** síðu, í **Vinnsluvalkostir** reit, veldu **Reverse stubbur**.
2. Í **Lokadagur** reit, stilltu lokadagsetningu til að tilgreina línurnar sem þú vilt nota ferlið á. Aðeins færslur þar sem upphafsdagur innheimtu er á eða fyrir tilgreindan lokadag verða sýndar.
3. Veldu **Skoða forskoðun** til að sýna línurnar sem þú vilt snúa við stubbnum.
4. Til að útiloka línu frá ferlinu skaltu merkja hana og velja síðan **Fjarlægja**.
5. Veldu **Ferli** að snúa við stubbnum línum.

## <a name="update-completion-date-process"></a>Uppfæra ferli fyrir dagsetningu loka

Nota **Lokadagur uppfærslu** síðu til að uppfæra lokadagsetningu fyrir ákveðin tímamótaatriði fyrir margar innheimtuáætlanir eða notendur. Þú getur líka uppfært lokaprósentu fyrir hluti á áfangasniðmátum sem nota **Prósenta lokið** aðferð.

1. Á **Lokadagur uppfærslu** síðu, farðu á **Áfangavinnsla**, og veldu **Uppfærsluprósentu lokið**.
2. Í **Hlutfallsupphæð** reit, sláðu inn heildarprósentu sem hefur verið lokið.
3. Veldu vörunúmerið sem tengist áfangasniðmátinu.
4. Á **Skrár til að hafa með** Flýtiflipi, veldu **Sía** til að velja tiltekið **Notendareikningur**, **innheimtuáætlunar**, eða **Vörunúmer** gildi sem síuviðmiðun.
5. Veldu **Allt í lagi** að afgreiða breytinguna. Þegar vinnslu er lokið bætist ný lína við áfangaúthlutun. Þessi lína táknar prósentuna sem hefur verið lokið fyrir áfangasniðmátið.

## <a name="unbilled-revenue-mass-processing"></a>Fjöldavinnsla óreikningsfærðra tekna

Nota **Óreikningsfærð tekjur fjöldavinnsla** síðu til að búa til óinnheimtu tekjubókarfærsluna eða stubba færslubókina fyrir eina eða fleiri valdar innheimtuáætlanir eða innheimtuupplýsingarlínur.

- **Stofna dagbókarfærslu** – Búðu til óinnheimtar tekjubókarfærslur fyrir margar innheimtuáætlunarlínur. Nota **Sía** hnappinn á **Skrár til að hafa með** Flýtiflipa til að velja svið skráa sem birtast á listanum. Listinn sýnir aðeins innheimtuáætlunarlínur sem óinnheimtar tekjubókarfærslur hafa ekki verið stofnaðar fyrir. Fyrstu dagbókarfærslurnar eru búnar til. Fyrir frestunarliði eru frestunaráætlanir einnig búnar til.
- **Stubbur dagbókarfærsla** – Merktu innheimtuáætlunarlínurnar sem óinnheimtu færslubókarfærslurnar hafa þegar verið stofnaðar fyrir. Þessi valkostur er notaður ef óinnheimta færslubókarfærslan var þegar bókuð í öðru kerfi. Það merkir óinnheimtu tekjubókina sem stubbað og bókar ekki færslu í fjárhag.
- **Snúið dagbókarfærslu stubbs** – Bakfæra stubbabókarfærslur sem hafa verið unnar. Ef mistök urðu við vinnslu fyrir **Stubbur dagbókarfærsla**, þessi valkostur mun hreinsa **Stubbaður** gátreit fyrir innheimtuáætlunarlínuna.
- **Stubbur innheimtuupplýsingalína** – Notaðu þetta ferli þegar óinnheimtar tekjur voru unnar í ytra kerfi og sumar reikningsupplýsingalínanna hafa þegar verið innheimtar. Þetta ferli mun tryggja að rétt upphæð birtist á óinnheimtu tekjureikningunum.
- **Snúið innheimtuupplýsingar línu** – Snúa einhverju við **Stubbur innheimtuupplýsingalína** aðgerðir.

The **Nafn dagbókar** reiturinn er notaður til að birta **Stofna dagbókarfærslu** í aðalbók.

> [!NOTE]
> Stubbaferlið bókar upphæðir ekki í fjárhag. The **Nafn dagbókar** reiturinn er ekki tiltækur fyrir alla stubba og öfuga stubbaferli.

### <a name="unbilled-revenue-stub-example"></a>Dæmi um óinnheimt tekjustubb

Innheimtuáætlun er sett upp til eins árs, frá október 2021 til september 2022. Óinnheimtu tekjur voru þegar unnar í ytra kerfi. Níu mánuðir af innheimtuáætlun hafa þegar verið rukkaðir. Upphæð hvers innheimtutímabils er $250. Í upphafi árs er heildarupphæðin sem hefur verið færð í óinnheimt tekjur $3,000. Eftir níu mánuði hefur $2,250 þegar verið innheimt og $750 í óinnheimtu tekna eftir.

Fylgdu þessum skrefum til að setja upp innheimtuáætlun þar sem aðeins þriggja mánaða óinnheimt tekjur eru eftir.

1. Á **Skoða innheimtuupplýsingar** síðu, búðu til innheimtuáætlun fyrir tímabilið frá október 2021 til september 2022, vörunúmer S0001 og upphæð $250 á mánuði.
2. Veldu **Stofna dagbókarfærslu** fyrir innheimtuáætlun. Upphæð $3,000 er færð í óinnheimt tekjur.
3. Veldu **Stubbur innheimtuupplýsingalína**, og tilgreindu viðskiptadagsetningu júní 2022 (níu mánuðir). Innheimtuáætlunarlínurnar birtast ekki í forskoðuninni. Línurnar sem verða fyrir áhrifum eru byggðar á færsludegi.
4. Veldu **Í lagi**.

Fyrstu níu mánuðirnir sem hafa verið rukkaðir eru stubbaðir.

[![Skoða innheimtuupplýsingar línur stubb.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

$3,000 er bakfært frá óinnheimtutekjum og $750 í óinnheimtutekjum sem eftir eru færðar. Til að skoða óreikningsfærðar tekjufærslur velurðu **Úttekt á óinnheimtu tekjubókarfærslu** á **Endurnýjun** flipa línuupplýsingasíðunnar.

[![Úttekt á óinnheimtu tekjubókarfærslu.](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Óinnheimtu tekjubókarfærsluna er hægt að búa til fyrir hvaða endurnýjunartímabil sem er, að því tilskildu að allar innheimtuupplýsingarlínur frá fyrra tímabili hafi verið innheimtar. Til dæmis hefur innheimtuáætlunarlína mánaðarlega innheimtutíðni fyrir 12 mánaða tímabil, frá janúar til desember 2021. Línan hefur þrjú kjörtímabil: upphafstímabil, annað kjörtímabil (janúar til desember 2022) og þriðja tíma (janúar til desember 2023). Eftir að reikningurinn hefur verið búinn til fyrir allar línur innheimtuupplýsinga frá fyrstu 12 mánuðum ársins 2021, er hægt að stofna færslubók fyrir óinnheimtaðar tekjur fyrir annað tímabilið.
>
> Fyrir frestunarvörur sem nota óinnheimtu teknaeiginleikann eru innheimtulínan og afsláttarlínurnar unnar. Fyrir þessar vörur eru óinnheimtuð tekjubókarfærsla og frestunaráætlun fyrir innheimtulínuna og afsláttarlínuna stofnuð.
>
> Færslubókarfærslurnar sem eru búnar til fyrir ófrestanlegar vörur og frestanlegar vörur bóka inneign á mismunandi tekjureikninga.
