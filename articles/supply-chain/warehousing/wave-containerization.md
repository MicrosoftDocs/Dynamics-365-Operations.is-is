---
title: Gámun
description: Þetta efnisatriði lýsir því hvernig á að gera gámun farms sjálfvirka. Sjálfvirk gámun stofnar gáma- og tínsluvinnu fyrir sendingar þegar bylgja er afgreidd.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3546547bd064835d195a2c6ac7e4eb1d5afc9b00
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838107"
---
# <a name="containerization"></a>Gámun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að gera gámun farms sjálfvirka. Sjálfvirk gámun stofnar gáma- og tínsluvinnu fyrir sendingar þegar bylgja er afgreidd.

Til að setja upp gámun þarf að stofna eftirfarandi:

- **Gámagerð** ─ Tilgreina eðliseiginleika gáma. Gámagerðir eru notaðar til að pakka birgðavörum í tiltekinni tegund og stærð umbúða, eins og körfur eða bretti.
- **Gámaflokkar** ─ Búa til hópa af gámum þar sem gerðir eru svipaðar. Til dæmis flokkur getur gáms innihaldið gámagerðum sem hafa svipuð stærð vídda. Gámahópur tilgreinir röð gámar eru pakkaðar og fyllingarhlutfall hvers gáms.
- **Gámaröðunarsniðmát** ─ Búa til sniðmát sem skilgreina reglur fyrir gámun. Til dæmis reglur fyrir blöndun birgða og aðrar pökkunaraðferðir.
- **Bylgjusniðmát** - Setja upp eitt eða fleiri bylgjusniðmát til að búa til tiltektarvinnu fyrir gámun.

## <a name="create-wave-templates-for-containerization"></a>Búa til bylgjusniðmát fyrir gámun

Setja verður upp eitt eða fleiri bylgjusniðmát sendingar fyrir gámun. Bylgjusniðmát fela í sér skilyrði sem ákvarða eftirfarandi:

- Hvernig á að vinna bylgjur. Þetta getur verið annað hvort handvirkt eða sjálfvirkt.
- Hvernig á að stofna tiltektarvinnu. Þetta er ákvarðað af aðferðir bylgju. Bylgjusniðmátið verður að hafa með í **gámunar** aðferð.
- Hvernig á að para saman vörur eða úthlutunarlínur við bylgju.

Frekari upplýsingar er að finna í [Bylgjusniðmát](wave-templates.md).

## <a name="create-container-types"></a>Stofna gámagerðir

Gámagerðir eru notaðar til að stofna lýsingar á gámum, þar á meðal hámarksgildi fyrir stærð efnislegar víddir og þyngd afkastagetu. Þegar unnið er úr gámabylgju eru gámarnir stofnaðir á grundvelli upplýsingar um gerð gáms.

Til að setja upp gámagerð skal fylgja þessum skrefum:

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámagerð**.
1. Smelltu á **Nýtt** til að stofna nýja gámagerð.
1. Færið inn einkvæmt kenni og lýsingu á gámategund.
1. Í **Tara gáms** skal færa inn raunverulega eða áætlaða þyngd gámsins.
1. Í reitnum **Hámarksþyngd** skal slá inn hámarksþyngd gámsins.
1. Í reitunum **Hámarksrúmmál gámunar**, **Hámarkslengd gámunar**, **Hámarksbreidd gámunar** og **Hámarkshæð gámunar** skal tilgreina mælivíddir gámsins.

    > [!NOTE]
    > Gildi fyrir lengd og breidd eru interchangeable. Þetta þýðir að er hægt að snúa vörur laterally eða á fyrir x-ásnum, ef þörf krefur. Til dæmis, ef lengdin er 2 fet og breidd er 1 fet er hægt að breyta hámarkslengd á 1 fet og breidd í 2 feta. Athugaðu að þetta gildir ekki um hæðarvídd. Ekki er hægt að breyta hæðargildi til að snúa vöru þversum.

1. Veljið sérsniðin eigindagildi fyrir gáminn í reitum fyrir eigindi. Eigindir eru sérsniðin gildi sem notuð eru til að sía eða raða vörum byggt á gildi sem er annars ekki í boði. Ef ætlunin er að pakka vörum fyrir ákveðinn viðskiptavin er hægt að búa til eigind fyrir heiti viðskiptavinarins. Eigindir eru búnar til á síðunni **Eigindir gáms**.

## <a name="create-container-groups"></a>Stofna gámaflokka

Þú getur sett upp rökrétta flokka af gámagerðum. Fyrir hvern hóp er hægt að tilgreinir röð gámar eru pakkaðar og fyllingarhlutfall hvers gáms. Stærðarvíddir vörunnar skera úr um hvort hún komi til með að passa inn í gám. Geymir sem er næst er afhendingardegi stærð vídda vörunnar er notað. Ef margar gámagerðum eru í flokki, er ráðlagt að hagræða röðinni eftir stærð, þannig að stærsta gámurinn er fyrst, númer 1 í röðinni og minnsti gámurinn er síðasta.

