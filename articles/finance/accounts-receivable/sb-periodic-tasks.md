---
title: Reglubundin verkefni í „Endurteknar samningsgreiðslur“
description: Þessi grein lýsir reglubundnum verkum sem eru í boði í endurtekinni samningsgreiðslu.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904789"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Reglubundin verkefni í „Endurteknar samningsgreiðslur“

Þessi grein lýsir reglubundnum verkum sem eru í boði í endurtekinni samningsgreiðslu.

## <a name="generate-invoice"></a>Mynda reikning

Notaðu síðuna **Búa til reikning** til að búa til fjölda mánaðarlegra endurtekinna reikninga úr upplýsingunum sem eru settar upp á síðunum **Allar greiðsluáætlanir** og **Skoða greiðsluupplýsingar**. Þegar reikningur er búinn til er vörulýsingin fyrir línu sölupöntunarvinnslu uppfærð með vörulýsingunni og upphafs- og lokadagsetningum greiðslu fyrir greiðslulínuna sem er reikningsfærð.

## <a name="generate-invoice-batch-processing"></a>Útbúa runuvinnslu reiknings

Notaðu síðuna **Búa til runuvinnslu reiknings** til að búa til endurtekna reikninga í gegnum endurtekna runuvinnslu. Færibreyturnar sem eru tiltækar eru þær sömu og færibreyturnar á síðunni **Búa til reikning**, en hægt er að vista þær í runuvinnslu sem hægt er að keyra mörgum sinnum.

## <a name="price-update"></a>Verðuppfærsla

Nota verðuppfærsluna til að uppfæra verð á nokkrum vörum í mörgum greiðsluáætlunum í einni aðgerð. Hægt er að uppfæra verðin út frá annaðhvort tiltekinni prósentu eða tiltekinni upphæð. Listi yfir línur sýnir eingöngu núgildandi einingarverð varanna. Verðin koma ekki fram eftir verðuppfærsluna.

Gæta skal eftirfarandi atriða um verðuppfærsluverkfærið:

- Ef sölupöntun fyrir tiltekið ár hefur þegar verið stofnuð (þ.e. vörurnar hafa verið reikningsfærðar) hefur það ekki áhrif á verð vörulínunnar.
- Hægt er að nota verðuppfærsluna fyrir vörulínur sem eru með stöðuna **Virkt** eða **Í biðstöðu**. Fyrir vörur sem eru í biðstöðu verður valkosturinn **Breyta áætlun** að hafa verið stilltur á **Nei** þegar biðstaðan var sett á.
- Ekki er hægt að nota verðuppfærsluna fyrir vörulínur sem eru notkunarvörur, sem nota stighækkun, áfangagreiðslu eða tekjuskiptingu.

### <a name="price-update-example"></a>Dæmi um uppfært verð

Greiðsluáætlun er búin til og vöru endurnýjunar er bætt við. Einingarverðið er $750. Fyrsta ár vörunnar er greitt 15. desember 2021. Greiðsluáætlunin er gerð fyrir tímabilið frá 1. janúar til 31. desember 2022.

Við endurnýjunartíma stofnar ferlið **Búa til reikning** sölupöntunina fyrir árið 2022. Eftir að verðuppfærslan er keyrð er verðið uppfært úr $750 í $800.

Sölupöntun og greiðsluáætlun fyrir 2022 verða ekki fyrir áhrifum og einingarverðið helst í $750 því að greiðsluáætlun fyrir 2022 hefur þegar verið reikningsfærð. Greiðsluáætlunarlínan og línuupplýsingarnar fyrir 2023 eru uppfærðar í $800 því að greiðsluáætlunin fyrir 2023 hefur ekki enn verið reikningsfærð.

### <a name="update-prices--flat-pricing-method"></a>Uppfært verð – Flöt verðlagning

Þegar verð eru uppfærð fyrir vörur sem nota fasta verðlagningaraðferð er hægt að tilgreina prósentu eð aupphæð til að hækka verðið.

Til að keyra verðuppfærsluna fyrir vörur sem nota fasta verðlagningaraðferð skal fylgja þessum skrefum.

