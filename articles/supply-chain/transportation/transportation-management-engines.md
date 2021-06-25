---
title: Flutningsstjórnunarvélar
description: Flutningsstjórnunarvélar skilgreina rökin sem eru notuð til að búa til og vinna flutningstaxta í Flutningsstjórnun.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61c745802edc419cb2ae94df6bc293f839cd8a0a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188850"
---
# <a name="transportation-management-engines"></a>Flutningsstjórnunarvélar

[!include [banner](../includes/banner.md)]

Flutningsstjórnunarvélar skilgreina rökin sem eru notuð til að búa til og vinna flutningstaxta í Flutningsstjórnun. 

Vél flutningsstjórnunar reiknar verk, eins og flutningsverðskrá flutningsaðila. Vélakerfið gerir kleift að breyta stefnu útreikninga á keyrslutíma, samkvæmt á gögnum í Supply Chain Management. Vél flutningsstjórnunar svipar til tengiforrits sem tengjast tilteknum samningi við flutningsaðila.

## <a name="what-engines-are-available"></a>Hvaða véla eru tiltækar?
Eftirfarandi tafla sýnir flutningsstjórnunarvélar sem eru tiltækar.

| Flutningsstjórnunarvél | Lýsing                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Taxtavél**                  | Reiknar út taxta.                                                                                                                                                                                                                                                                                                           |
| **Almenn vél**               | Einföld aukakerfi sem eru notuð af öðrum kerfum sem þurfa ekki gögn úr Supply Chain Management, t.d. skiptingarvél. Skiptingarvélar eru notaðar til að draga úr endanlegum kostnaði á flutningi i tilgreindar pantanir og línur, byggt á stærð, svo sem magni og þyngd. |
| **Akstursvél**               | Reiknar út flutningsfjarlægð.                                                                                                                                                                                                                                                                                     |
| **Flutningstímavél**          | Reiknar út tímann sem nauðsynlegur er til ferðir frá upphafi til lok áfangastað.                                                                                                                                                                                                                                       |
| **Svæðisvél**                  | Reiknar út svæði byggt á gildandi aðseturs og reiknar út fjölda staði sem krossa verður við fyrir ferðir frá aðsetur A til aðsetur B.                                                                                                                                                                    |
| **Gerð farmbréfs**            | Staðlar farmreikning og línur farmbréfs og er notað fyrir sjálfvirka samsvörun farmbréfs.                                                                                                                                                                                                                |


## <a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Hvað véla verður að vera skilgreind til að meta sendingu?

Til að meta sendingu með því að nota tiltekna flutningsaðila, þarf að skilgreina margar flutningsstjórnunarvélar. **Taxtavél** er nauðsynleg, en aðrar flutningsstjórnunarvélar kunna að vera nauðsynlegar til að styðja við **Taxtavél**. Til dæmis er hægt að nota **taxtavélina** til að sækja gögn úr **akstursvél** til að reikna út taxta á grundvelli vegalengdar milli uppruna- og áfangastaðar.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Hvað er krafist að frumstilla á vél stjórnun flutningsstjórnunar
Vél flutningsstjórnunar krefst þess að setja upp frumstillingargögn til þess að aðgerð virki á ákveðinn hátt. Uppsetning getur innihaldið eftirfarandi gögnum:
-   Tilvísanir í aðrar flutningsstjórnunarvélar. Nánari upplýsingar eru í dæmi afbrigði í þessum hluta.
-   Tilvísun í .NET tegundir sem eru notaðar af flutningsstjórnunarvélar.
-   Einföld grunnstillingargögn

Í flestum tilvikum getur þú smellt á hnappinn **Færibreytur** í uppsetningarskjámyndum vélar flutningsstjórnunar til að skilgreina frumstillingargögn. **Dæmi um uppsetningu á taxtavél sem vísar til kílómetravélina** Eftirfarandi dæmi sýnir uppsetningu sem krafist er fyrir taxtavél sem byggir á .NET vélargerðin Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine og vísar í akstursvél.

