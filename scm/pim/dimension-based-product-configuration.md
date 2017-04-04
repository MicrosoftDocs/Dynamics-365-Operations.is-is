---
title: "Afurðarafbrigði byggt á vídd"
description: "Afurðarafbrigði sem byggist á víddum stendur fyrir einfalda lausn til að búa til mörg afbrigði vöru frá einum afurðarsniðmáti og uppskrift þess."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7fbf69dc217a2f61ec3aeda952ff221491e9385a
ms.lasthandoff: 03/31/2017


---

# <a name="dimension-based-product-configuration"></a>Afurðarafbrigði byggt á vídd

Afurðarafbrigði sem byggist á víddum stendur fyrir einfalda lausn til að búa til mörg afbrigði vöru frá einum afurðarsniðmáti og uppskrift þess.

Skilgreiningu afurðar sem byggja á víddum er einn af þremur afbrigðistækni innbyggðu afurðar. Hinar tvær tækninálganirnar eru forskilgreind afbrigði og skorðuskilgreining. Allar þrjár tækninálganirnar nota afurðarsniðmát sem upphafspunkt og leyfa notanda að stofna margar afurðarafbrigða fyrir eitt afurðarsniðmát .

## <a name="key-concepts"></a>Lykilhugtök
Skilgreiningu afurðarafbrigðis sem byggja á víddum byggist á eftirfarandi grundvallarhugtök:

-   Afurðarsniðmát
-   Skilgreind Afurðarvídd
-   Afbrigðaflokkar
-   Uppskrift
-   Afbrigðaleið
-   Afbrigðareglur

### <a name="product-masters"></a>Afurðarsniðmát

Afurðarsniðmát er upphafspunkt fyrir öll afurðarafbrigðisferli. Fyrir afurðarafbrigði sem byggja á víddum þarf afurðarsniðmát með þessu tiltekna afbrigðistækni og afurðavíddaflokk sem inniheldur víddaskilgreiningu afurðar.

### <a name="configuration-product-dimension"></a>Skilgreind Afurðarvídd

Víddaskilgreining afurðar er notuð til að auðkenna afurðarafbrigði fyrir afurðarsniðmát með skilgreiningartækninni sem byggist á víddum. víddargildi Skilgreiningar er færð inn af notandanum ætti að hjálpa við að auðkenna einstaka afurðarafbrigði.

### <a name="configuration-groups"></a>Afbrigðaflokkar

Afbrigðaflokkar eru skilgreindar í miðlægri geymslu og er hægt að nota fyrir allar afbrigðalíkönum afurða sem byggja á víddum. Afbrigðaflokkar eru tengdir einstaka uppskriftalínur og halda saman flokki af línum sem gagnkvæmt útiloka hverja aðra. Þetta þýðir að hægt er að velja aðeins eina lína í flokki fyrir eitt afurðarafbrigði.

### <a name="bill-of-materials-bom"></a>Uppskrift

Uppskriftin standa fyrir einingar fyrir afurðarafbrigði sem byggja á víddum. Það verður að innihalda allar mismunandi afurðir sem hægt er að nota í hvaða afurðarafbrigði sem er. Hverja línu í Uppskriftinni getur vísað til afbrigðaflokkur. Ef línu ekki vísa afbrigðaflokkur er hún höfð með í öll afurðarafbrigði.

### <a name="configuration-route"></a>Afbrigðaleið

Skilgreiningarleiðinni ákvarðar röð skilgreiningarflokka, eins og þær birtast notandanum við ferli afurðarafbrigðis.

### <a name="configuration-rules"></a>Afbrigðareglur

Skilgreiningarreglur tákna mekanisma til að tryggja að afurð sem er í einumafbrigðisflokk í Uppskrift framkalli annað hvort meðtalningu eða útilokun fyrir vöru í mismunandi afbrigðisflokkum í sömu uppskrift.

## <a name="product-modeling-process"></a>Ferli vörulíkanagerðar
Eðlileg röðun til að byggja vörulíkan fyrir afurð sem byggist á víddum byrjar á skilgreiningu viðeigandi afbrigðisflokka. Það er mikilvægt að tryggja að allar afurðir sem verður notaður í Uppskriftinni hafa verið losaðar í fyrirtækið sem vörulíkan er búið til fyrir. Með þessum grunneiningar í stað, notandi hægt að stofna Uppskrift og úthluta afbrigðisflokka allar viðeigandi uppskriftalínur. Þegar Uppskrift er lokið er hægt að skilgreina skilgreiningu leið panta skilgreiningaflokka í viðeigandi númeraröð fyrir. \[myndatexta = "viðhengi\_282671" jafna = "alignnone" breidd = "1187"\][![byggja á víddum afurð líkansgerðarferli](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) byggja á víddum afurð líkansgerðarferli\[/myndatexti\] tilteknar vörur úr mismunandi skilgreiningarflokkum sem þarf eða má ekki nota saman Eru hægt að stofna afbrigðareglur tryggja verður þessum afurðavensl. Eftir að uppskrift hefur verið tengd við afurðarsniðmát sem byggist á víddum í gegnum uppskriftarútgáfu og bæði hafa verið samþykktar og virkjaðar, er hægt að stofna afurðarafbrigði og færa inn heiti fyrir hvert afbrigði. Hægt er að skilgreina afbrigði áður en neinar færslur eru mynduðar eða það er gert þegar þörf fyrir ákveðið afbrigði á sér stað.

### <a name="suggested-use"></a>Notkun sem mælt er með

Afbrigðistækni sem byggist á víddum hentar best fyrir vörur með takmörkuðum breytileika og samsetningu staðlaðra stærða afurðarvídda, lit, stíl, og afbrigði hentar ekki til að auðkenna tiltekinn afurðarafbrigði. Dæmi gæti verið reiðhjól með stellhæð, hjólastærð, og mismunandi gíra.


