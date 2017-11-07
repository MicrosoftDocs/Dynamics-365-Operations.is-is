---
title: "Afurðarafbrigði byggt á vídd"
description: "Afurðarafbrigði sem byggist á víddum stendur fyrir einfalda lausn til að búa til mörg afbrigði vöru frá einum afurðarsniðmáti og uppskrift þess."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e2ce0e95a5e1230df970b5d5249fdb248113cf54
ms.openlocfilehash: b6895726af6028035830893fdbb01a4a407d7076
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="dimension-based-product-configuration"></a>Afurðarafbrigði byggt á vídd

[!include[banner](../includes/banner.md)]


Afurðarafbrigði sem byggist á víddum stendur fyrir einfalda lausn til að búa til mörg afbrigði vöru frá einum afurðarsniðmáti og uppskrift þess.

Skilgreiningu afurðarafbrigðis sem byggja á víddum er einn af þremur innbyggðu afbrigðistækni afurðar. Hinar tvær tækninálganirnar eru forskilgreind afbrigði og skorðuskilgreining. Allar þrjár tækninálganirnar nota afurðarsniðmát sem upphafspunkt og leyfa notanda að stofna margar afurðarafbrigða fyrir eitt afurðarsniðmát .

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
Eðlileg röðun til að byggja vörulíkan fyrir afurð sem byggist á víddum byrjar á skilgreiningu viðeigandi afbrigðisflokka. Það er mikilvægt að tryggja að allar afurðir sem verður notaður í Uppskriftinni hafa verið losaðar í fyrirtækið sem vörulíkan er búið til fyrir. Með þessum einingum á sínum stað, getur notandi stofna Uppskrift og úthluta afbrigðisflokka á allar viðeigandi uppskriftalínur. Þegar Uppskrift er lokið er hægt að skilgreina afbrigðisleið skilgreinda fyrir röðun á afbrigðisflokkum í viðeigandi númeraröð. [![Víddarmiðað vörulíkanaferli](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Ef það er vitað um afurðir úr mismunandi afbrigðisflokkum sem annað hvort verður eða má ekki nota saman, er hægt að stofna afbrigðareglur sem munu framfylgja þessum afurðavenslum. Eftir að uppskrift hefur verið tengd við afurðarsniðmát sem byggist á víddum í gegnum uppskriftarútgáfu og bæði hafa verið samþykktar og virkjaðar, er hægt að stofna afurðarafbrigði og færa inn heiti fyrir hvert afbrigði. Hægt er að skilgreina afbrigði áður en neinar færslur eru mynduðar eða það er gert þegar þörf fyrir ákveðið afbrigði á sér stað.

### <a name="suggested-use"></a>Notkun sem mælt er með

Afbrigðistækni sem byggist á víddum hentar best fyrir vörur með takmörkuðum breytileika og samsetningu staðlaðra stærða afurðarvídda, lit, stíl, og afbrigði hentar ekki til að auðkenna tiltekinn afurðarafbrigði. Dæmi gæti verið reiðhjól með stellhæð, hjólastærð, og mismunandi gíra.

### <a name="next-step"></a>Næsta skref 

Eftirfarandi átta verkefnaleiðbeiningar eru taldar upp í þeirri röð sem ætti að ljúka þeim. 

1.  [Búa til afurðarsniðmát sem byggir á víddum (verkleiðbeiningar)](tasks/create-dimension-based-product-master.md)
2.  [Losa afurðarsniðmát sem byggir á víddum (verkleiðbeiningar)](tasks/release-dimension-based-product-master.md)
3.  [Ljúka grunnuppsetningu útgefins afurðarsniðmáts (verkleiðbeiningar)](tasks/complete-basic-setup-released-product-master.md)
4.  [Skilgreina skilgreiningarflokka (verkleiðbeiningar)](tasks/define-configuration-groups.md)
5.  [Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum (verkleiðbeiningar)](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Skilgreina skilgreiningarleiðir (verkleiðbeiningar)](tasks/define-configuration-route.md)
7.  [Stofna skilgreiningarreglur (verkleiðbeiningar)](tasks/create-configuration-rules.md)
8.  [Stofna skilgreiningar sem byggja á víddum (verkleiðbeiningar)](tasks/create-dimension-based-configurations.md)


