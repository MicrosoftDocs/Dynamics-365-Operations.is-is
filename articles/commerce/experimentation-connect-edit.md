---
title: Tengja tilraun og breyta afbrigðum
description: Þetta efnisatriði lýsir því hvernig á að tengja tilraun í þjónustu þriðja aðila við Dynamics 365 Commerce og hvernig á að breyta afbrigðum fyrir tilraunina.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 030640ba8907ae52c198ac96ad2c243b533d8c53
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/22/2020
ms.locfileid: "4413299"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Tengja tilraun og breyta afbrigðum

Þetta efnisatriði lýsir því hvernig á að tengja tilraunina í Commerce og gera breytingar á afbrigðum þannig að þau samræmist tilgátunni. 

Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Önnur skref eru afgreidd í aðskildum efnisatriðum.

[ ![Tilraunastarfssemi notanda - Tengja og breyta](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Þegar [búið er að setja upp tilraunina](experimentation-setup.md) í þjónustu þriðja aðila skal tengja tilraunina við Dynamics 365 Commerce og breyta afbrigðum tilraunarinnar.

## <a name="planning-considerations"></a>Athugunarefni við gerð verkefnaáætlunar

Áður en þú tengir tilraunina þína í Commerce þarftu að taka nokkrar ákvarðanir sem hafa áhrif á það hvernig Commerce hefur umsjón með efninu þínu.

### <a name="determine-the-scope-of-your-experiment"></a>Ákvarða umfang tilraunarinnar
Þegar tilraun er tengd er beðið um að skilgreina umfang tilraunarinnar. Tilraunir eru skilgreindar með umfang **að hluta** eða **allt** .
- Veljið **að hluta** ef framkvæma á tilraun á tilteknum hluta síðu. Ef þessi valkostur er valinn verður að auðkenna hvaða einingar eru teknar með í tilrauninni. Breytingar sem eru gerðar á hlutum sjálfgefinnar síðu eða broti sem er ekki tengt tilrauninni eru sjálfkrafa samstillt á milli afbrigða.
- Veljið **allt** ef framkvæma á tilraun á heilli síðu eða broti. Aðskilin afrit af sjálfgefinni síðu eða hluta eru stofnuð. Ekki þarf að velja hvaða einingar eru hafðar með í tilrauninni vegna þess að hægt er að breyta öllu útlitinu. Hægt er að bæta við, eyða eða endurraða einingum eins og þörf er á. Ef einhverjar breytingar eru hins vegar gerðar á sjálfgefinni síðu eða broti sem tilraunin tengist verða þessar breytingar að vera samstilltar handvirkt yfir öll afbrigðin.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Ef þú tengir tilraunina þína við síðu sem notar útlit er aðeins hægt að stilla umfang tilraunarinnar á **allt**.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Ákveða hvort eigi að tímasetja hvenær tilraunin verður gefin út
Ef ætlunin er að tímasetja hvenær tilraunin er birt á lifandi svæðinu, skal ganga úr skugga um efnið sem tengja á við tilraunina sé tiltækt í birtingarhóp *áður en* þú tengir tilraunina. 

Frekari upplýsingar um birtingarhópa er að finna í [Vinna með birtingarhópa](publish-groups.md).


## <a name="connect-your-experiment"></a>Tengja tilraun
Til að tengja tilraunina þarf að ræsa leiðsagnarforritið **Tengja tilraun**. Leiðsagnarforritið fer með þér í gegnum skrefin sem þarf til að tengja tilraunina. Þegar leiðsagnarforritinu er lokið er tillraunin tengd og afbrigði eru búin til og þau tilbúin fyrir breytingar.

Til að hefjast handa við að tengjasting tilraun í Commerce svæðasmíð skal fylgja þessum skrefum.

1. Til að ræsa **Connect-tilraun** leiðsagnarforritið skal velja **Tilraunir** í vinstra yfirlitssvæði og síðan velja **Tengja**. Einnig er hægt að opna leiðsagnarforritið af síðu eða broti með því að breyta því og velja **Connect tilraun** á skipanastikunni.

    > [!NOTE]
    > Síða getur aðeins verið tengd við eina tilraun í einu. Til að tengja síðu við aðra tilraun skal fyrst eyða tilrauninni sem síðan er tengd við.

1. Veldu síðuna eða hlutann sem þú vilt keyra tilraunina þína á.
1. Stilltu umfang tilraunir á **að hluta** eða **allt** samkvæmt valinu þínu í hlutanum [Ákvarða umfang tilraunarinnar](#determine-the-scope-of-your-experiment) hér að ofan.
    > [!NOTE]
    > Virkja verður flagg eiginleikans **Tilraun á síðum eða broti** ef ætlunin er að gera tilraun á heilli síðu eða síðubroti. Frekari upplýsingar er að finna í efnisatriðinu [Tilraunir í Dynamics 365 Commerce](experimentation-overview.md).
    
1. Í lokaskrefi leiðsagnarforritsins skal velja **Búa til afbrigði og hætta í leiðsagnarforritinu**. Afbrigði eru búin til fyrir tilraunina. 

## <a name="edit-your-variations"></a>Breyta afbrigðum
Þegar farið er út úr leiðsagnarforritinu eru afbrigði stofnuð fyrir þig. 

Því næst skaltu breyta afbrigðunum þannig að þau endurspegli valkostina sem þú þarft að sannprófa í tilgátu tilraunarinnar. Veldu eina af eftirfarandi ferlum sem samsvarar umfanginu sem þú valdir fyrir tilraun þína í hlutanum [Ákvarða umfang tilraunarinnar](#determine-the-scope-of-your-experiment) hér að ofan.

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Breyta afbrigðum fyrir tilraunir með umfang að hluta til
Fylgið eftirfarandi skrefum ef umfang tilraunarinnar var skilgreint sem **að hluta** í leiðsagnarforritinu **Tengja tilraun**.

1. Í yfirliti ritils skal nota fellivalmynd afbrigðanna fyrir neðan skipanastikuna til að breyta hverju afbrigði fyrir sig samkvæmt upprunalegu tilgátunni. Þú gætir einnig viljað setja upp samanburðar- eða grunnafbrigði með því að skilja eitt þessarar afbrigða eftir óbreytt.
1. Veldu eininguna sem á að gera tilraunir á, veldu úrfellingarmerkið (...) og veldu síðan **Bæta við tilraun**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Breyta afbrigðum fyrir tilraunir með fullt umfang
Ef þú skilgreindir umfang tilraunarinnar sem **allt** í leiðsagnarforritinu **Tengja tilraun**, skaltu í yfirliti ritils skal nota fellivalmynd afbrigðanna fyrir neðan skipanastikuna til að breyta hverju afbrigði fyrir sig samkvæmt upprunalegu tilgátunni. 

> [!NOTE]
> Hvort sem verður fyrir valinu, gætir þú einnig viljað setja upp samanburðar- eða grunnafbrigði með því að skilja eitt þessarar afbrigða eftir óbreytt.

## <a name="previous-step"></a>Fyrra skref
[Setja upp tilraun](experimentation-setup.md) 


## <a name="next-step"></a>Næsta skref
[Forskoða og birta tilraun](experimentation-preview-publish.md)