1. Á síðunni **Verðuppfærsla** skal velja verðlagningaraðferðina **Fast**.
2. Í reitnum **Hækkunaraðferð** skal velja hækkunaraðferðina sem er notuð til að uppfæra verð á vörunum.
3. Það fer eftir hækkunaraðferðinni sem er valin hvort tilgreina eigi prósentu í reitnum **Prósenta** eða upphæð í reitnum **Upphæð**.
4. Í flýtiflipanum **Færslur til að taka með** skal nota hnappinn **Sía** til að bæta við gagnasíum.
5. Veldu **Skoða forskoðun** til að skoða færslusvið.
6. Ef ekki á að vinna úr einhverjum línum skal merkja þær og síðan velja **Fjarlægja**.
7. Veldu **Í lagi**.

### <a name="update-prices--standard-pricing-method"></a>Uppfært verð – Hefðbundin verðlagnin

Ef verði á vöru hefur verið breytt í færslu vörunnar er hægt að uppfæra það fyrir allar greiðsluáætlunarlínur ef varan notar staðlaða verðlagningaraðferð.

1. Á síðunni **Verðuppfærsla** skal velja verðlagningaraðferðina **Staðlað**.
2. Í flýtiflipanum **Færslur til að taka með** skal nota hnappinn **Sía** til að bæta við gagnasíum.
3. Veldu **Skoða forskoðun** til að skoða færslusvið.
4. Ef ekki á að vinna úr einhverjum línum skal merkja þær og síðan velja **Fjarlægja**.
5. Veldu **Í lagi**.

## <a name="mass-hold-processing"></a>Fjöldaúrvinnsla biðstöðu

Notaðu síðuna **Fjöldabið** til að setja nokkrar greiðsluáætlanir í biðstöðu á sama tíma.

Til að setja aðeins eina greiðsluáætlun eða eina greiðsluáætlunarlínu í bið skal opna síðuna **Allar greiðsluáætlanir** og velja **Setja í bið**. Til að fjarlægja bið skal nota síðuna **Fjarlægja bið**.

### <a name="put-billing-schedules-on-hold"></a>Setja greiðsluáætlanir í bið

Til að setja nokkrar greiðsluáætlanir í bið skal fylgja þessum skrefum.

1. Á síðunni **Fjöldabið** skal stilla reitinn **Valkostur vinnslu** á **Setja í bið**.
2. Á svæðinu **Ástæðukóði** skal velja ástæðukóða.
3. Stillið valkostinn **Breyta áætlun**:

    - **Já** – Ef valkosturinn er stilltur á **Já** skal tilgreina biðdagsetningu í reitnum **Biðdagsetning**. Allar greiðsluáætlunarlínur eftir biðdagsetninguna eru fjarlægðar.
    - **Nei** – Greiðsluáætlunarlínum er ekki breytt. Eingöngu stöðunni er breytt. Er uppfært í **Í bið**.

4. Í flýtiflipanum **Færslur til að taka með** skal nota hnappinn **Sía** til að bæta við gagnasíum.
5. Veldu **Skoða forskoðun** til að skoða færslusvið.
6. Ef ekki á að vinna úr einhverjum línum skal merkja þær og síðan velja **Fjarlægja**.
7. Veldu **Í lagi**.

Þegar farið er aftur á listann yfir greiðsluáætlanir ættirðu að sjá að staðan á greiðsluáætlunum hefur verið breytt í **Í biðstöðu**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Fjarlægja bið af nokkrum greiðsluáætlunum

1. Á síðunni **Fjöldabið** skal stilla reitinn **Valkostur vinnslu** á **Fjarlægja biðstöðu**.
2. Í reitnum **Ástæðukóði** skal slá inn ástæðukóða.
3. Í reitnum **Dagsetning fjarlægingar** skal velja dagsetninguna þegar fjarlægja á biðstöðuna.
4. Stilltu reitina **Dagsetning áframhalds** og **Dagsetning frestunar** eftir þörfum. Frestunardegi er bætt við allar línur sem hægt er að fresta.
5. Í flýtiflipanum **Færslur til að taka með** skal nota hnappinn **Sía** til að bæta við gagnasíum.
6. Veldu **Skoða forskoðun** til að skoða færslusvið.
7. Ef ekki á að vinna úr einhverjum línum skal merkja þær og síðan velja **Fjarlægja**.
8. Veldu **Í lagi**.

> [!NOTE]
> Til að fjarlægja biðstöðu þarf að stilla gildið **Hnekkja notendaflokki fyrir fjarlægingu biðstöðu** á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.

