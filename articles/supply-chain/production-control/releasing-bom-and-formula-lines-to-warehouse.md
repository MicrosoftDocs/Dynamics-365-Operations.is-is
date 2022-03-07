---
title: Losa uppskriftar- og formúlulínur í vöruhúsið
description: Þetta efnisatriði lýsir ferlinu fyrir losun hráefnis fyrir uppskriftar- og formúlulína í vöruhúsið.
author: johanhoffmann
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm, ProdParmReleaseToWarehouse, WHSReleaseToWarehouseProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: c9956290ce8f90f04bc144d710ad35b5a0243e3898a8f3e75692b1a9da506149
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731224"
---
# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Losa uppskriftar- og formúlulínur í vöruhúsið

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir ferlinu fyrir losun hráefnis fyrir uppskriftar- (BOM) og formúlulína í vöruhúsið. Þegar þú losar uppskriftar- eða formúlulínu í vöruhúsið ákvarðar kerfið fyrst hvort efni sé þegar í boði á staðsetningu framleiðsluinntaks í vinnusalnum þar sem efnið verður notað fyrir framleiðsluferlið.

- Ef efnið er í boði á staðsetningu framleiðsluinntaks, er það tiltekið frá þeirri staðsetningu strax eftir að merki er gefið fyrir losun efnis í vöruhúsið.
- Ef efnið er ekki tiltækt á staðsetningu framleiðsluinntaks, gefur losun efnis til kynna að efni skuli flutt frá staðsetningu í vöruhúsinu til staðsetningu framleiðsluinntaks. Efnið er flutt með vinnu vöruhúss fyrir tiltekt hráefnis. Þ.a.l. þarf vinnsla vöruhúss fyrir tiltekt hráefnis að vera grunnstillt. Frekari upplýsingar, sjá [Yfirlit áfyllingar](../warehousing/replenishment.md) og [Stýra vöruhúsavinnu með vinnusniðmát og staðsetningarleiðbeiningar](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Aðferðir til að losa uppskriftarlínur og formúlulínur

Þú getur grunnstillt losun uppskriftar- og formúlu línur þannig að það gerist sem hluti af losun framleiðslupöntunar eða runupöntunar. Að öðrum kosti getur losunin verið stjórnað af runuvinnslu eða framkvæmd sem handvirk samskipti.

Aðferðin sem notuð er til að losunar uppskriftar- og formúlulínur er stjórnað af **Losun framleiðslulínu** færibreytunni. Þú getur fundið þessa færibreytu í **Framleiðslustýring** \> **Uppsetning** \> **Framleiðslufæribreytur**.

- **Losa uppskriftar- og formúlu línur sem hluta af framleiðslu- eða runupöntunarlosun** - Í þessari aðferð eru BOM og formúlu línur fyrir framleiðslu eða runupöntun losaðar sem hluti af því ferli að losa pöntunina. Venjulega, þegar framleiðsla eða runupöntun er losað, eru framleiðsluverk losaðar til starfsmanna vinnusalarins og framleiðsluskjöl eru prentaðar. Á meðan þessu ferli stendur er staða pöntunar einnig breytt í **Losuð**.
- **Losaðu BOM og formúlu línur í gegnum runuvinnslu eða sem handvirkt samskipti** - Í þessari aðferð er hægt að losa BOM og formúlu línur aðeins með **Sjálfvirk losun BOM og formúlu línum** runuvinnslu eða sem handvirk samskipti. Til að losa handvirkt BOM og formúlulínur, á listasíðu framleiðslupantana eða upplýsingasíðu um framleiðslupantana, í aðgerðarglugganum, veldu **Losa í vörugeymslu**.

Til að fá snögga sýnikennslu um losun uppskrifta og formúlulína til framleiðslu með runuvinnslu skal horfa á þetta stutta YouTube myndband: [Losa framleiðslutiltekt til vöruhúss í runu](https://www.youtube.com/watch?v=8urAJn50dQ8).

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>Losa uppskriftarlínur og formúlulínur með því að nota runuvinnslu

**Sjálfvirk losun BOM og formúlulínur** runuvinnsla fer í gegnum valin BOM og formúlu línur sem hafa eftirstandandi magn til að sleppa. Vinnslan tekur aðeins til greina pantanir með stöðuna **Losað**, **Byrjað** eða **Tilkynnt sem lokið**. Ef uppskriftar- eða formúlulína hefur eftirstandandi magn til að losa, þá losar vinnslan allt að magni sem hægt er að dekka með því magni sem þegar hefur verið efnislega frátekið og magnið sem er efnislega tiltækt.

### <a name="example-of-a-batch-job-release"></a>Dæmi um losun runuvinnslu

| Aðstæður | Eftirstandandi magn til losunar | Efnislega frátekið magn | Efnislega tiltækt magn | Magn losað af runuvinnslunni |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Uppsetning runuvinnslu

Í fyrirspurninni um **Sjálfvirkan losun uppskriftar- og formúlulína** runuvinnslu, getur þú sett upp síuviðmið til að tilgreina hversu marga daga fram í tímann vinnslan ætti að leita að línum sem hafa ólosað magn. Í fyrirspurninni um vinnsluna, á **Dagsetning hráefnis** reitnum, notaðu **(LessThanDate())** virknina sem síuskilyrði.

Eftirfarandi mynd sýnir framleiðslupöntun sem hefur tvær vinnslur, 10 og 20, sem dekka samsetninguna og pökkun fyrir framleiðslupöntunina. Hver vinnsla er sett upp til að nota magn efnis. Í þessari mynd eru tímamörk losunar sem táknað er með græna örina undir tímalínunni jafngildir fjölda daga sem hefur verið tilgreint í **(LessThanDate ())** viðmiðuninni. Til dæmis, **(LessThanDate (2))** gefur til kynna að vinnslan ætti að leita að ólosuðu magni aðeins innan tímamarka upp á tvo daga.

![Dæmi um framleiðslupöntun sem hefur tvær runuvinnslur.](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Losun efnis fyrir hverja aðgerðarnúmer eða í hlutfalli við magn fullunninnar vöru

Ef þú sleppir efni með því að nota færibreytustillingu **Á losun framleiðslupöntunar**, þegar þú framkvæmir handvirkt losun, hefur þú tvo valkosti til að stjórna losun efnisins:

- Losaðu efni eftir aðgerðarnúmeri.
- Losaðu efni í hlutfalli við magn fullunnar vöru.

### <a name="release-material-per-operation-number"></a>Losaðu efni eftir aðgerðarnúmeri

Til að stjórna þeim aðgerðum sem efnið ætti að vera losað til, notaðu síðuna **Losa í vöruhús**.

- Veldu **Framleiðslustýring** \> **Framleiðslupantanir** \> **Allar framleiðslupantanir**, veldu framleiðslupöntun og síðan á **Vöruhús** flipanum velurðu **Losa í vöruhús**. Síðan skal nota **Frá aðg. nr.** og **Til aðg. nr.** reitina til að tilgreina bil aðgerðanúmera.

Eftirfarandi mynd sýnir framleiðslupantanir sem hefur tvær aðgerðir, 10 og 20. Í þessu dæmi, ef þú takmarkar losun við aðgerð 10, verður aðeins efni M9203 losað.

![Dæmi um losun efnis fyrir hvert aðgerðarnúmer.](media/two-operations.PNG)

Til að fá snögga sýnikennslu um losun hraéfna í hlutfalli við magn fullunninna vara skal horfa á þetta stutta YouTube-myndband um [endurbætur á losunarferli framleiðslupöntunar](https://www.youtube.com/watch?v=Rm3ojAz6Zu0).

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Losa efni í hlutfalli við magn fullunninnar vöru

Þú getur losað hráefni fyrir hluta magns fullunninnar vöru eða í tiltekinni einingu.

- Til að losa hráefni fyrir hluta magns fullunnar vöru skaltu velja **Framleiðslustýring** \> **Framleiðslupantanir** \> **Allar framleiðslupantanir**, veldu framleiðslupöntun og síðan á **Vöruhús** flipanum velurðu **Losa í vöruhús**. Í reitinn **Magn** skal síðan slá inn magn.

    Til dæmis er stofnuð og áætluð framleiðslupöntun fyrir 1.000 stykki (pcs.). Yfirmaður vinnusalar áætlar framleiðslu 100 stk. fyrir næsta vakt og vill losa efni aðeins fyrir þá vakt. Í þessu tilfelli getur umsjónarmaðurinn notað **Magn** reitinn til að losa efni fyrir 100 stk. sem eru áætlaðir fyrir næstu vakt.

- Til að losa hráefni í tiltekinni einingu velurðu **Framleiðslustýring** \> **Framleiðslupantanir** \> **Allar framleiðslupantanir**, veldu framleiðslupöntun og síðan á **Vöruhús** flipanum velurðu **Losa í vöruhús**. Notaðu síðan **Eining** reitinn til að velja eininguna fyrir fullunnu vöruna til að losa efni í.

    Einingarnar sem eru tiltækar eru skilgreindar í kenni einingaröðunarflokks fullunnu vörunnar.

    Til dæmis hefur fullunnin vara eftirfarandi einingaumreikning á milli punda (lbs.) og bretti (PL): 1 PL = 100 pund. Til að stofna framleiðslupöntun fyrir 10.000 pund. af fullunnu vörunni, getur þú losað hráefni fyrir fjölda bretti sem þú áætlar að framleiða. Veldu **PL** sem eininguna og veldu síðan samsvarandi númer í **Magn** reitnum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]