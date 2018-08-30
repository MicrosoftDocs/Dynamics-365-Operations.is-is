---
title: "Gagnagjafar þvert á fyrirtæki í rafrænni skýrslugerð (ER)"
description: "Þetta efnisatriði útskýrir hvernig hægt er að nota gagnagjafa þvert á fyrirtæki í rafrænni skýrslugerð."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 201d0f1e3fddd662748008c7304d67ef6003ef02
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Gagnagjafar þvert á fyrirtæki í rafrænni skýrslugerð (ER)

[!include[banner](../includes/banner.md)]

Hægt er að hanna snið rafrænnar skýrslugerðar til að búa til skjöl á útleið í ýmsum sniðum. Þegar skjal er búið til kallar snið rafrænnar skýrslugerðar á gagnagjafa sem voru skilgreindir í samsvarandi líkanavörpun rafrænnar skýrslugerðar. Til að stilla aðgang að forritatöflum til að sækja skrá er hægt að nota gagnagjafa rafrænnar skýrslugerðar af gerðinni **Töflufærslur**. Þegar taflan sem fengin er aðgangur að er samnýtt tafla (þ.e. tafla þar sem gögn eru vistuð án fyrirtækiskennis) skilar þessi gagnagjafi öllum færslum. Þegar taflan sem fengin er aðgangur að er fyrirtækjaháð tafla (þ.e. tafla þar sem gögn eru vistuð fyrir hvert fyrirtæki) skilar þessi gagnagjafi aðeins færslum sem hafa verið vistaðar fyrir núverandi fyrirtæki (þ.e. samhengi fyrirtækisins sem snið rafrænnar skýrslugerðar keyrir undir).

Sérhver gagnagjafi af gerðinni **Töflufærslur** í líkanavörpun getur nú verið merkt sem gagnagjafi þvert á fyrirtæki. Þess vegna er hægt að nota gagnagjafa af gerðinni **Töflufærslur** til að fá aðgang að gögnum þvert á fyrirtæki í forritartöflum. 

Ef gagnagjafi er merktur sem þvert á fyrirtæki mun eftirfarandi hegðun gerast:

- Fyrir gagnagjafa sem vísar til einhverrar samnýttrar töflu nema CompanyInfo skilar gagnagjafinn öllum færslum sem eru til staðar í töflunni sem vísað er í. 
- Fyrir gagnagjafa sem vísar til CompanyInfo-töflunnar, jafnvel þótt CompanyInfo sé samnýtt tafla, skilar gagnagjafinn færslunum sem innihalda auðkenni fyrirtækis frá skilgreindu umfangi.
- Fyrir sérhverja töflu sem er háð fyrirtæki skilar gagnagjafinn færslum töflunnar sem vísað er í sem innihalda auðkenni fyrirtækisins frá skilgreindu umfangi.

Í svarglugga kerfisfyrirspurnar þegar kveikt er á valkostinum **Biðja um fyrirspurn** fyrir hvaða gagnagjafa sem er merktur sem þvert á fyrirtæki, er hægt að velja handvirkt eitt eða fleiri fyrirtæki til að hafa með í flipanum **Fyrirtækjasvið**.

> [!IMPORTANT]
> Eins og aðrar síur er fyrirtækissía notuð sem síðast notaða gildið fyrir fyrirspurnir þegar snið rafrænnar skýrslugerðar er keyrt. Sían breytist ekki sjálfkrafa ef gildinu þvert á fyrirtæki er breytt fyrir gagnagjafa. Til að nota annað gildi þvert á fyrirtæki fyrir annan gagnagjafa skal eyða samsvarandi notendasértæku vali.

Fyrir hvern gagnagjafa sem merktur er sem þvert á fyrirtæki er hægt að velja færslurnar sem þú vilt með því að nota virknirnar **SÍA** og **HVAR** í segðum rafrænnar skýrslugerðar. Einnig er hægt að nota reitinn **dataAreaID** sem auðkenni fyrirtækis. Reiturinn **dataAreaID** er, eins og er, takmarkaður við eftirfarandi gerðir af skilyrðum þegar virknin **SÍA** er notuð: 