|          Færibreyta           |                                                                                  Lýsing                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>RateBaseAssigner</em>   | .NET-gerð sem túlkar úthlutunargögn vaxtastigs fyrir tiltekið skema. Málskipan færibreytugildis samanstendur af tveimur hlutum sem eru afmörkuð með lóðréttu striki ( |
|  <em>MileageEngineCode</em>  |                       Kílómetravélakóði sem auðkennir skráningu kílómetravélar í gagnagrunninum.                        |
| <em>Kostnaðarskiptingarvél</em> |                        Almennur vélakóða sem auðkennir kostnaðarskiptingarvél í gagnagrunninum.                        |

## <a name="how-is-metadata-used-in-transportation-management-engines"></a>Hvernig er lýsigögnum notuð í flutningsstjórnunarvélar?

Flutningsstjórnunarvélar sem reiða sig á gögn sem eru skilgreind í Supply Chain Management geta notað mismunandi gagnaskemu. Flutningur stjórnkerfi gerir mismunandi flutningsstjórnunarvélar til að nota sama almennan efnislegt töflurnar. Til að tryggja að túlkun keyrslutíma á vélagögnum sé rétt er hægt að skilgreina lýsigögn fyrir gagnagrunnstöflurnar. Þetta dregur úr kostnaður við að byggja nýju flutningsstjórnunar stjórnun vélar þar sem viðbótar töflu og í skjámyndarskipulags er ekki krafist í Operations.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Hægt er að nota það sem gögn afurðaleitar í útreikninga?
Gögnum sem eru notuð við útreikning taxta í er stýrt af afbrigði lýsigagna. Til dæmis, ef óskað er að leita að taxta sem póstnúmer á grundvelli setja verður upp lýsigögn samkvæmt uppsláttargerð fyrir póstnúmer.

## <a name="do-all-engine-configurations-require-metadata"></a>Krefjast allar vélaskilgreiningar lýsigagna?
Nei, flutningsstjórnunarvélar sem eru notaðar til að sækja gögn sem krafist er fyrir taxtaútreikning frá utanaðkomandi kerfum þurfa ekki lýsigögn. Hægt að endurheimta gögnin taxta fyrir þessar véla úr ytri flutningsstöðu flutningsaðila kerfum, vanalega í gegnum vefþjónustu. Til dæmis er hægt að nota akstursvél sem sækir gögn beint úr Bing-kortum þannig að þarf ekki að lýsigögn fyrir þessa vél.

| **Ábending**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flutningsstjórnunarvélar sem eru afhentar með Supply Chain Management reiða sig á gögn sem eru sóttar úr forritinu. Vélar sem tengjast við ytri kerfi eru ekki teknar með í Operations. Hins vegar vélmiðað framlengingarlíkan gerir það mögulegt að byggja upp viðbætur með Visual Studio verkfærum. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Hvernig get ég skilgreina lýsigögn fyrir vél stjórnun flutningsstjórnunar?
Lýsigögn fyrir flutningsstjórnunarvélar eru stillt á mismunandi hátt fyrir mismunandi tegundir af vélum.

| Flutningsstjórnunarvél               | Skilgreining lýsigagna                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Taxtavél**                                | Krefst **Gerð taxtagrunns**. Gerð taxtagrunnsins inniheldur lýsigögn fyrir taxta grunngögnum og á úthlutun taxtagrunns gögn. Skipan grunngögn lýsigögn fyrir taxta ákvarðast af gerð taxtavél. Skipulag lýsigagna úthlutun taxtagrunns taxta ákvarðast af gerð taxta grunngögn assigner sem tengist þeirri taxtavél. Setja upp taxta grunngerð við taxtavél í skjámyndinni **Taxtavél** og á síðunni **Taxtasniðmát**. |
| **Svæðisvél**                                | Krefst lýsigögn til að setja upp beint á svæðissniðmátið.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Flutningstímavél** og **akstursvél** | Sækir lýsigögn beint úr uppsetningarskjámynd fyrir skilgreiningu akstursvélina.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Dæmi um lýsigögn fyrir taxtavél** Flutningsstjórnunarvél krefst kenni aðsetursuppruna, áfangastaðsríki og lands/svæðis og upphafs- og endastöð sendingarinnar. Með því að nota þessar þarfir lýsigögn myndu líta út eins og gögn í eftirfarandi töflu. Taflan inniheldur einnig upplýsingar um hvers konar gögn inntaks er krafist.
-   Þessar upplýsingar á að skilgreina í **Flutningsstjórnun** &gt; **Uppsetning** á síðunni **Gerð taxtagrunns**.

| Röð | Nafn                          | Gerð svæðis | Gagnagerð | Uppsláttargerð    | Áskilið |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Póstnúmer upprunalands            | Úthlutun | Strengur    | Póstnúmer    | Valið  |
| 2        | Áfangaríki             | Úthlutun | Strengur    | Ástand          |           |
| 3        | Upphafspóstnúmer áfangastaðar | Úthlutun | Strengur    | Póstnúmer    | Valið  |
| 4        | Póstnúmer áfangastaðar   | Úthlutun | Strengur    | Póstnúmer    | Valið  |
| 5        | Áfangaland           | Verkefni | Strengur    | Land/svæði |           |

### <a name="whitepaper"></a>Hvítbók

Frekari upplýsingar er að hlaða niður eftirfarandi hvítbók (skrifuð til að styðja AX2012, en gildir einnig fyrir Dynamics 365 Supply Chain Management)

- [Flutningsstjórnunarvélar](https://download.microsoft.com/download/e/0/9/e0957665-c12f-43c7-94c0-611cc49d7d61/TransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]