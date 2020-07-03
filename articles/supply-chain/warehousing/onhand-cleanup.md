---
title: Hreinsunarvinnsla lagerbirgðafærslna vöruhúsakerfis
description: Þetta efnisatriði lýsir hreinsunarvinnslu á lagerbirgðafærslum, sem eykur afköst kerfisins með því að auðkenna og eyða tengdum en ónauðsynlegum færslum.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f6d1f8a4c85c2161d1b79246d437bb3b4d223d1d
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410956"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Hreinsunarvinnsla lagerbirgðafærslna vöruhúsakerfis

Afköst fyrirspurna sem eru notaðar til að reikna lagerbirgðir verður fyrir áhrifum af færslufjöldanum í töflunum sem koma við sögu. Ein leið til að auka afköst er að draga úr fjölda færslna sem gagnagrunnurinn þarf að hafa í huga.

Þetta efnisatriði lýsir hreinsunarvinnslu á lagerbirgðafærslum, sem eyðir ónauðsynlegum færslum í töflunum InventSum og WHSInventReserve. Þessar töflur geyma upplýsingar um lager fyrir vörur sem eru virkar fyrir vinnslu vöruhúsakerfis. (Þessar vörur nefnast WHS-vörur.) Eyðing þessara færslna getur stóraukið afköst lagerútreikninga.

## <a name="what-the-cleanup-job-does"></a>Hvað gerir hreinsunarvinnslan

Hreinsunarvinnsla lagerbirgðafærslna eyðir öllum færslum í töflunum WHSInventReserve og InventSum þar sem öll reitargildi eru *0* (núll). Hægt er að eyða þessum færslum vegna þess að þær leggja ekki til upplýsingar um lagerbirgðir. Vinnslan eyðir aðeins færslum sem eru fyrir neðan stigið **Staðsetning**.

Ef neikvæðar efnislegar birgðir eru leyfðar er hugsanlegt að hreinsunarvinnslan geti ekki eytt öllum færslum sem eiga við. Ástæðan fyrir þessari takmörkun er sú að vinnslan verður að leyfa sérstakar aðstæður þar sem númeraplata er með mörg raðnúmer og eitt þessara raðnúmera er orðið neikvætt. Til dæmis verður kerfið með núll á lager á stigi númeraplötu þegar númeraplata er með +1 stk af raðnúmeri 1 og –1 stk af raðnúmeri 2. Við þessar sérstöku aðstæður eyðir vinnslan fyrst á breiddina, þar sem hún reynir fyrst að eyða á lægri stigum.

## <a name="schedule-and-configure-the-cleanup-job"></a>Áætla og skilgreina hreinsunarvinnsluna

Hreinsunarvinnsla lagerbirgðafærslna er tiltæk í **Birgðastjórnun \> Reglubundin verkefni \> Hreinsun \> Hreinsun lagerbirgðafærslna vöruhúsakerfis**. Notið staðlaðar vinnslustillingar til að stýra umfangi og áætlun fyrir keyrslu vinnslunnar. Þar að auki eru eftirfarandi stillingar í boði:

- **Eyða ef ekki uppfærðar í þetta marga daga** – Færið inn lágmarksfjölda daga sem vinnslan á að bíða áður en hún eyðir lagerbirgðafærslu sem hefur dottið niður í núll í magni. Notið þessa stillingu til að draga úr hættu á að eyða færslum á lager sem enn er verið að nota. Ef hreinsun á að fara fram sem fyrst skal annaðhvort slá inn *0* (núll) eða skilja reitinn eftir auðan.
- **Hámarkskeyrslutími (klukkustundir)** - Sláið inn hámarkskeyrslutíma hreinsunarvinnslu, í klukkustundum. Ef vinnslunni er ekki lokið áður en þessi tími rennur út, vistar hún vinnuna sem er lokið fram að þessu og lokar vinnslunni. Þessi möguleiki á sérstaklega við um innleiðingar með mikilli birgðanotkun. Í slíkum tilfellum ætti að áætla að keyra vinnsluna á tímum þegar er sem minnst álag á kerfinu. Ef halda á keyrslu runuvinnslunnar áfram þar til hún klárast skal slá inn *0* (núll) eða skilja reitinn eftir auðan. Þessi stilling er aðeins í boði ef tengdur eiginleiki hefur verið [kveikt á í kerfinu](#max-execution-time).

Þótt hægt sé að keyra vinnsluna á venjulegum vinnutíma er mælt með því að keyra hana utan vinnustunda. Þannig er komið í veg fyrir árekstra sem geta átt sér stað ef notandi er að vinna í færslu sem einnig er verið að hreinsa.

Ef vinnslan reynir að eyða færslu fyrir vöru á meðan annar notandi er að nota þá færslu, kemur upp sjálfhelduvilla hjá annaðhvort hreinsunarvinnslunni eða notandanum.

Þegar vinnslan er í gangi er hún með staðfestingarstærðina 100. Hún reynir sem sagt að staðfesta eitt skipti fyrir hverjar 100 eyðingar. Hins vegar, vegna þess að sumar eyðingar eru samstæðubyggðar, geta komið upp aðstæður þar sem hægt er að eyða meira en 100 skrám í sömu færslunni. Þess vegna geta stigvaxandi læsingar enn átt sér stað.

## <a name="possible-user-impact"></a>Hugsanleg áhrif á notanda

Notendur gætu orðið fyrir áhrifum ef hreinsunarvinnsla lagerbirgðafærslna eyðir öllum færslum fyrir uppgefið stig (t.d. númeraplötustigið). Í slíku tilfelli gæti aðgerðin til að sjá að birgðir séu til staðar á lager á númeraplötu ekki virkað sem skyldi vegna þess að viðeigandi lagerbirgðafærslur eru ekki lengur í boði. (Þessi aðgerð athugar skilyrðið **Magn \<\> 0** í stillingunum **Birting víddar** þegar notendur skoða lagerupplýsingar.) Hins vegar ættu aukin afköst sem hreinsunarvinnslan býður upp á að bæta upp fyrir þetta litla tap í virkni.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Gera stillingu hámarkskeyrslutíma tiltæka

Sjálfgefið er að stillingin **Hámarkskeyrslutími** sé ekki í boði. Ef ætlunin er að nota hann þarf að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á tengdum eiginleika í kerfinu. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Hámarkskeyrslutími á hreinsunarvinnslu lagerbirgðafærslna vöruhúsakerfis*
