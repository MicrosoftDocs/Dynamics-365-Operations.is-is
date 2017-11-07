---
title: "Fjárhagsvíddir"
description: "Þessi efnisgrein lýsir ýmsum gerðum fjárhagsvídda og hvernig þær eru settar upp."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3950dc3fcd1e293802c88bf2616a27e139b48399
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="financial-dimensions"></a>Fjárhagsvíddir

[!include[banner](../includes/banner.md)]

Þessi efnisgrein útskýrir ýmsar gerðir fjárhagsvídda og hvernig þær eru settar upp.

Nota skal skjámyndina **Fjárhagsvíddir** til að stofna fjárhagsvíddir sem nota má sem hluta lykils fyrir bókhaldslykla. Til eru tvær gerðir fjárhagsvídda: sérsniðnar víddir og afritaðar víddir. Sérsniðnar víddir eru samnýttar á milli lögaðila og gildi eru færð inn og þeim stjórnað af notendum. Fyrir afritaðar víddir eru víddir hvers gildis skilgreindar annars staðar í kerfinu, eins og Viðskiptavinum eða Verslunum. Sumar afritaðar víddir eru samnýttar á milli lögaðila, en aðrar afritaðar víddir eru bundnar fyrirtækjum. 

Eftir að búið er að stofna fjárhagsvíddir skal nota síðuna **Fjárhagsvíddargildi** til að úthluta fleiri eiginleikum fyrir hverja fjárhagsvídd. 

Hægt er að nota fjárhagsvíddir til að tákna lögaðila. Ekki þarf að stofna á lögaðila í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Hins vegar eru kostnaðarjafnaðar fjárhagsvíddir ekki hannaðar til að taka á rekstrar- eða viðskiptaþörfum lögaðila. Eiginlekin millieiningabókhalds í Finance and Operations er hannaður til að eiga aðeins við bókhaldsfærslur sem eru stofnaðar fyrir hverja færslu. 

Áður en fjárhagsvíddir eru settar upp sem lögaðilar skal meta viðskiptaferli á eftirfarandi svæðum til að ákvarða hvort þessi uppsetning muni gagnast fyrirtækinu:

- Birgðir
- Sölu og innkaup milli fjárhagsvíddir og lögaðila
- útreikningur VSK og skýrslugerð
- Aðgerðaskýrslugerð

Hér eru sumar af skorðunum:

- Hægt er að nota virkni virðisaukaskatts ekki með fjárhagsvíddum, aðeins við lögaðila.
- Sumar skýrslur innihalda ekki fjárhagsvíddir. Þar af leiðandi gæti þurft að breyta skýrslunum til að gera skýrslu eftir fjárhagsvídd.

## <a name="custom-dimensions"></a>Sérsniðnar víddir

Til að stofna notandaskilgreinda fjárhagsvídd er í reitnum **Nota gildi frá** valin **&lt; Sérsniðin vídd &gt;**. Einnig er hægt að tilgreina lykilsíu til að takmarka magn og gerð upplýsinga sem hægt er að færa inn víddargildi fyrir. Hægt er að færa inn stafi sem eru þeir sömu og fyrir hvert víddargildi eins og stafi eða bandstrik (-). Einnig er hægt að slá inn tölumerki (\#) og og-merki (&) sem frátakara fyrir stafi og tölur sem breytast í hvert skipti sem víddargildi er stofnað. Notaðu tölumerki (\#) sem frátakara fyrir tölu og og-merki (&) sem frátakara fyrir staf. Reiturinn fyrir sniðsíuna er aðeins tiltækur þegar valið er **&lt; Sérsniðin vídd &gt;** í reitnum **Nota gildi frá**.

**Dæmi**

Til að takmarka víddargildi við stafina „CC“ og þrjár tölur færirðu inn **CC-\#\#\#** sem sniðsíu.

## <a name="entity-backed-dimensions"></a>Einingastuddar víddir

Að búa til einingastuddar fjárhagsvíddir skal í svæðinu **Nota gildi frá** velja kerfisskilgreindar einingar til að byggja fjárhagsvídd á. Fjárhagsvíddargildi eru síðan stofnuð úr þeirri einingu. Til dæmis skal velja Verk til að stofna víddargildi fyrir **Verk**. Víddargildi eru síðan stofnuð fyrir hvert heiti verks. Síðan **Fjárhagsvíddargildi** sýna gildi fyrir eininguna. Ef þessi gildi eru bundin tilteknu fyrirtæki sýnir síðan einnig fyrirtækið.

## <a name="activating-dimensions"></a>Notkun vídda

Þegar fjárhagsvídd er virkjuð er taflan uppfærð þannig að hún felur í sér heiti fjárhagsvíddarinnar. Eyddar víddir eru fjarlægðar. Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð. Hins vegar er ekki hægt að nota fjárhagsvídd neins staðar fyrri en hún er gerð virk. Til dæmis er ekki hægt að bæta fjárhagsvídd við lykilskipulag þar til að fjárhagsvídd hefur verið virkjuð. Þegar smellt er á **Virkja** eru allar víddir uppfærðar og sýna stöðu breytingar. 

## <a name="translations"></a>Þýðingar

Á síðunni **Textaþýðing** er hægt að færa inn texta fyrir valda fjárhagsvídd á mismunandi tungumálum. Á síðunni **Þýðing aðallykils** er hægt að færa inn texta fyrir aðallykil á mismunandi tungumálum. 

## <a name="legal-entity-overrides"></a>Lögaðili hnekkir

Ekki eru allar víddir gildar fyrir alla lögaðila. Þar að auki kunna sumar víddir að vera aðeins viðeigandi fyrir tiltekið tímabil. Í þessum tilfellum er hægt að nota hlutann **Lögaðili hnekkir** til að tilgreina hvaða fyrirtæki ætti ekki að nota víddir fyrir, hver er eigandi og tímabilið sem víddin er virk.

## <a name="deleting-financial-dimensions"></a>Eyðing fjárhagsvídda

Til að viðhalda heilleika gagna er sjaldan hægt að eyða fjárhagsvíddum. Ef reynt er að eyða fjárhagsvíddum eru eftirfarandi skilyrði metin:

- Hefur fjárhagsvíddin verið notuð á einhverjar bókaðar eða óbókaðar færslur eða einhverja gerð af víddarsamsetningu gilda?
- Er fjárhagsvíddin notuð í öllu virku lykilskipulagi, ítarleg reglu skipulag fjárhagsvídd eða fjárhagsvídd set?
- Er fjárhagsvídd hluti af sjálfgefinu samþættingarsniði fjárhagsvíddar?
- Hefur fjárhagsvídd verið uppsett sem sjálfgefin vídd?

Ef einhverjum skilyrðum er mætt er ekki hægt að eyða fjárhagsvíddinni.


Frekari upplýsingar er hægt að finna í eftirfarandi efni:
- [Skilgreina fjárhagsvíddir](tasks/define-financial-dimensions.md)
- [Viðhalda sjálfgefnum sniðmátum fjárhagsvídda](tasks/maintain-financial-dimension-default-templates.md)

