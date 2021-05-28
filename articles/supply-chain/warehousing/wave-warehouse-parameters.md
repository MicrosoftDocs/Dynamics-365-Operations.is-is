---
title: Færibreytur vöruhúss fyrir bylgjuvinnslu
description: Þetta efnisatriði lýsir því hvernig á að setja upp færibreytur vöruhúss fyrir bylgjuvinnslu. Hægt er að nota bylgjuvinnslu til að flokka tiltekt fyrir margar vinnupantanir í einni bylgju.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b120c24ad3289f5f46119d70c8cb7124546e41b1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019179"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Færibreytur vöruhúss fyrir bylgjuvinnslu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp færibreytur vöruhúss fyrir bylgjuvinnslu. Hægt er að nota bylgjuvinnslu til að flokka tiltekt fyrir margar vinnupantanir í einni bylgju.

Til að nota bylgjuvinnslu skal tilgreina eftirfarandi á síðunni **Færibreytur vöruhúsakerfis**:

- Ef hægt er að vinna úr bylgjum með því að nota runuvinnslu.
- Ef upplýsingum er safnað í annálaskrá þegar bylgjur eru unnar.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Setja upp færibreytur vöruhúsakerfis fyrir bylgjuvinnslu

Til að setja upp færibreytur vöruhúss til bylgjuvinnslu skal fylgja þessum skrefum:

1. Farið í **Vöruhúsakerfi** \> **Uppsetning** \> **Færibreytur vöruhúsakerfis**.

1. Á flipanum **Bylgjuvinnsla** skal stilla eftirfarandi:

    - **Bylgjuúrvinnsla runuhóps** - Velja runuflokk til að nota við að vinna bylgjur með því að nota runuvinnslur. Runuflokkur tilgreinir sem runuvinnslur sem keyra á þjóninum.
    - **Vinna bylgjur í runu** - Veljið hvort það eigi að virkja að bylgjur séu sjálfkrafa unnar af runuvinnslu. Stillið þetta á *Já* til að nota hliðstæða vinnslu. Þú settir upp runuvinnsluna á síðunni **Vinna bylgjur** . (Sjá einnig athugasemdina aftast í þessum lista.)
    - **Stofna kladda fyrir framvindu bylgju** - Veljið hvort kerfið eigi að mynda kladdafærslu í hvert skipti sem úthlutun fyrir vöru og víddir hennar hefst og lýkur. Aðeins ætti að virkja þennan kladda þegar þess gerist þörf, til dæmis við fyrstu prófun eða fyrir úrræðaleit. Frekari upplýsingar er að finna í [Bylgjuúthlutun](wave-allocation-method.md).
    - **Stofna kladda fyrir framvindu bylgju** - Veljið hvort vista eigi sjálfkrafa upplýsingar bylgju í kladdaskrá þegar unnið er úr bylgjunni, þ. á m. við samhliða vinnslu á úthlutunum í biðstöðu. Yfirleitt ætti aðeins að gera þetta virkt við úrræðaleit vegna þess að það bætir við auknum kostnaði. Til að skoða kladdann skal fara í **Vöruhúsakerfi \> Bylgjur á útleið \> Sögulegur kladdi bylgjuvinnslu**. Frekari upplýsingar er að finna í [Stofnun og meðhöndlun bylgju](wave-processing.md).
    - **Stofna ferilskrá gámunar** - Veljið hvort vista eigi sjálfkrafa upplýsingar um gámun fyrir bylgju í kladdaskrá þegar unnið er úr bylgjunni. Til að skoða kladdann skal fara í **Vöruhúsakerfi \> Pökkun og gámun \> Gámunarferill**.
    - **Bíða eftir læsingu (ms)** – Sláið inn tímann í millisekúndum sem úthlutunarskref mun bíða eftir tilfangi kerfis sem er læst af öðru úthlutunarskrefi. Þegar farið er yfir þennan tíma er ekki unnið úr bylgjunni og villuboð birtist.

1. Á flýtiflipanum **Losa í vöruhús** skal stilla eftirfarandi:

    - **Villa í runuvinnslu** - Veljið hvort sýna eigi villu þegar runuvinnsla fyrir losun í vöruhús mistekst. Ef kveikt er á þessu munu mislukkaðar vinnslur enda með stöðuna *Villa*. Ef slökkt er á þessu munu mislukkaðar vinnslur enda með stöðuna *Lokið*.

> [!NOTE]
> Á bylgjusniðmátið sem er notað til að vinna úr bylgja, getur þú tilgreint stillingarnar sem gera sjálfvirka bylgjuvinnslu. Ef sett er upp áætlun fyrir runuvinnsluna ætti að samstilla tímasetningu með stillingar fyrir sjálfvirkni í bylgjusniðmátið. Frekari upplýsingar eru í [Stofna bylgjusniðmát](wave-templates.md).
>
> Ef notað er *Flutningsstjórnun* og *Ítarlegt vöruhúsakerfi* er hægt að tilgreina hvort eigi að sameina hleðslur þegar unnið er úr bylgju. Í þessu dæmi er gagnlegt þegar hægt er að senda nokkrar litlar hleðslur samtímis. Til að sameina hleðslur við bylgjuvinnslu, á **Hleðslur** flipanum, skal velja gátreitinn **Sameina hleðslur við framkvæmd bylgju** .</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Setja upp alla eða hluta frátekning fyrir framleiðslubylgjur

Fyrir sölupantanir og kanbanpantanir verður að taka frá birgðir áður en pöntun er losuð í vöruhús. Annars eru vörur eða úthlutunarlínur ekki hægt að vinna í bylgju. Framleiðslupantanir eru hins vegar örlítið sveigjanlegri. Fyrir framleiðslupantanir er hægt að tilgreina eftirfarandi:

- Leyfa framleiðslupantanir til að gefa út á vöruhús þó að ekki sé hægt að taka frá allt efni. Ef þessi valkostur er valinn verður handvirkt að endurtaka losun í vöruhúsaferli þegar viðbótar efni verða tiltækar. Þetta er til dæmis hentugt ef efnin sem þarf til að hefja framleiðslu eru til staðar og geta beðið þar til viðbótarefni verða tiltæk.
- Krefjast þess að allt efni sé tekið frá áður en pöntun er losuð í vöruhúsið.

Til að krefjast fullrar frátekningar eða leyfa hlutafrátekningu, skal fylgja þessum skrefum:

1. Farið í **Framleiðslustýring** \> **Uppsetning** \> **Færibreytur framleiðslustýringar**.
1. Á flipanum **Almennt**, í reitnum **Losa í vöruhús**, skal velja sjálfgefna stillingu.
