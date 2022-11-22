---
title: Yfirlit yfir víddarbyggðar skilgreiningar fyrir afurð
description: Afurðarafbrigði sem byggist á víddum stendur fyrir einfalda lausn til að búa til mörg afbrigði vöru frá einum afurðarsniðmáti og uppskrift þess.
author: t-benebo
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba11a561f320a7f4e787e4fe3f4e6f4fb88bbfb
ms.sourcegitcommit: ca73177dedf40df16860eaf88b1c701c61992028
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/10/2022
ms.locfileid: "9754111"
---
# <a name="dimension-based-product-configuration-overview"></a>Yfirlit yfir víddarbyggðar skilgreiningar fyrir afurð

[!include [banner](../includes/banner.md)]

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
Eðlileg röðun til að byggja vörulíkan fyrir afurð sem byggist á víddum byrjar á skilgreiningu viðeigandi afbrigðisflokka. Það er mikilvægt að tryggja að allar afurðir sem verður notaður í Uppskriftinni hafa verið losaðar í fyrirtækið sem vörulíkan er búið til fyrir. Með þessum einingum á sínum stað, getur notandi stofna Uppskrift og úthluta afbrigðisflokka á allar viðeigandi uppskriftalínur. Þegar Uppskrift er lokið er hægt að skilgreina afbrigðisleið skilgreinda fyrir röðun á afbrigðisflokkum í viðeigandi númeraröð. [![Víddarmiðað vörulíkanaferli.](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Ef það er vitað um afurðir úr mismunandi afbrigðisflokkum sem annað hvort verður eða má ekki nota saman, er hægt að stofna afbrigðareglur sem munu framfylgja þessum afurðavenslum. Eftir að uppskrift hefur verið tengd við afurðarsniðmát sem byggist á víddum í gegnum uppskriftarútgáfu og bæði hafa verið samþykktar og virkjaðar, er hægt að stofna afurðarafbrigði og færa inn heiti fyrir hvert afbrigði. Hægt er að skilgreina afbrigði áður en neinar færslur eru mynduðar eða það er gert þegar þörf fyrir ákveðið afbrigði á sér stað.

### <a name="suggested-use"></a>Notkun sem mælt er með

Afbrigðistækni sem byggist á víddum hentar best fyrir vörur með takmörkuðum breytileika og samsetningu staðlaðra stærða afurðarvídda, lit, stíl, og afbrigði hentar ekki til að auðkenna tiltekinn afurðarafbrigði. Dæmi gæti verið reiðhjól með stellhæð, hjólastærð, og mismunandi gíra.

### <a name="next-step"></a><a name="sequence"></a>Næsta skref

Eftirfarandi átta verkefnaleiðbeiningar eru taldar upp í þeirri röð sem ætti að ljúka þeim. 

1.  [Búa til afurðarsniðmát sem byggir á víddum](tasks/create-dimension-based-product-master.md)
2.  [Gefa út afurðarsniðmát sem byggir á víddum](tasks/release-dimension-based-product-master.md)
3.  [Ljúka grunnuppsetningu útgefins afurðarsniðmáts](tasks/complete-basic-setup-released-product-master.md)
4.  [Skilgreina afbrigðaflokka](tasks/define-configuration-groups.md)
5.  [Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Skilgreina afbrigðaleiðir](tasks/define-configuration-route.md)
7.  [Stofna skilgreiningareglur](tasks/create-configuration-rules.md)
8.  [Stofna skilgreiningar sem byggja á víddum](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]