Til dæmis er greiðslulína með upphafsdagsetninguna 1. febrúar 2022 og lokadagsetninguna 28. febrúar 2022. Greiðsluupphæðin er $200. Reiturinn **Biðtími** er stilltur á 10. febrúar 2022. Því er febrúartímabilið leiðrétt til að útiloka allar dagsetningar eftir 10. febrúar. Nýja tímabilið er frá 1. febrúar til og með 9. febrúar og upphæðin er $64,29 (með daglegri hlutfallsskiptingu). Allar greiðsluáætlunarlínur á eða eftir 10. febrúar eru fjarlægðar.

Ef ferlinu **Fjarlægja biðstöðu** er lokið og reiturinn **Dagsetning fjarlægingar** er stilltur á 10. febrúar 2022 verða tvöö greiðslutímabil. Fyrsta greiðslutímabilið er frá 1. febrúar til og með 9. febrúar og upphæðin er $64,29. Seinna greiðslutímabilið er frá 10. febrúar til og með 28. febrúar og upphæðin er $135,71.

## <a name="mass-termination-processing"></a>Úrvinnsla fjöldauppsagnar

Notaðu síðuna **Fjöldauppsögn** til að segja upp greiðsluáætlunarlínum sem eru sýndar með því að tilgreina uppsagnardag.

Ef þú ert að notar tekju- og kostnaðarfrestanir eiga greiðsluáætlanir þar sem reiturinn **Dagsetning uppsagnar** er stilltur á **Breyta áætlun** á síðunni **Allar greiðsluáætlanir** rétt á endurgreiðslu.

Greiðsluáætlanir sem nota úthlutunaraðferð margra eininga birtast á síðunni **Fjöldauppsögn**. Enn er hægt að segja upp einstaka greiðsluáætlun með því að nota uppsagnaraðgerðina í greiðsluáætluninni.

> [!NOTE]
> Greiðsluáætlunarlínur sem eru nú í rununni **Búa til reikning** eru ekki í boði fyrir þetta ferli.

