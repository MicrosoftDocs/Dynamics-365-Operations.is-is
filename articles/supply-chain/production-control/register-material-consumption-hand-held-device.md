---
title: "Skrá efnisnotkun með fartæki"
description: "Þetta efnisatriði lýsir verkflæði sem gerir kleift að skrá hráefnanotkun í framleiðslu með því að nota lófatæki."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: b84b63ec519ae686b55905170c956fcb2b08334a
ms.contentlocale: is-is
ms.lasthandoff: 03/08/2018

---

# <a name="register-material-consumption-using-a-mobile-device"></a>Skrá efnisnotkun með fartæki

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir verkflæði sem gerir kleift að skrá hráefnanotkun í framleiðslu með því að nota lófatæki.

<a name="introduction"></a>Inngangur
------------

Þetta verkflæði á við ef strangar kröfur gilda um rekjanleika hráefna. Í þeim tilvikum verður að skrá nákvæman tíma og magn í hráefnanotkun svo hægt sé að viðhalda rekjanleika þeirra. Það má bera þetta ferli saman við bakfærslukostnaðaraðferðir, þar sem það líður ákveðinn tími milli skráningar og þegar raunveruleg notkun á sér stað. Þetta skýrir hvers vegna er ekki hægt að nota áætlun fyrir sjálfvirka notkun fyrir sum hráefni sem hafa kröfu um rekjanleika. Skoðum einfalt dæmi sem útskýrir hvernig á að setja upp verkflæði til að gera kleift að skrá hráefnanotkun í framleiðslu með því að nota lófatæki. [![setja upp verkflæði til að virkja skráningu hráefnisnotkunar með handfrjálsu tæki ](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Upplýsingar um dæmi

Samfellt framleiðsluferli (5) notast við runustýrt hráefni RM-100. Hráefnið er tiltækt í lagerbirgðum í staðsetningu Laust 001 (1) á númeraplötu PL-1 með tvær runur, B1 og B2, hvor tveggja með 50 kg magn. Vöruhúsavinna (2) er útgefin og unnin fyrir RM-100 og hráefnið er tekið til úr Laust-001 í staðsetningu framleiðsluinntaks PIL-01 (3), sem er skilgreind sem staðsetning sem er ekki númeraplötustýrð. Starfsmaður á vél vigtar hráefnið út úr staðsetningu framleiðsluinntaks (3) og skráir þyngd og rununúmer eftir notkun (4). Úr staðsetningu framleiðsluinntaks er hluta af hráefninu bætt handvirkt við framleiðsluferlið með skilgreindu millibili. Þegar starfsmaður á vél bætir við hráefni er það vigtað á vigt og rununúmerið er skráð.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>Settu upp verkflæði til að skrá notkun með lófatæki
Stofnaðu fullunna vöru, FG-100, með uppskrift sem hefur runustýrða hráefnið RM-100. Bættu við tveimur runum, B1 og B2 af RM-100, í magninu 100 í staðsetningu: Laust-001 á númeraplötu: PL 1. Losunarreglan í uppskriftarlínunni fyrir RM-100 er stillt á **Handvirkt**. Stilltu staðsetningu framleiðsluinntaks á PIL-01. Það er hægt að gera með því að velja þessa staðsetningu sem sjálfgefna staðsetningu framleiðsluinntaks í vöruhúsi 51.

1.  Nýtt valmyndaratriði fartækis stofnað: 

-    **Heiti valmyndaratriðis** - Skrá hráefnanotkun. 
-    **Heiti** - Skrá hráefnanotkun. 
-    **Máti** - Óbeint. 
-    **Verkþáttarkóði** - Skrá hráefnanotkun.

2.  Bættu valmyndaratriðinu **Farframleiðsla** við valmynd tækis.
3.  Framleiðslupöntun fyrir fullunnu afurðina stofnuð: 

-    **Vörunúmer** - FG-100 
-    **Svæði** - 5 
-    **Vöruhús** - 51 
-    **Magn** - 150

Framleiðslupöntun er **Áætluð** og **Útgefin** og vöruhúsavinna er stofnuð.

4.  Ljúktu við verkið með verkflæðinu fyrir tiltekt hráefnis fyrir lófatækið.

Þetta færir hráefnið úr biðstaðsetningu í staðsetningu framleiðsluinntaks PIL-01. Að verkinu loknu hefur hráefnið stöðuna **Tekið til á staðsetningu framleiðsluinntaks**. Staðan eftir að verk er fullunnið getur verið annaðhvort **Tekið til** eða **Frátekið á lager**. Það er skilgreint með færibreytunni **Gefa út stöðu eftir að sett er í skjámyndina vöruhús**.

5.  Settu framleiðslupöntunina í gang, annaðhvort úr biðlaranum eða úr lófatækinu með valmyndaratriðinu **Byrja framleiðslu**.

Eftir að framleiðslupöntun hefur verið ræst er hægt að skrá hráefnisnotkun með verkflæðinu fyrir lófatækið. Byrjum á því að skrá notkun á 10 kg af runu B1.

6.  Veldu valmyndaratriðið **Skrá** **hráefnisnotkun** í valmyndinni fyrir lófatækið og færðu inn eftirfarandi upplýsingar: 

-    Númer framleiðslupöntunarinnar. 
-    Staðsetningin þar sem hráefnið verður notað er í þessu tilviki PIL-01. 
-    Vörunúmer RM-100. 
-    Rununúmer B1. 
-    Magn 25.

7.  Veldu **Í lagi**.

Athugið að skilaboðin "Færslubókarlína var stofnuð" birtast á skjánum. Í framleiðslupöntun er opin færslubók af gerðinni **Tiltektarlisti framleiðslu** fyrir vörunúmer RM-100 og rununúmer B1. 

Nú er hægt að velja að halda áfram skráninguna, til dæmis fyrir rununúmerið B2, og í hvert sinn sem þú velur **í lagi** er nýrri færslubókarlínu bætt við opna færslubók. 

Eftir að þú hefur lokið við skráningu skaltu velja **Lokið** til að bóka færslubókina og binda enda á verkflæðið.

### <a name="additional-comments"></a>Frekari athugasemdir 

-   Ef notandi hættir í verkflæði eftir að færslubókarlína er stofnuð er færslubókin óbókuð, en ef notandi notar verkflæðið síðar fyrir sömu framleiðslupöntun verður línunum bætt við opna færslubók í stað nýrrar færslubókar.
-   Nýja verkflæðið styður einnig skráningu raðnúmera.
-   Aðeins er hægt að skrá vörunúmer sem er skilgreint í uppskrift eða í formúlunni fyrir valda framleiðslupöntun eða runupöntun.
-   Hægt er að ofnota hráefni. Sem dæmi um þetta má nefna að ef ætlað er að nota hráefni með magnið 50 kg er hægt að ofnota það með magni sem til dæmis nemur 52 kg.



