---
title: Skrá efnisnotkun með fartæki
description: Þetta efnisatriði lýsir verkflæði sem gerir kleift að skrá hráefnanotkun í framleiðslu með því að nota lófatæki.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1aeb527255358ecafafcb64185cb9dcb31243d499c533f9c9390d79658534e3c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777864"
---
# <a name="register-material-consumption-using-a-mobile-device"></a>Skrá efnisnotkun með fartæki

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir verkflæði sem gerir kleift að skrá hráefnanotkun í framleiðslu með því að nota lófatæki.

## <a name="introduction"></a>Inngangur

Þessi verkflæði er við hæfi ef strangar kröfur eru um rekjanleika efnis. Í þeim tilvikum verður að skrá nákvæman tíma og magn í hráefnanotkun svo hægt sé að viðhalda rekjanleika þeirra. Það má bera þetta ferli saman við bakfærslukostnaðaraðferðir, þar sem það líður ákveðinn tími milli skráningar og þegar raunveruleg notkun á sér stað. Þetta skýrir hvers vegna er ekki hægt að nota áætlun fyrir sjálfvirka notkun fyrir sum hráefni sem hafa kröfu um rekjanleika. Lítum á einfalt dæmi sem útskýrir hvernig á að setja upp verkflæði til að virkja skráningu hráefnisnotkunar í framleiðslu með handfrjálsu tæki. [![setja upp verkflæði til að virkja skráningu hráefnisnotkunar með handfrjálsu tæki.](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Upplýsingar um dæmi

Stöðugt framleiðsluferli (5) notar runustýrða hráefnið RM-100. Hráefnið er tiltækt í lagerbirgðum í staðsetningu Laust 001 (1) á númeraplötu PL-1 með tvær runur, B1 og B2, hvor tveggja með 50 kg magn. Vöruhúsavinna (2) er útgefin og unnin fyrir RM-100 og hráefnið er tekið til úr Laust-001 í staðsetningu framleiðsluinntaks PIL-01 (3), sem er skilgreind sem staðsetning sem er ekki númeraplötustýrð. Starfsmaður á vél vigtar hráefnið út úr staðsetningu framleiðsluinntaks (3) og skráir þyngd og rununúmer eftir notkun (4). Úr staðsetningu framleiðsluinntaks er hluta af hráefninu bætt handvirkt við framleiðsluferlið með skilgreindu millibili. Þegar starfsmaður á vél bætir við hráefni er það vigtað á vigt og rununúmerið er skráð.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>Setja upp verkflæðið til að skrá notkun með handfrjálsu tæki
Búðu til fullunna afurð, FG-100, með uppskrift sem inniheldur runustýrða hráefnið RM-100. Bætið við tveimur runum, B1 og B2, af RM-100 í magninu 100 á staðsetningu: Bulk-001 á númeraplötu: PL-1. Losunarreglan í uppskriftarlínunni fyrir RM-100 er stillt á **Handvirkt**. Setjið staðsetningu framleiðsluinntaks á PIL-01. Það er hægt að gera með því að velja þessa staðsetningu sem sjálfgefna staðsetningu framleiðsluinntaks í vöruhúsi 51.

1.  Nýtt valmyndaratriði fartækis stofnað: 

-    **Nafn valmyndaratriðis** - Skrá efnisnotkun. 
-    **Heiti** - Skrá hráefnanotkun. 
-    **Máti** - Óbeint. 
-    **Verkþáttarkóði** - Skrá efnisnotkun.

2.  Bæta valmyndaratriði við valmyndina **Framleiðsla** í fartæki.
3.  Framleiðslupöntun fyrir fullunnu afurðina stofnuð: 

-    **Vörunúmer** - FG-100 
-    **Svæði** - 5 
-    **Vöruhús** - 51 
-    **Magn** - 150

Framleiðslupöntun er **Áætluð** og **Útgefin** og vöruhúsavinna er stofnuð.

4.  Ljúktu við verkið með verkflæðinu fyrir tiltekt hráefnis fyrir lófatækið.

Þetta færir hráefnið úr biðstaðsetningu í staðsetningu framleiðsluinntaks PIL-01. Eftir að vinnu er lokið er efnið með stöðuna **Tekið til á staðsetningu framleiðsluinntaks**. Staðan eftir að verk er fullunnið getur verið annaðhvort **Tekið til** eða **Frátekið á lager**. Það er skilgreint með færibreytunni **Gefa út stöðu eftir að sett er í skjámyndina vöruhús**.

5.  Settu framleiðslupöntunina í gang, annaðhvort úr biðlaranum eða úr lófatækinu með valmyndaratriðinu **Byrja framleiðslu**.

Eftir að framleiðslupöntun hefur verið ræst er hægt að skrá hráefnisnotkun með verkflæðinu fyrir lófatækið. Við skulum byrja á því að skrá notkun upp á 25 pund af runu B1.

6.  Veljið valmyndaratriðið **Skrá efni** **Notkun** í valmyndinni fyrir handfrjálsa tækið og sláið inn eftirfarandi upplýsingar: 

-    Númer framleiðslupöntunarinnar. 
-    Staðsetningin þar sem hráefnið verður notað er í þessu tilviki PIL-01. 
-    Vörunúmer RM-100. 
-    Rununúmer B1. 
-    Magn upp á 25.

7.  Veldu **Í lagi**.

Takið eftir að skilaboðin „Færslubókarlína er stofnuð“ birtast á skjánum. Í framleiðslupöntun er opin færslubók af gerðinni **Tiltektarlisti framleiðslu** fyrir vörunúmer RM-100 og rununúmer B1. 

Nú er hægt að velja að halda áfram skráninguna, til dæmis fyrir rununúmerið B2, og í hvert sinn sem þú velur **í lagi** er nýrri færslubókarlínu bætt við opna færslubók. 

Þegar skráningunni er lokið skal velja **Lokið** til að bóka færslubókina og ljúka verkflæðinu.

### <a name="additional-comments"></a>Frekari athugasemdir 

-   Ef notandi hættir verkflæðinu eftir að færslubókarlína er búin til, er færslubókin í með stöðuna óbókað en ef notandinn notar síðar meir verkflæðið fyrir sömu framleiðslupöntun, þá verður línunum bætt við opnu færslubókina frekar en nýja færslubók.
-   Nýja verkflæðið styður einnig skráningu raðnúmera.
-   Aðeins er hægt að skrá vörunúmer sem er skilgreint í uppskrift eða í formúlunni fyrir valda framleiðslupöntun eða runupöntun.
-   Hægt er að ofnota hráefni. Sem dæmi um þetta má nefna að ef ætlað er að nota hráefni með magnið 50 kg er hægt að ofnota það með magni sem til dæmis nemur 52 kg.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]