Frekari upplýsingar um hvern reit og ferlið er að finna í [Segja upp greiðsluáætlunum](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Ferli fjöldasafnvistunar

Notaðu síðuna **Fjöldasafnvistun** til að safnvista mörgum greiðsluáætlunum. Aðeins er hægt að safnvista riftar greiðsluáætlanir.

Þegar greiðsluáætlun hefur verið safnvistuð gerast eftirfarandi tilvik:

- Stöðunni er breytt í **Safnvistað**.
- Greiðsluáætlanir eru læstar til frambúðar.
- Greiðsluáætlunarlínur eru ekki lengur í boði á fyrirspurnarsíðum.

> [!NOTE]
> Safnvistun greiðsluáætlunar er varanleg aðgerð og ekki er hægt að afturkalla hana.

Til að safnvista greiðsluáætlanir skal fylgja eftirfarandi skrefum.

1. Á síðunni **Fjöldasafnvistun** í reitnum **Lokadagsetning innheimtu** skal tilgreina lokadagsetningu innheimtu. Til að skoða allar greiðsluáætlanir sem búið er að segja upp skal skilja þennan reit eftir auðan.
2. Í flýtiflipanum **Færslur til að taka með** skal nota hnappinn **Sía** til að takmarka færslurnar sem eru sýndar.
3. Veljið **Skoða forútgáfu**.
4. Ef ekki á að safnvista sumar færslurnar skal merkja þær og síðan velja **Fjarlægja**.
5. Veljið **OK** til að vista færslurnar á síðunni.

## <a name="mass-stubbing-process"></a>Fjöldavinnsla styttingar

Notaðu síðuna **Fjöldastytting** til að merkja valdar greiðsluáætlunarlínur sem innheimtar (styttar) eða óinnheimtar (bakfæra styttingu). Stytting eða bakfærð stytting eru oftast framkvæmd á innfluttum greiðsluáætlunarlínum sem voru áður innheimtar í öðru kerfi. Styttar greiðsluáætlunarlínur birtast sem styttar og búa ekki til reikning fyrir viðskiptavininn.

### <a name="stub-records"></a>Styttingarfærslur

1. Á síðunni **Fjöldastytting** skal í reitnum **Vinnsluvalkostir** velja **Stytting**.
2. Í reitnum **Lokadagsetning** skal stilla lokadagsetningu til að tilgreina línur sem nota á í ferlinu. Aðeins færslur þar sem upphafsdagsetning greiðslu er á eða á undan tilgreindri lokadagsetningu verða sýndar.
3. Veldu **Skoða forskoðun** til að sýna línurnar sem á að stytta.
4. Til að útiloka línu frá ferlinu skaltu merkja hana og velja svo **Fjarlægja**.
5. Veldu **Vinna úr** til að stytta línurnar.

### <a name="reverse-stub-records"></a>Bakfæra styttar færslur

1. Á síðunni **Fjöldastytting** skal í reitnum **Vinnsluvalkostir** velja **Bakfæra styttingu**.
2. Í reitnum **Lokadagsetning** skal stilla lokadagsetningu til að tilgreina línur sem nota á í ferlinu. Aðeins færslur þar sem upphafsdagsetning greiðslu er á eða á undan tilgreindri lokadagsetningu verða sýndar.
3. Veldu **Skoða forskoðun** til að sýna línurnar sem á að bakfæra styttingu.
4. Til að útiloka línu frá ferlinu skaltu merkja hana og velja svo **Fjarlægja**.
5. Veldu **Vinna úr** til að bakfæra styttingu línanna.

## <a name="update-completion-date-process"></a>Uppfæra ferli fyrir dagsetningu loka

Notaðu síðuna **Uppfæra dagsetningu loka** til að uppfæra dagsetningu loka fyrir tilteknar vörur áfanga fyrir margar greiðsluáætlanir eða notendur. Einnig er hægt að uppfæra prósentu yfir það sem er lokið fyrir vörur í áfangasniðmátum sem nota aðferðina **Prósentum lokið**.

1. Á síðunni **Uppfæra dagsetningu loka** skal fara í **Úrvinnsla áfanga** og velja **Uppfæra prósentu sem er lokið**.
2. Í reitinn **Prósentuhlutfall** skal færa inn heildarprósentuna sem er lokið.
3. Veldu vörunúmerið sem tengist áfangasniðmátinu.
4. Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að velja tiltekið gildi fyrir **Notandareikning**, **Greiðsluáætlunarnúmer** eða **Vörunúmer** sem síuskilyrði.
5. Veldu **Í lagi** til að vinna breytinguna. Nýrri línu er bætt við þáttaskilaúthlutun þegar vinnslu er lokið. Þessi lína táknar prósentuna sem er lokið fyrir áfangasniðmátið.

## <a name="unbilled-revenue-mass-processing"></a>Fjöldavinnsla óreikningsfærðra tekna

Notaðu síðuna **Fjöldavinnsla óreikningsfærðra tekna** til að stofna óreikningsfærða færslu í tekjubókinni eða stytta færslu færslubókar fyrir eina eða fleiri greiðsluáætlanir eða greiðsluupplýsingalínur.

- **Stofna færslu í færslubók** – Stofnaðu óreikningsfærðar færslur í færslubók fyrir margar greiðsluáætlunarlínur. Notaðu hnappinn **Sía** í flýtiflipanum **Færslur til að taka með** til að velja færslubilið sem á að birtast í listanum. Listinn sýnir aðeins greiðsluáætlunarlínur sem óreikningsfærðar færslur í tekjubókinni hafa ekki verið stofnaðar fyrir. Upphaflegar bókarfærslur eru stofnaðar. Fyrir frestunarvörur eru frestunaráætlanir líka búnar til.
- **Stytt færsla í færslubók** – Merktu greiðsluáætlunarlínurnar sem óreikningsfærðar færslur færslubókar hafa þegar verið stofnaðar fyrir. Þessi valkostur er notaður ef óreikningsfærð færsla í færslubók var þegar bókuð í öðru kerfi. Hann merkir óreikningsfærða tekjubók sem stytta og bókar ekki færslu í fjárhaginn.
- **Bakfæra stytta færslu í færslubók** – Bakfærðar styttar færslur í færslubók hafa verið afgreiddar. Ef mistök voru gerð við vinnslu fyrir **Stytta færslu í færslubók** mun þessi valkostur hreinsa gátreitinn **Stytt** fyrir greiðsluáætlunarlínuna.
- **Stytt upplýsingalína greiðslu** – Notaðu þetta ferli þegar óreikningsfærðar tekjur voru afgreiddar í ytra kerfinu og sumar upplýsingalínur reikningsfærslu hafa þegar við reikningsfærðar. Þetta ferli mun tryggja að rétt upphæð birtist í óreikningsfærðum tekjulyklum.
- **Bakfæra upplýsingalínu greiðslustyttingar** – Bakfærðu allar aðgerðir **Stytta línu greiðsluupplýsinga**.

Reiturinn **Heiti færslubókar** er notað til að bóka **Stofna færslu í færslubók** í fjárhaginn.

> [!NOTE]
> Styttingarferlið bókar ekki upphæðir í fjárhaginn. Reiturinn **Heiti færslubókar** er ekki í boði fyrir öll styttingar- og bakfærð styttingarferli.

### <a name="unbilled-revenue-stub-example"></a>Dæmi um óreikningsfærða tekjustyttingu

Greiðsluáætlun er sett upp til eins árs, frá október 2021 til september 2022. Óreikningsfærðar tekjur voru þegar afgreiddar í ytra kerfi. Níu mánuðir af greiðsluáætlun hafa þegar verið reikningsfærðar. Upphæðin fyrir hvert reikningstímabil er $250. Í upphafi árs er heildarupphæðin sem hefur verið bókuð á óreikningsfærðar tekjur samtals $3.000. Eftir níu mánuði hafa $2.250 þegar verið reikningsfærð og $750 í óreikningsfærðar tekjur standa eftir.

Til að setja upp greiðsluáætlunina þar sem aðeins þrír mánuðir af óreikningsfærðum tekjum standa eftir skal fylgja þessum skrefum.

1. Á síðunni **Skoða greiðsluupplýsingar** skal búa til greiðsluáætlun fyrir tímabilið frá október 2021 til og með september 2022, vörunúmer S0001 og upphæðina $250 á mánuði.
2. Veldu **Stofna færslu í færslubók** fyrir greiðsluáætlunina. $3000 eru lagðir inn á óreikningsfærðar tekjur.
3. Veldu **Stytta línu greiðsluupplýsinga** og tilgreindu færsludagsetningu í júní 2022 (níu mánuðir). Línur greiðsluáætlunar birtast ekki í forskoðuninni. Línurnar sem verða fyrir áhrifum byggjast á færsludagsetningunni.
4. Veldu **Í lagi**.

Fyrstu níu mánuðirnir sem hafa verið innheimtir eru styttir.

[![Skoða styttar upplýsingalínur greiðslu.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

$3.000 eru bakfærðar úr óreikningsfærðum tekjum og $750 í óreikningsfærðar tekjur sem standa eftir er bókað. Til að skoða óreikningsfærðar tekjubókanir skal velja **Eftirlit með bókarfærslu óreikningsfærðra tekna** í flipanum **Endurnýjanir** á síðu upplýsingalínunnar.

[![Eftirlit með bókarfærslu óreikningsfærðra tekna](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Hægt er að stofna færslu tekjubókar fyrir öll endurnýjunartímabil svo lengi sem upplýsingalínur greiðslu frá síðasta tímabili hafi verið reikningsfærðar. Til dæmis er greiðsluáætlunarlína með mánaðarlega greiðslutíðni fyrir 12 mánaða tímabil, frá janúar til og með desember 2021. Línan er með þrjú tímabil: upphaflegt tímabil, annað tímabil (janúar til og með desember 2022) og þriðja tímabil (janúar til og með desember 2023). Eftir að reikningurinn hefur verið stofnaður fyrir allar greiðsluupplýsingalínur frá fyrstu 12 mánuðum ársins 2021 verður hægt að stofna færslu í færslubók fyrir óreikningsfærðar tekjur fyrir annað tímabilið.
>
> Fyrir frestunaratriði sem nota eiginleika óreikningsfærðra tekna er unnið úr greiðslulínu og afsláttarlínum. Fyrir þessar vörur eru stofnuð færsla í tekjubók og frestunaráætlun fyrir greiðslulínu og afsláttarlínu er búin til.
>
> Færslubókarfærslurnar sem eru stofnaðar fyrir vörur sem ekki er frestað og frestaðar vörur bóka kreditfærslu á mismunandi tekjulykla.