Til að setja upp gámaflokk skal fylgja þessum skrefum:

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámahópar**.
1. Veljið **Nýtt** til að búa til gámaflokk.
1. Færið inn einkvæmt kenni og lýsingu fyrir gámahópinn.
1. Í flýtiflipanum **Upplýsingar** skal velja **Ný** til að bæta gámagerð við flokkinn.
1. Í reitnum **Gámagerð** velurðu gámagerð.
1. Veljið **Færa upp** eða **Færa niður** til að tilgreina röðina sem gámagerðirnar eru pakkaðir í.

## <a name="create-container-build-templates"></a>Stofna gámaröðunarsniðmát

Þú getur sett upp reglur fyrir gámunarferli, svo sem blöndunarreglur lagers og aðrar pökkunaraðferðir. Til dæmis er hægt að setja upp reglu svo að starfsmenn geti ekki pakkað úthlutunarlínum sem standa fyrir sölupantanir úr mismunandi viðskiptavini í sama gáms.

Til að setja upp gámaröðunarsniðmát skal fylgja þessum skrefum.

1. Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámaröðunarsniðmát**.
1. Stofnið nýtt gámaröðunarsniðmát.
1. Í reitina **Heiti gámunar** og **Raðnúmer** skal slá inn heiti gámunarsniðmáts og röðina sem er parað saman við úthlutunarlínurnar.

    > [!NOTE]
    > Kerfið mun beita fyrsta sniðmáti sem úthlutunarlína uppfyllir fyrir fyrirspurnarskilyrði. Þess vegna er að setja sniðmátið með nákvæmasta skilyrði efst á listanum. Því almennara sem skilyrðið er, þeim mun líklegra er að úthlutunarlína komi til með að uppfylla skilyrðið. Það gæti leitt til línur úthlutað á röng gámi. Ef þess gerist þörf er hægt að velja **Færa upp** eða **Færa niður** til að breyta röð sniðmátanna.

1. Í reitnum **Auðkenni gámaflokks** skal velja gámaflokkinn sem búa á til gáma út frá.
1. Í reitnum **Grunngerðir fyrirspurna** velurðu fyrirspurnargerð sem mun ákvarða hverju á að pakka og hvað á að miða síufyrirspurnina á. Eftirtaldir valkostir eru í boði:

      - **Úthlutunarlína sölu** ─ Taka saman úthlutunarlína sem eru búnar til fyrir sölupöntun..
      - **Úthlutunarlína flutnings** ─ Taka saman úthlutunarlína sem eru búin til fyrir flutningspöntun.
      - **Gámur** ─ Fylltu gám sem þegar var stofnaður í gámunarferlinu. Til dæmis er þetta notað fyrir gáma sem hægt er að raða ofan í hvern annan.

        > [!NOTE]
        > Til að nota nesting gáma, verður að gera aðferð gámun endurtekna. Frekari upplýsingar er að finna í [Bylgjusniðmát](wave-templates.md).

1. Á flýtiflipanum **Almennt**, í reitnum **Kóði bylgjuskrefs**, er slegið inn einkvæmt kenni vinnsluaðferðar bylgjuferlis sem tengir gámauppbyggingu sniðmát skrefum í bylgjusniðmáti.
1. Veljið **Leyfa skipta tiltekt** gátreitinn til að leyfa starfsmönnum að pakka vörum úr vinnupöntun í aðskildum gáma. Þetta krefst allt magnið passi í gám. Stærsta mælieiningin í úthlutunarlínunni er alltaf notuð.
1. Í reitnum **Pakka eftir einingu** skal velja mælieininguna sem notuð verður fyrir gáminn. Til dæmis er hægt að gefa upp að kassi sé gámur. Ef að pakkað er samkvæmt mælieiningu, er ekki hægt einnig að tilgreina flokk gáms því mælieiningin er gámurinn.
1. Í reitnum **Pökkunarstefna gáms** velurðu pökkunarstefnu til að nota. Eftirtaldir valkostir eru í boði:

    > [!NOTE]
    > Stjórnunarstefnan nær aðeins til úthlutunarlínur sölu og úthlutunarlína færslu.

      - **Pakka í alla opna gáma** – Kerfið metur hvort úthlutunarlína passar í hvaða gám sem var búin til í gámunarferlinu.
      - **Pakka aðeins í núverandi gám** – Kerfið metur einungis hvort úthlutunarlína passar í nýlegustu gáma sem búnir voru til.

1. Til að setja upp reglur fyrir pökkun úthlutunarlína í gámum skal velja **Blöndun rökfræðiskila**. Til dæmis er hægt að búa til reglu sem leyfir starfsmönnum að pakkar úthlutunarlínum fyrir tvær mismunandi vörur í sama gámnum. Til að skilgreina blöndunarreglu skal fylgja þessum skrefum:

    1. Á síðunni **síðunni Skipti í blöndunarrökum** skal velja **Nýtt**.
    1. Í reitnum **Tafla** velurðu töflu sem inniheldur reit til að nota sem viðmiðun fyrir blöndun rökfræðiskila.
    1. Í reitnum **Reitarval** velurðu reitinn sem á að nota sem viðmiðun fyrir blöndun rökfræðiskila.
    1. Endurtakið þessi skref þar til þú hefur bætt öllum skilyrði fyrir blöndun rökfræðiskila.

    > [!NOTE]
    > Ef notast er við blöndunarrök, er ráðlagt að raða samkvæmt sömu reitum í síuskilyrðum fyrirspurnar. Þetta mun draga úr fjölda gáma sem eru stofnaðar.