- Aðeins skilyrði sem hafa einn **dataAreaID** reitarsamanburð eru studd.
- Aðeins samanburður sem hefur segðir sem eru ekki háðar vörum færslulista er heimilaður.

Þess vegna er eftirfarandi segð gild.

    FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
    While shown below expressions will not pass the validation:
    FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
    FILTER (MyTable, 
        OR(
            MyTable.dataAreaID = $StringUserInputParameter1,
            MyTable.dataAreaID = $StringUserInputParameter2
        )
    )

Umfangið inniheldur að sjálfgefnu öll fyrirtæki núverandi forrits. Hins vegar er hægt að takmarka það. Til að takmarka umfang aðgangs að gögnum þvert yfir fyrirtæki fyrir eitt snið rafrænnar skýrslugerðar skal úthluta tilteknu stigveldi fyrirtækis á sniðið. Þegar stigveldi er skilgreint fyrir snið rafrænnar skýrslugerðar er eingöngu færslum fyrir lögaðila sem eru kynntir í úthlutuðu stigveldi skilað, jafnvel þótt sniðið kalli á gagnagjafa þvert yfir fyrirtæki. Þegar tilvísun í stigveldi sem ekki er lengur til er skilgreint fyrir snið rafrænnar skýrslugerðar er sjálfgefið umfang notað og sniðið kallar á gagnagjafa þvert yfir fyrirtæki. Í þessum kringumstæðum er færslum fyrir öll umsóknarfyrirtæki skilað. 

Athugaðu að þegar kveikt er á valkostinum **Nota drög** fyrir úthlutun á einu fyrirtækisstigveldi fyrir snið rafrænnar skýrslugerðar verða lögaðilar frá drögunum af þessu stigveldi notaðir til að bera kennsl á umfang gagnagjafa þvert á fyrirtæki. Ef útgáfudrög eru ekki til verða lögaðilar frá síðustu birtu útgáfu af þessu fyrirtækisstigveldi notaðir fyrir þetta.

Athugaðu að þegar slökkt er á valkostinum **Nota drög** fyrir úthlutun á einu fyrirtækisstigveldi fyrir snið rafrænnar skýrslugerðar verða lögaðilar frá síðustu birtu útgáfu af þessu fyrirtækisstigveldi notaðir til að bera kennsl á umfang gagnagjafa þvert á fyrirtæki. Skilvirkni dagsetningar fyrir fyrirtækisstigveldi er enn ekki stutt í ramma rafrænnar skýrslugerðar.

Hægt er að úthluta stigveldinu á snið á tiltekinni síðu sem hægt er að nálgast frá vinnusvæði rafrænnar skýrslugerðar eða með því að nota valmyndaratriðið **Fyrirtækisstjórnun -> Rafræn skýrslugerð -> Sía lögaðila fyrir snið**. Til að fá aðgang að síðunni verður að veita notandanum réttindin **Vinna með síur lögaðila** (ERMaintainFormatMappingLegalEntityFilters). Takmörkun á umfangi lögaðila sem eru byggðir á stigveldi fyrir sniðið er notað til viðbótar við takmörkunina sem notandinn getur handvirkt tilgreint í svarglugga kerfisfyrirspurnar. Skörun þessara takmarkana er notuð þegar sniðið er keyrt.

Til að læra meira um þennan eiginleika skal spila verkefnaleiðbeiningarnar, **Aðgangsfærslur rafrænnar skýrslugerðar fyrir töflum háðum fyrirtæki í stillingunni þvert yfir fyrirtæki**, sem er hluti af viðskiptaferlinu 7.5.4.3 Acquire/Þróun upplýsingatækniþjónustu/lausnarhlutar (10677) og hægt er að sækja á [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Þessar verkefnaleiðbeiningar fylgja þér í gegnum skilgreiningarferli fyrir líkanavörpun rafrænnar skýrslugerðar og snið rafrænnar skýrslugerðar til að fá aðgang að forritatöflum í stillingunni þvert á fyrirtæki.

Sæka eftirfarandi skrár til að ljúka verkefnaleiðbeiningunni:

- [Skilgreining á líkani rafrænnar skýrslugerðar - CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [Skilgreining á líkani rafrænnar skýrslugerðar - CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

